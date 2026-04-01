# 02 - Recursos Ocultos e Codinomes

## Visao geral

A base revela uso forte de codinomes (principalmente nomes de animais) e varias feature flags com nomes opacos.

## Exemplos citados

- Tengu
- Capybara
- Fennec
- Numbat

## Achados relevantes

- mecanismos de protecao para evitar vazamento de codinomes em canais publicos;
- diferencas de tratamento entre usuario interno (`USER_TYPE === ant`) e externo;
- comandos e ferramentas internas ou parcialmente ocultas por flags;
- patches de prompt especificos para reduzir comportamento indesejado de modelos.

## Impacto

As flags e codinomes dificultam inferencia externa sobre roadmap real e capacidades em rollout.
