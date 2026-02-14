# Framework de Maturidade de Serving

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
