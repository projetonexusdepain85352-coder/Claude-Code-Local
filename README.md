# Claude Code Local (Organizado)

Este repositório é uma organização local de materiais relacionados ao código-fonte extraído do Claude Code, estruturado para facilitar estudo técnico, auditoria e navegação.

## Objetivo

- Centralizar o conteúdo em uma estrutura limpa.
- Separar claramente o que é útil para análise técnica do que é apenas metadado/duplicata.
- Preservar rastreabilidade com documentação e manifestos completos.

## Estrutura do Projeto

```text
.
├── util/
│   ├── codigo_fonte_extraido/
│   │   └── claude_code_src/
│   ├── artefatos_originais/
│   │   ├── repositorios_bundle/
│   │   └── compactados_zip/
│   └── documentacao/
└── inutil/
    ├── duplicatas_descartadas/
    └── metadados_arquivamento/
```

## O que tem em cada pasta

### `util/`
Conteúdo técnico principal.

- `codigo_fonte_extraido/claude_code_src/`: código-fonte extraído (`.ts`, `.tsx`, `.js`).
- `artefatos_originais/repositorios_bundle/`: uma cópia útil de cada `.bundle`.
- `artefatos_originais/compactados_zip/`: `.zip` preservado para referência.
- `documentacao/`: documentação exaustiva, árvores, manifestos CSV e hashes SHA256.

### `inutil/`
Conteúdo preservado, mas não essencial para desenvolvimento direto.

- `duplicatas_descartadas/`: cópias duplicadas de pacotes.
- `metadados_arquivamento/`: arquivos de arquivo/publicação (`.xml`, `.sqlite`, `.torrent`, capas/thumbs).

## Documentação Principal

Leia primeiro:

- `util/documentacao/DOCUMENTACAO_EXAUSTIVA.md`
- `util/documentacao/INDICE_DOCUMENTACAO.md`

Arquivos de apoio importantes:

- `manifesto_completo_util.csv`
- `manifesto_completo_inutil.csv`
- `hashes_artefatos_uteis_sha256.csv`
- `arvore_util_completa.txt`
- `arvore_inutil_completa.txt`

## Padrão de Nomes

- Convenção: `snake_case`
- Idioma: português técnico
- Nomes descritivos por finalidade

## Fluxo de Trabalho (Git)

Exemplo de fluxo para subir alterações:

```bash
git checkout codex/organizacao-estrutura-documentacao
git pull --rebase
git push -u origin codex/organizacao-estrutura-documentacao
```

## Observação

Este repositório foi preparado para estudo e organização técnica. A pasta `util` contém o núcleo de trabalho; `inutil` mantém contexto histórico sem poluir a navegação principal.
