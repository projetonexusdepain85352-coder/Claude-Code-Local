# Subsistemas do Runtime

## Panorama quantitativo

Na base principal, os modulos superiores mais volumosos sao:

| Modulo | Arquivos | Papel dominante |
|---|---:|---|
| `components/` | 389 | interface, dialogs, visualizacao de mensagens, permissoes e menus |
| `commands/` | 207 | comandos slash e operacoes auxiliares |
| `tools/` | 184 | ferramentas que o modelo pode invocar |
| `services/` | 130 | integracoes e orquestradores de infraestrutura |
| `hooks/` | 104 | costura entre UI, estado e eventos |
| `ink/` | 96 | camada de terminal e renderizacao |
| `utils/` | 52 | utilitarios transversais |
| `bridge/` | 31 | controle remoto, bridge e sessao remota |
| `constants/` | 21 | configuracoes estaticas e chaves centrais |
| `skills/` | 20 | carregamento e registro de skills |

## Subsistema de comandos

### Centro nervoso

- `../../codigo_principal/claude_code_src/commands.ts`

### Subareas de maior peso

| Submodulo | Arquivos | Observacao |
|---|---:|---|
| `commands/plugin/` | 17 | navegacao, marketplace, validacao e gestao de plugins |
| `commands/install-github-app/` | 14 | fluxo guiado de instalacao da app GitHub |
| `commands/review/` | 4 | comandos ligados a review |
| `commands/mcp/` | 4 | comandos para infraestrutura MCP |
| `commands/clear/` | 4 | limpeza de caches e conversa |

## Subsistema de ferramentas

### Centros nervosos

- `../../codigo_principal/claude_code_src/tools.ts`
- `../../codigo_principal/claude_code_src/Tool.ts`

### Subareas de maior peso

| Submodulo | Arquivos | Observacao |
|---|---:|---|
| `tools/AgentTool/` | 20 | agentes customizados, definicoes, spawn e resume |
| `tools/BashTool/` | 18 | shell, execucao e controles de permissao |
| `tools/PowerShellTool/` | 14 | camada equivalente para ambientes PowerShell |
| `tools/LSPTool/` | 6 | integracao de linguagem |
| `tools/FileEditTool/` | 6 | edicao de arquivos |

## Subsistema de servicos

### Subareas de maior peso

| Submodulo | Arquivos | Observacao |
|---|---:|---|
| `services/mcp/` | 23 | conexao, configuracao, recursos e comandos MCP |
| `services/api/` | 20 | cliente do modelo, retry, logging, erros e custos |
| `services/compact/` | 11 | estrategias de reducao de contexto |
| `services/analytics/` | 9 | telemetria, sinks e tracing |
| `services/lsp/` | 7 | suporte a linguagem |

## Subsistema de UI

`components/` e o maior modulo superior do projeto, com destaque para:

| Submodulo | Arquivos | Observacao |
|---|---:|---|
| `components/permissions/` | 51 | dialogs e pedidos de permissao |
| `components/messages/` | 41 | renderizacao e manipulacao de transcript |
| `components/agents/` | 26 | UI e fluxos ligados a agentes |
| `components/PromptInput/` | 21 | entrada principal de prompt |
| `components/design-system/` | 16 | base visual reutilizavel |

### Arquivo-chave

- `../../codigo_principal/claude_code_src/screens/REPL.tsx`

## Subsistema de estado

### Centros principais

- `state/AppStateStore.ts`
- `state/store.ts`
- `context/`
- `bootstrap/state.ts`

## Subsistema remoto e colaborativo

### Pastas centrais

- `bridge/`
- `remote/`
- `server/`
- `tasks/`
- `tools/AgentTool/`

## Subsistema de memoria e contexto

### Pastas centrais

- `memdir/`
- `query/`
- `services/compact/`
- `utils/messages.js`
- `utils/queryContext.js`
