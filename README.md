# Claude Code Local (Unificado)

Este repositorio consolida o melhor de duas bases:

- extracao local principal do codigo-fonte;
- material complementar do repositorio `sanbuphy/claude-code-source-code`.

Tudo foi organizado em portugues tecnico, com estrutura unica e rastreavel.

## Objetivo

- manter uma base unica de trabalho (sem projeto paralelo);
- preservar fontes e documentacoes originais;
- disponibilizar traducoes em PT-BR para consulta rapida;
- separar claramente conteudo util e conteudo inutil para desenvolvimento direto.

## Estrutura Atual

```text
.
|-- util/
|   |-- codigo_fonte_extraido/
|   |   `-- claude_code_src/
|   |-- artefatos_originais/
|   |   |-- repositorios_bundle/
|   |   `-- compactados_zip/
|   |-- complementos_sanbuphy/
|   |   |-- repositorio_original/
|   |   |-- traducao_pt_br/
|   |   `-- analise_diferencas/
|   `-- documentacao/
`-- inutil/
    |-- duplicatas_descartadas/
    `-- metadados_arquivamento/
```

## O que foi unificado

### Base principal (util)

- `util/codigo_fonte_extraido/claude_code_src/`
  - fonte principal para estudo, leitura e navegacao de codigo.

### Complementos sanbuphy (util)

- `util/complementos_sanbuphy/repositorio_original/`
  - documentacao original (EN/JA/KO/ZH), scripts, stubs, vendor e arquivos de infraestrutura.
  - nada foi descartado dessa documentacao.

- `util/complementos_sanbuphy/traducao_pt_br/`
  - versoes em portugues dos documentos principais do material complementar.

- `util/complementos_sanbuphy/analise_diferencas/`
  - relatorio de diferencas entre `src/` do sanbuphy e a fonte principal local.

## Documentacao em portugues

Leia primeiro:

- `util/documentacao/DOCUMENTACAO_UNIFICADA_PT_BR.md`
- `util/documentacao/INDICE_UNIFICACAO_PT_BR.md`
- `util/complementos_sanbuphy/traducao_pt_br/INDICE_TRADUCOES_PT_BR.md`

## Convencao aplicada

- nomes em `snake_case`
- termos descritivos em portugues tecnico
- originais preservados, traducoes separadas

## Nota

`inutil/` existe para manter historico e rastreabilidade, mas sem poluir o fluxo principal de desenvolvimento.
