# Framework de Maturidade de Serving

A maturidade de serving analytics (ou análise de dados em regime de autosserviço/serviço) refere-se ao nível de sofisticação com que uma organização disponibiliza dados, relatórios e insights para os usuários finais, permitindo que líderes e equipes tomem decisões sem depender constantemente da TI ou de cientistas de dados. Essa jornada vai desde relatórios estáticos manuais até análises preditivas automatizadas e integradas.

Este framework serve para diagnóstico e roadmap.

---

## Nível 1 — Exploração (risco alto)
- BI direto em tabela bruta
- Sem governança
- Sem controle de custo
- Métricas inconsistentes

## Nível 2 — Curado (ganho inicial)
- Tabelas curadas centralizadas
- Performance básica
- Métricas parcialmente padronizadas
- Acesso ainda inconsistente

## Nível 3 — Semântico (confiança)
- Camada semântica central
- Métrica oficial única
- Versionamento de regra
- Ownership por domínio

## Nível 4 — Operacionalizado (sustentável)
- Custo monitorado por área
- SLO de performance (dashboards críticos)
- Alertas de queries caras
- Revisão periódica de ativos (dashboards/datasets)

## Nível 5 — Estratégico (produto)
- Data as a Product
- ROI analítico mensurado
- FinOps integrado a governança
- Serving tratado como produto corporativo

---

## Indicadores de avaliação (o que medir)

- % dashboards com métrica oficial
- Custo por usuário ativo
- Custo por dashboard crítico
- Tempo médio de carregamento (P95)
- Incidentes de divergência de métrica
- % de relatórios “ativos” (uso real)

---

## 🔜 Próximo

➡️ [FinOps aplicado a Serving](./07-finops-serving.md)
