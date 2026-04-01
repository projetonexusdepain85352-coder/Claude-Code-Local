# DOCUMENTACAO UNIFICADA (PT-BR)

## 1. Contexto

Este repositorio foi reorganizado para unificar:

1. a base local principal de codigo extraido;
2. a base complementar do repositorio sanbuphy.

A unificacao foi feita dentro do mesmo projeto `Claude Code Local`, sem manter o sanbuphy como projeto operacional separado.

## 2. Decisao de arquitetura

- Fonte principal ativa: `util/codigo_fonte_extraido/claude_code_src/`
- Complementos preservados: `util/complementos_sanbuphy/repositorio_original/`
- Traducoes PT-BR: `util/complementos_sanbuphy/traducao_pt_br/`
- Comparativo tecnico: `util/complementos_sanbuphy/analise_diferencas/`

## 3. O que foi preservado do sanbuphy

- `docs/` completo (EN/JA/KO/ZH)
- `scripts/`
- `stubs/`
- `tools/` (extras de build/gates)
- `types/` e `utils/` complementares
- `vendor/`
- `README*.md`, `QUICKSTART.md`, `package.json`, `package-lock.json`, `tsconfig.json`, `.gitignore`

## 4. O que foi traduzido para PT-BR

- resumo tecnico do README do sanbuphy
- guia rapido de build
- 5 relatorios principais de `docs/en`

Consulte: `util/complementos_sanbuphy/traducao_pt_br/INDICE_TRADUCOES_PT_BR.md`

## 5. Qualidade da fusao

Foi gerado comparativo entre `sanbuphy/src` e a fonte principal local:

- `util/complementos_sanbuphy/analise_diferencas/relatorio_diferencas_src.csv`
- `util/complementos_sanbuphy/analise_diferencas/resumo_diferencas.txt`

## 6. Regra de uso

- Trabalhe na base principal (`codigo_fonte_extraido/claude_code_src`).
- Use `complementos_sanbuphy` como referencia documental/infraestrutural.
- Nao remova originais; acrescente traducoes e notas tecnicas em paralelo.
