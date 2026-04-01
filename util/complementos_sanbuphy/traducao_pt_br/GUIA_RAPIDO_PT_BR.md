# Guia Rapido de Build (PT-BR)

## Resumo

- Rebuild completo depende de Bun por causa de intrinsics de compilacao (`feature()`, `MACRO`, `bun:bundle`).
- Build com esbuild pode chegar perto, mas exige stubs e ajustes manuais.

## Opcao A - Usar CLI pre-compilado (recomendado)

1. Entre na pasta com `cli.js` e `package.json`.
2. Execute:
   - `node cli.js --version`
   - `node cli.js -p "Hello Claude"`
3. Se quiser, instale globalmente com npm.

## Opcao B - Build best-effort com esbuild

1. Instale dependencia de build (`esbuild`).
2. Rode script de build.
3. Execute `node dist/cli.js --version`.

## Limites conhecidos

- `feature()` e `MACRO` sao resolvidos em compile-time no Bun.
- Existem modulos internos ausentes no artefato publicado.
- Algumas partes precisam de stubs adicionais.

## Opcao C - Build com Bun (contexto interno)

Sem a configuracao interna completa, nao replica 100% do build oficial.
