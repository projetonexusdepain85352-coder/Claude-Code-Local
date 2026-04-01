# Criterios de Organizacao

## Regra mestra

Tudo o que ajuda a estudar, entender ou comparar o codigo fica em `util/`.
Tudo o que so precisa existir por preservacao historica fica em `inutil/`.

## Criterios usados na reorganizacao

### 1. Funcao antes da origem

As pastas foram nomeadas pela funcao que exercem no acervo, nao apenas pela forma como surgiram.

Exemplos:

- bundles e zips foram agrupados como `fontes_preservadas`;
- material complementar foi concentrado em `referencia_sanbuphy`.

### 2. Uma pasta, uma responsabilidade

Cada diretorio superior deve responder a um unico papel:

- codigo ativo;
- referencia externa;
- artefato bruto;
- documentacao;
- arquivo morto.

### 3. Preservacao sem poluicao

O repositorio manteve documentos antigos e material historico, mas estes foram deslocados para areas em que nao atrapalham a leitura principal.

### 4. Documentacao autoral separada da documentacao preservada

O acervo agora diferencia claramente:

- documentacao propria do repositorio reorganizado;
- documentacao traduzida do material complementar;
- documentacao original preservada do repositorio complementar.

### 5. Navegacao por intencao

Quem abre o repositorio pela primeira vez deve conseguir escolher rapidamente:

- onde esta o codigo principal;
- onde esta a documentacao principal;
- onde esta a referencia complementar;
- onde esta o material inutil para o fluxo diario.

## O que nao foi feito

- nenhum arquivo foi apagado;
- nenhum conteudo historico foi descartado;
- nenhuma raiz falsa de build foi criada na pasta principal para mascarar a natureza de acervo tecnico.

## Consequencia pratica

Com essa organizacao, a pergunta "onde eu olho para X?" passa a ter resposta curta:

- runtime principal -> `../../codigo_principal/claude_code_src/`
- docs do repositorio -> `../`
- contexto complementar -> `../../referencia_sanbuphy/`
- historico morto -> `../../../inutil/`
