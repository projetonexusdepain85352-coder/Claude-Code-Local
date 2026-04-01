# Visao Geral do Acervo

## Objetivo

Este repositorio nao e apenas um dump de arquivos. Ele foi reorganizado para cumprir quatro objetivos simultaneos:

1. manter uma base principal de leitura do codigo;
2. preservar fontes e artefatos originais;
3. separar material operacional de material apenas historico;
4. documentar o runtime em portugues tecnico, com foco em navegacao profunda.

## O que e a base principal

A base principal do codigo esta em:

- `../../codigo_principal/claude_code_src/`

Esse diretorio concentra o runtime que deve ser lido como fonte ativa do projeto. E nele que ficam os pontos de entrada, o loop principal de query, os registradores de comandos e ferramentas, a interface REPL, o estado global e a maior parte dos modulos de suporte.

## O que e referencia preservada

O acervo complementar esta em:

- `../../referencia_sanbuphy/fonte_original/`

Essa area nao e a raiz operacional do repositorio reorganizado. Ela preserva o contexto do repositorio complementar, incluindo:

- `package.json`
- `package-lock.json`
- `tsconfig.json`
- `README*.md`
- `QUICKSTART.md`
- `docs/`
- `scripts/`
- `src/`
- `stubs/`
- `tools/`
- `types/`
- `utils/`
- `vendor/`

Na pratica, ela funciona como uma referencia documental e comparativa para:

- validar nomes e comportamento de modulos;
- entender o contexto de build;
- consultar documentacao original;
- comparar a arvore `src/` com a base principal.

## O que e historico inutil para fluxo diario

O diretorio `../../../inutil/` preserva tudo o que foi mantido por rastreabilidade, mas que nao deve ser o ponto de entrada para leitura tecnica:

- duplicatas arquivadas;
- metadados de arquivamento e origem.

Essa camada existe para auditoria e cadeia de custodia do material, nao para desenvolvimento ou estudo do runtime.

## Resultado da comparacao com a base complementar

O comparativo preservado em `../../referencia_sanbuphy/analise_de_diferencas/` registra:

- total de arquivos em `sanbuphy/src`: `1902`;
- total de registros de diferenca: `1902`;
- `1384` arquivos com `conteudo_diferente`;
- `518` arquivos `faltando_no_local`.

Essa informacao e importante porque mostra que o acervo principal e a base complementar nao sao equivalentes. Por isso a reorganizacao separa explicitamente:

- `codigo_principal`: leitura preferencial;
- `referencia_sanbuphy`: apoio contextual e comparativo.

## Leitura recomendada

Se o objetivo for entender "o que este repositorio e", abra nesta ordem:

1. `02-mapa-da-arvore.md`
2. `03-criterios-de-organizacao.md`
3. `../codigo/01-arquitetura-geral.md`
