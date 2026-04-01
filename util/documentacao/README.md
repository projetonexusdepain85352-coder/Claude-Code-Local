# Documentacao Tecnica do Repositorio

Esta pasta concentra a documentacao propria do acervo. Ela substitui a antiga abordagem de poucos arquivos-resumo por uma camada documental pensada para navegacao, manutencao e estudo profundo do codigo.

## Ordem recomendada de leitura

1. `repositorio/01-visao-geral.md`
2. `repositorio/02-mapa-da-arvore.md`
3. `codigo/01-arquitetura-geral.md`
4. `codigo/02-fluxo-de-execucao.md`
5. `codigo/03-subsistemas.md`
6. `codigo/04-ferramentas-permissoes-e-tarefas.md`
7. `codigo/05-extensibilidade.md`
8. `codigo/06-mapa-de-modulos.md`
9. `codigo/07-leitura-orientada-por-objetivo.md`

## O que cada bloco documenta

### `repositorio/`

Documenta a organizacao fisica do acervo:

- qual pasta existe por qual motivo;
- o que e base principal, referencia preservada e arquivo morto;
- quais foram os criterios de reorganizacao.

### `codigo/`

Documenta o runtime em profundidade:

- entrada e bootstrap;
- fluxo de execucao interativo e headless;
- loop de query e execucao de ferramentas;
- API, estado, persistencia, UI;
- agentes, plugins, skills e MCP;
- mapa de modulos para leitura direta do codigo.

### `legado/`

Guarda documentos antigos movidos para preservacao historica. Eles nao foram apagados; apenas deixaram de ser o ponto de entrada principal.

## Ponto de partida do codigo

Para estudo tecnico do runtime, abra:

- `../codigo_principal/claude_code_src/main.tsx`
- `../codigo_principal/claude_code_src/entrypoints/cli.tsx`
- `../codigo_principal/claude_code_src/QueryEngine.ts`
- `../codigo_principal/claude_code_src/query.ts`
- `../codigo_principal/claude_code_src/tools.ts`
- `../codigo_principal/claude_code_src/state/AppStateStore.ts`

## Referencias complementares

Quando a documentacao mencionar comportamento de build, empacotamento ou contexto original, consulte:

- `../referencia_sanbuphy/fonte_original/package.json`
- `../referencia_sanbuphy/fonte_original/README.md`
- `../referencia_sanbuphy/fonte_original/QUICKSTART.md`
- `../referencia_sanbuphy/analise_de_diferencas/resumo_diferencas.txt`
