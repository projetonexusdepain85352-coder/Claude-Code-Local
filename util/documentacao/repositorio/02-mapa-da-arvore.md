# Mapa da Arvore do Repositorio

## Estrutura consolidada

```text
.
|-- README.md
|-- util/
|   |-- codigo_principal/
|   |   `-- claude_code_src/
|   |-- fontes_preservadas/
|   |   |-- compactados_zip/
|   |   `-- repositorios_bundle/
|   |-- referencia_sanbuphy/
|   |   |-- fonte_original/
|   |   |-- documentacao_traduzida_pt_br/
|   |   `-- analise_de_diferencas/
|   `-- documentacao/
|       |-- README.md
|       |-- repositorio/
|       |-- codigo/
|       `-- legado/
`-- inutil/
    |-- duplicatas_arquivadas/
    `-- metadados_de_origem/
```

## Interpretacao por responsabilidade

### Raiz

- `README.md`: porta de entrada do acervo.

### `util/codigo_principal/`

- contem a fonte principal para leitura do runtime;
- nao mistura documentos traduzidos, bundles e metadados;
- deve ser a primeira parada para estudo do codigo.

### `util/fontes_preservadas/`

- guarda artefatos brutos;
- separa material empacotado do codigo principal;
- impede que bundles e arquivos compactados sejam confundidos com modulos ativos.

### `util/referencia_sanbuphy/`

- agrupa tudo que pertence ao contexto complementar;
- evita que `repositorio_original/`, traducoes e analises fiquem espalhados;
- cria um polo unico para referencia externa.

### `util/documentacao/`

- concentra toda a camada autoral da documentacao;
- organiza leitura do repositorio e do codigo em trilhas claras;
- preserva o legado em pasta separada.

### `inutil/`

- isola o que precisa permanecer, mas nao deve ser lido como base principal;
- reforca a fronteira entre acervo tecnico e arquivo morto.

## Decisao de nomenclatura

As renomeacoes foram feitas para reduzir ambiguidade:

- `codigo_fonte_extraido` -> `codigo_principal`
- `artefatos_originais` -> `fontes_preservadas`
- `complementos_sanbuphy` -> `referencia_sanbuphy`
- `repositorio_original` -> `fonte_original`
- `traducao_pt_br` -> `documentacao_traduzida_pt_br`
- `analise_diferencas` -> `analise_de_diferencas`
- `duplicatas_descartadas` -> `duplicatas_arquivadas`
- `metadados_arquivamento` -> `metadados_de_origem`

O criterio foi privilegiar nomes que respondam rapidamente a pergunta: "por que essa pasta existe?".
