# Mapa de Modulos do Codigo Principal

## Arquivos-raiz do runtime

| Arquivo | Papel |
|---|---|
| `../../codigo_principal/claude_code_src/entrypoints/cli.tsx` | entrada leve do processo, fast paths e dispatch inicial |
| `../../codigo_principal/claude_code_src/main.tsx` | bootstrap pesado e composicao do runtime |
| `../../codigo_principal/claude_code_src/QueryEngine.ts` | classe que encapsula uma conversa persistente |
| `../../codigo_principal/claude_code_src/query.ts` | loop principal agente-ferramenta |
| `../../codigo_principal/claude_code_src/Tool.ts` | contrato de ferramentas, contexto e permissoes |
| `../../codigo_principal/claude_code_src/tools.ts` | registro mestre de ferramentas |
| `../../codigo_principal/claude_code_src/Task.ts` | contrato de tarefas |
| `../../codigo_principal/claude_code_src/tasks.ts` | registro mestre de tarefas |
| `../../codigo_principal/claude_code_src/commands.ts` | registro mestre de comandos |
| `../../codigo_principal/claude_code_src/context.ts` | composicao de contexto de sistema e usuario |
| `../../codigo_principal/claude_code_src/history.ts` | historico e referencias de mensagens |

## Diretorios superiores

| Diretorio | Papel principal | Observacoes |
|---|---|---|
| `assistant/` | modulos condicionais de assistant mode | feature-gated |
| `bootstrap/` | estado e boot compartilhado | suporte a inicializacao |
| `bridge/` | remote control e bridge session | integra sessao local/remota |
| `buddy/` | companion e observadores auxiliares | UX adicional |
| `cli/` | handlers e transportes de CLI | caminhos headless e especializados |
| `commands/` | comandos slash e operacoes de usuario | 207 arquivos |
| `components/` | UI do terminal | maior modulo superior |
| `constants/` | tabelas, chaves e configuracoes estaticas | base de varios subsistemas |
| `context/` | providers e contexto de runtime/UI | stats, notifications etc. |
| `coordinator/` | modos coordenados | feature-gated |
| `entrypoints/` | entradas de processo e SDK | bootstrap e adaptadores |
| `hooks/` | costura entre UI, runtime e eventos | 104 arquivos |
| `ink/` | infraestrutura de terminal/render | 96 arquivos |
| `keybindings/` | atalhos e resolucao de comandos de teclado | UI interativa |
| `memdir/` | memoria persistente e descoberta de contexto | apoio ao prompt |
| `migrations/` | migracoes de configuracao e defaults | evolucao do produto |
| `plugins/` | plugins bundled e base de integracao | extensibilidade |
| `query/` | funcoes auxiliares do loop principal | tokens, config, stop hooks |
| `remote/` | sessoes e adaptadores remotos | complementar a bridge |
| `schemas/` | schemas centrais | pequeno e especializado |
| `screens/` | telas de alto nivel | REPL, Doctor, Resume |
| `server/` | bootstrap de sessao remota direta | conexao e direct connect |
| `services/` | integracoes e mecanismos transversais | API, MCP, compact etc. |
| `skills/` | skills bundled e carregadores | extensibilidade |
| `state/` | store e shape do estado global | centro da UI |
| `tasks/` | implementacoes de tasks | background e agentes |
| `tools/` | implementacoes de ferramentas | 184 arquivos |
| `types/` | tipos centrais | mensagens, ids, logs etc. |
| `utils/` | utilitarios transversais | suporte geral |

## Diferenca entre base principal e referencia complementar

A base principal em `../../codigo_principal/claude_code_src/` cobre o runtime foco deste acervo.

A referencia complementar em `../../referencia_sanbuphy/fonte_original/src/` preserva uma arvore semelhante, mas:

- inclui tambem `vim/` e `voice/`;
- traz contexto de build pelo `package.json`;
- serve como apoio comparativo, nao como substituto automatico da base principal.
