# Claude Code v2.1.88 - Analise de Codigo Fonte (PT-BR)

## Escopo

Este documento resume em portugues o README tecnico do repositorio complementar sanbuphy.

Base analisada:
- pacote npm `@anthropic-ai/claude-code` v2.1.88
- fonte TypeScript extraida do bundle

## Pontos principais

- Estrutura de agente com loop de ferramentas (tool_use -> tool_result).
- Sistema de ferramentas amplo (40+), com permissoes e controles de risco.
- Grande uso de feature flags e eliminacao de codigo em build.
- Diferencas entre comportamento interno (ant) e externo.
- Presenca de modulos ausentes no pacote publicado (gated/dead-code).

## Relatorios aprofundados

Os 5 relatorios principais foram traduzidos para PT-BR em:
`docs_pt_br/`

Eles cobrem:
1. telemetria e privacidade
2. recursos ocultos e codinomes
3. modo undercover
4. controle remoto e killswitches
5. roteiro futuro (roadmap)

## Aviso legal

Todo o codigo original continua pertencendo aos detentores dos direitos.
Este repositorio local e para estudo tecnico, auditoria e organizacao.
