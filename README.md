# Claude Code Local

Este repositorio foi reorganizado para funcionar como um acervo tecnico navegavel, com duas fronteiras explicitas:

- `util/`: tudo o que serve para estudo, leitura, comparacao, referencia e trabalho tecnico.
- `inutil/`: tudo o que precisa ser preservado por rastreabilidade, mas nao deve poluir o fluxo principal.

Nenhum arquivo foi apagado na reorganizacao. O trabalho consistiu em mover diretorios para destinos mais intuitivos, preservar material legado e criar documentacao propria em Markdown para explicar profundamente o codigo.

## Estrutura principal

```text
.
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
`-- inutil/
    |-- duplicatas_arquivadas/
    `-- metadados_de_origem/
```

## Como ler este repositorio

1. Comece por `util/documentacao/README.md`.
2. Use `util/codigo_principal/claude_code_src/` como base principal de estudo do runtime.
3. Consulte `util/referencia_sanbuphy/fonte_original/` quando precisar do contexto do repositorio complementar que inclui `package.json`, `tsconfig.json`, `docs/`, `scripts/` e outros artefatos de build.
4. Use `util/referencia_sanbuphy/documentacao_traduzida_pt_br/` para leitura rapida em portugues do material complementar.
5. Ignore `inutil/` no dia a dia, exceto quando precisar rastrear origem, duplicatas ou metadados de arquivamento.

## O que existe em cada area

### `util/codigo_principal/claude_code_src/`

Codigo principal extraido e tratado como fonte ativa para leitura arquitetural, navegacao entre modulos e entendimento do runtime.

### `util/fontes_preservadas/`

Artefatos originais mantidos por integridade historica:

- bundles de repositorios;
- arquivos compactados;
- material bruto que nao deve ser confundido com a base principal de estudo.

### `util/referencia_sanbuphy/`

Camada de referencia para comparacao com a base complementar:

- `fonte_original/`: espelho do repositorio complementar com `src/`, `docs/`, `scripts/`, `package.json` e `tsconfig.json`;
- `documentacao_traduzida_pt_br/`: traducoes tecnicas existentes;
- `analise_de_diferencas/`: comparativo entre a fonte complementar e a base principal.

### `util/documentacao/`

Documentacao propria deste acervo. Esta e a camada autoral do repositorio:

- explica a organizacao;
- documenta o fluxo do codigo;
- descreve modulos, runtime, ferramentas, estado, extensibilidade e rotas de leitura.

### `inutil/`

Conteudo mantido por rastreabilidade, sem papel operacional:

- duplicatas arquivadas;
- metadados de origem e arquivamento.

## Documentacao principal

- `util/documentacao/README.md`
- `util/documentacao/repositorio/01-visao-geral.md`
- `util/documentacao/codigo/01-arquitetura-geral.md`
- `util/documentacao/codigo/02-fluxo-de-execucao.md`
- `util/documentacao/codigo/06-mapa-de-modulos.md`

## Observacao importante

Este repositorio nao foi convertido em um projeto "pronto para build" na raiz. O `package.json` e os demais arquivos de build continuam preservados em `util/referencia_sanbuphy/fonte_original/`, porque esse material pertence ao repositorio complementar e deve permanecer contextualizado como referencia preservada, nao como a raiz operacional deste acervo.
