# Leitura Orientada por Objetivo

## Se voce quer entender o bootstrap

Abra nesta ordem:

1. `../../codigo_principal/claude_code_src/entrypoints/cli.tsx`
2. `../../codigo_principal/claude_code_src/main.tsx`
3. `../../codigo_principal/claude_code_src/entrypoints/init.ts`
4. `../../codigo_principal/claude_code_src/bootstrap/state.ts`

## Se voce quer entender como o prompt vira resposta

Abra nesta ordem:

1. `../../codigo_principal/claude_code_src/QueryEngine.ts`
2. `../../codigo_principal/claude_code_src/query.ts`
3. `../../codigo_principal/claude_code_src/query/config.ts`
4. `../../codigo_principal/claude_code_src/query/tokenBudget.ts`
5. `../../codigo_principal/claude_code_src/query/stopHooks.ts`

## Se voce quer entender como as ferramentas rodam

Abra nesta ordem:

1. `../../codigo_principal/claude_code_src/Tool.ts`
2. `../../codigo_principal/claude_code_src/tools.ts`
3. `../../codigo_principal/claude_code_src/services/tools/toolOrchestration.ts`
4. `../../codigo_principal/claude_code_src/services/tools/toolExecution.ts`
5. `../../codigo_principal/claude_code_src/services/tools/StreamingToolExecutor.ts`

## Se voce quer entender permissoes

Abra nesta ordem:

1. `../../codigo_principal/claude_code_src/Tool.ts`
2. `../../codigo_principal/claude_code_src/state/AppStateStore.ts`
3. `../../codigo_principal/claude_code_src/utils/permissions/`
4. `../../codigo_principal/claude_code_src/components/permissions/`

## Se voce quer entender a UI do terminal

Abra nesta ordem:

1. `../../codigo_principal/claude_code_src/screens/REPL.tsx`
2. `../../codigo_principal/claude_code_src/components/PromptInput/`
3. `../../codigo_principal/claude_code_src/components/messages/`
4. `../../codigo_principal/claude_code_src/hooks/`
5. `../../codigo_principal/claude_code_src/ink/`

## Se voce quer entender MCP e extensoes

Abra nesta ordem:

1. `../../codigo_principal/claude_code_src/services/mcp/`
2. `../../codigo_principal/claude_code_src/commands/mcp/`
3. `../../codigo_principal/claude_code_src/tools/ListMcpResourcesTool/`
4. `../../codigo_principal/claude_code_src/tools/ReadMcpResourceTool/`
5. `../../codigo_principal/claude_code_src/components/mcp/`

## Se voce quer entender agentes, plugins e skills

Abra nesta ordem:

1. `../../codigo_principal/claude_code_src/tools/AgentTool/loadAgentsDir.ts`
2. `../../codigo_principal/claude_code_src/tools/AgentTool/`
3. `../../codigo_principal/claude_code_src/skills/`
4. `../../codigo_principal/claude_code_src/plugins/`
5. `../../codigo_principal/claude_code_src/utils/plugins/`
6. `../../codigo_principal/claude_code_src/commands/plugin/`

## Se voce quer entender persistencia e retomada

Abra nesta ordem:

1. `../../codigo_principal/claude_code_src/utils/sessionStorage.js`
2. `../../codigo_principal/claude_code_src/utils/conversationRecovery.js`
3. `../../codigo_principal/claude_code_src/utils/sessionRestore.js`
4. `../../codigo_principal/claude_code_src/history.ts`
5. `../../codigo_principal/claude_code_src/utils/fileHistory.js`

## Se voce quer comparar com a base complementar

Abra nesta ordem:

1. `../../referencia_sanbuphy/analise_de_diferencas/resumo_diferencas.txt`
2. `../../referencia_sanbuphy/analise_de_diferencas/relatorio_diferencas_src.csv`
3. `../../referencia_sanbuphy/fonte_original/src/`
4. `../../referencia_sanbuphy/documentacao_traduzida_pt_br/`
