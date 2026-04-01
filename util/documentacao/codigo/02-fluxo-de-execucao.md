# Fluxo de Execucao

## Visao geral

O runtime tem dois caminhos principais:

- caminho interativo, centrado no REPL;
- caminho headless/SDK, centrado em `QueryEngine`.

Ambos compartilham os mesmos registradores de ferramentas, servicos de API e boa parte das regras de contexto, permissao e mensagens.

## Fluxo 1: inicializacao do processo

### Etapa A: `entrypoints/cli.tsx`

O processo inicia por `entrypoints/cli.tsx`, que executa tres tipos de decisao:

1. fast paths baratos como `--version`;
2. modais especializados como bridge, daemon, bg sessions e runners;
3. carga do runtime completo apenas quando necessario.

### Etapa B: `main.tsx`

Quando o fast path nao encerra o processo, `main.tsx` entra como bootstrap pesado:

- prepara side effects e leituras de ambiente;
- carrega configuracoes, auth e telemetry;
- resolve comandos, ferramentas e estado inicial;
- escolhe o caminho interativo ou nao interativo.

## Fluxo 2: sessao interativa REPL

### Etapa A: montagem da tela

`screens/REPL.tsx` monta a sessao interativa com:

- transcript;
- prompt input;
- barras de status;
- notificacoes;
- componentes de permissao;
- tarefas em background;
- integracoes IDE/MCP/bridge.

### Etapa B: submissao de prompt

Quando o usuario envia um prompt, o REPL:

1. prepara contexto e mensagens;
2. resolve ferramentas e comandos ativos;
3. consulta contexto de sistema e memoria;
4. chama `query(...)`.

### Etapa C: loop agente-ferramenta

`query.ts`:

1. emite evento de inicio de request;
2. chama a API do modelo;
3. recebe blocos de resposta;
4. detecta `tool_use`;
5. envia os usos de ferramenta para execucao;
6. agrega `tool_result`;
7. decide se continua o turno ou encerra.

### Etapa D: execucao de ferramentas

Existem dois caminhos principais:

- `services/tools/toolOrchestration.ts`: particiona chamadas em lotes concorrentes ou seriais;
- `services/tools/StreamingToolExecutor.ts`: executa ferramentas enquanto elas chegam no streaming, preservando ordem observavel.

### Etapa E: retorno ao transcript

As mensagens, tool results, avisos e eventos de progresso voltam para a lista de mensagens do REPL, o `AppState` e a persistencia de sessao.

## Fluxo 3: sessao headless ou SDK

### `QueryEngine.ts`

No caminho nao interativo, `QueryEngine` encapsula o estado de uma conversa. O metodo `submitMessage()`:

1. fixa `cwd` e contexto da conversa;
2. prepara permissao, caches e prompts;
3. chama `query(...)`;
4. transforma a saida do loop em mensagens do SDK;
5. acumula uso, status e persistencia.

## Fluxo 4: permissao e seguranca

O controle de permissao atravessa todo o sistema:

- `Tool.ts` define `ToolPermissionContext` e o contrato de execucao;
- `useCanUseTool` decide autorizacoes em runtime;
- `AppStateStore.ts` carrega o contexto de permissoes na UI;
- ferramentas que alteram sistema de arquivos, shell ou rede passam por esse gate.

## Fluxo 5: API e recuperacao

`services/api/claude.ts` e a camada de integracao com o modelo. Ela coordena:

- betas e headers dinamicos;
- normalizacao de mensagens;
- streaming;
- retry com `withRetry`;
- custo, limites e telemetria;
- correlacao entre mensagens, modelos e ferramentas.

`query.ts` acopla essa camada a mecanismos de recuperacao como:

- retries por erro de API;
- tratamentos de `prompt too long`;
- recuperacao de `max_output_tokens`;
- compactacao reativa ou preventiva;
- stop hooks.

## Fluxo 6: compactacao

O runtime inclui uma familia inteira de modulos em `services/compact/` para:

- reduzir historico;
- inserir fronteiras de compactacao;
- reconstruir mensagens posteriores;
- limitar crescimento de contexto.

## Fluxo 7: persistencia e restauracao

O sistema salva e restaura estado por meio de utilitarios como:

- `utils/sessionStorage.js`
- `utils/conversationRecovery.js`
- `utils/sessionRestore.js`
- `history.ts`
- `fileHistory.js`

## Leitura orientada por fluxo

Se voce quiser seguir o runtime em ordem quase cronologica, abra:

1. `../../codigo_principal/claude_code_src/entrypoints/cli.tsx`
2. `../../codigo_principal/claude_code_src/main.tsx`
3. `../../codigo_principal/claude_code_src/screens/REPL.tsx`
4. `../../codigo_principal/claude_code_src/QueryEngine.ts`
5. `../../codigo_principal/claude_code_src/query.ts`
6. `../../codigo_principal/claude_code_src/services/tools/toolOrchestration.ts`
7. `../../codigo_principal/claude_code_src/services/tools/StreamingToolExecutor.ts`
8. `../../codigo_principal/claude_code_src/services/api/claude.ts`
