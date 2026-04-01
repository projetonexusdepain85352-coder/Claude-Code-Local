# 01 - Telemetria e Privacidade

## Visao geral

A analise de codigo indica um pipeline de telemetria em duas camadas:

- logging first-party para endpoint da Anthropic;
- logging third-party (Datadog) para eventos pre-aprovados.

Nao ha evidencia direta de keylogger ou exfiltracao ampla de codigo, mas o volume de metadados coletados e relevante.

## O que e coletado

- fingerprint de ambiente (plataforma, runtime, terminal, CI, kernel, etc);
- metricas de processo (uso de CPU/memoria, uptime);
- identificadores de sessao/usuario/dispositivo;
- dados de assinaturas e organizacao;
- hash do remote de repositorio para correlacao.

## Ponto sensivel

Para uso direto com API da Anthropic, o desativamento completo de logging first-party nao aparece como opcao clara de UI.

## Riscos práticos

1. alto volume de eventos por sessao;
2. persistencia de tentativas em disco quando falha envio;
3. correlacao de ambiente e sessao;
4. possibilidade de log detalhado de entradas de ferramentas em cenarios especificos.
