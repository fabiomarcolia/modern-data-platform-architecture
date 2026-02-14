# Estudo de Caso — Financeiro

## Contexto
Instituição financeira com exigências regulatórias e auditoria frequente.
Indicadores de risco divergiam e o processo de auditoria era manual.

## Sintomas
- Divergência de métricas de risco
- Acesso inconsistentes a dados sensíveis
- Auditoria lenta e com baixa rastreabilidade
- Alto risco reputacional/regulatório

## Decisões estruturais
1. Classificar datasets (interno/sensível/regulado)
2. Aplicar RLS/CLS na camada de dados (não apenas no BI)
3. Camada semântica versionada (mudanças auditáveis)
4. Auditoria estruturada por engine + BI
5. FinOps integrado: custo por domínio e por dados regulados

## Resultado (exemplo)
- Auditoria automatizada e rastreável
- Redução de incidentes de acesso indevido
- Métricas de risco unificadas
- Sustentabilidade financeira do consumo analítico

## Lição
Em finanças, serving é também “controle de risco”. Performance vem depois.
