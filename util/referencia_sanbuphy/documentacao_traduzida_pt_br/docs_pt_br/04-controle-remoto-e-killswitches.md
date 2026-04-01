# 04 - Controle Remoto e Killswitches

## Visao geral

A base indica infraestrutura de controle remoto de comportamento por configuracoes gerenciadas e feature flags.

## Mecanismos observados

- polling periodico de configuracoes remotas;
- fallback para cache local quando endpoint remoto falha;
- switches de emergencia para recursos especificos;
- gates para recursos como auto mode, fast mode, voice mode e equipes de agentes.

## Implicacao

Parte das decisoes operacionais pode ser alterada sem interacao explicita do usuario final,
principalmente em contextos enterprise/managed.

## Ponto de governanca

Em ambientes corporativos, politicas remotas podem ser mandatarias e inegociaveis para o usuario.
