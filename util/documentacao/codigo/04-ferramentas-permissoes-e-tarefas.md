# Ferramentas, Permissoes e Tarefas

## Contrato central das ferramentas

O arquivo mais importante para entender como o runtime conversa com o mundo externo e:

- `../../codigo_principal/claude_code_src/Tool.ts`

Ele define:

- tipos de schema de entrada;
- contexto de uso de ferramenta;
- contexto de permissao;
- tipos de progresso;
- contratos para atualizacao de UI, estado e notificacoes.

## Registro e disponibilizacao

### `tools.ts`

Esse arquivo faz quatro trabalhos:

1. enumera as ferramentas base;
2. aplica gates por feature flag e ambiente;
3. filtra por disponibilidade real;
4. expande o conjunto com ferramentas opcionais ou internas.

Entre as ferramentas visiveis no registro estao:

- `AgentTool`
- `BashTool`
- `FileReadTool`
- `FileEditTool`
- `FileWriteTool`
- `WebFetchTool`
- `WebSearchTool`
- `LSPTool`
- `PowerShellTool`
- ferramentas de task management;
- ferramentas de plan/worktree;
- ferramentas de skill, MCP e mensagens entre agentes.

## Orquestracao de execucao

### `services/tools/toolOrchestration.ts`

Esse modulo recebe blocos `tool_use` e decide se podem rodar:

- em paralelo, quando forem considerados concurrency-safe;
- em serie, quando puderem alterar estado compartilhado ou forem potencialmente perigosos.

### `services/tools/StreamingToolExecutor.ts`

Esse executor cobre o caso mais complexo: ferramentas que chegam por streaming antes do termino completo da resposta do modelo. Ele:

- enfileira tool uses;
- inicia execucao conforme a politica de concorrencia;
- preserva ordem de emissao observavel;
- gera erros sinteticos quando ocorre fallback, interrupcao ou erro paralelo.

## Sistema de permissoes

### Centro conceitual

- `ToolPermissionContext` em `Tool.ts`
- `AppState.toolPermissionContext` em `state/AppStateStore.ts`

### O que o contexto de permissao contem

- modo de permissao atual;
- diretorios adicionais liberados;
- regras always allow, always deny e always ask;
- disponibilidade de bypass e auto mode;
- sinalizadores para suprimir prompts ou aguardar verificacoes automatizadas.

## Tarefas

### Registro

- `../../codigo_principal/claude_code_src/tasks.ts`
- `../../codigo_principal/claude_code_src/Task.ts`

### Tipos centrais registrados

`tasks.ts` expoe um registro pequeno, mas estrategico:

- `LocalShellTask`
- `LocalAgentTask`
- `RemoteAgentTask`
- `DreamTask`
- tasks opcionais de workflow e monitoramento

## Como estudar esse subsistema

1. Abra `Tool.ts` para entender os contratos.
2. Leia `tools.ts` para ver o catalogo e os gates.
3. Leia `services/tools/toolOrchestration.ts` para a politica de batching.
4. Leia `services/tools/StreamingToolExecutor.ts` para a execucao em streaming.
5. Leia `tasks.ts` e `Task.ts` para entender o modelo de tarefas.
