# Extensibilidade: Agentes, Skills, Plugins e MCP

## Visao geral

O runtime foi desenhado para extensao em varias frentes ao mesmo tempo. O projeto nao depende apenas de um catalogo fixo de comandos e ferramentas; ele inclui mecanismos para incorporar comportamento novo por configuracao, disco, plugins e servidores externos.

## Agentes

### Arquivo-chave

- `../../codigo_principal/claude_code_src/tools/AgentTool/loadAgentsDir.ts`

### O que esse modulo mostra

O loader de agentes aceita agentes:

- built-in;
- de plugin;
- de user settings;
- de project settings;
- de policy settings;
- de flag settings.

O schema tambem revela que um agente pode configurar:

- prompt;
- descricao e when-to-use;
- lista de ferramentas permitidas e proibidas;
- modelo e esforco;
- permission mode;
- MCP servers;
- hooks;
- memoria;
- isolamento em worktree ou remoto;
- background execution.

## Skills

### Pastas centrais

- `../../codigo_principal/claude_code_src/skills/`
- `../../codigo_principal/claude_code_src/skills/bundled/`

## Plugins

### Pastas centrais

- `../../codigo_principal/claude_code_src/plugins/`
- `../../codigo_principal/claude_code_src/utils/plugins/`
- `../../codigo_principal/claude_code_src/commands/plugin/`

## MCP

### Pastas centrais

- `../../codigo_principal/claude_code_src/services/mcp/`
- `../../codigo_principal/claude_code_src/components/mcp/`
- `../../codigo_principal/claude_code_src/commands/mcp/`
- `../../codigo_principal/claude_code_src/tools/ListMcpResourcesTool/`
- `../../codigo_principal/claude_code_src/tools/ReadMcpResourceTool/`

## Hooks e configuracao

### Pastas e arquivos centrais

- `../../codigo_principal/claude_code_src/utils/hooks/`
- `../../codigo_principal/claude_code_src/commands/hooks/`
- `../../codigo_principal/claude_code_src/utils/settings/`

## Onde a extensibilidade aparece no estado

`state/AppStateStore.ts` deixa visivel que o runtime incorpora extensibilidade no proprio estado global:

- `mcp`
- `plugins`
- `agentDefinitions`
- `tasks`
- `sessionHooks`

## Trilha de leitura para este tema

1. `tools/AgentTool/loadAgentsDir.ts`
2. `skills/`
3. `commands/plugin/`
4. `utils/plugins/`
5. `services/mcp/`
6. `state/AppStateStore.ts`
