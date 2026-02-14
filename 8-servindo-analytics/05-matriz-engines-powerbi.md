# Matriz Comparativa: Engines + Power BI

A matriz abaixo ajuda a explicar decisões de forma executiva e técnica.

| Critério | Trino/Presto | Athena | BigQuery | Snowflake | Power BI (VertiPaq / Import) |
|---|---|---|---|---|---|
| Modelo | SQL distribuído federado | Serverless por query | MPP gerenciado | DW elástico | Engine analítica in-memory |
| Custo | Cluster/provisionamento | Por dados escaneados | Por dados/compute | Compute elástico | Capacidade/licença + modelo |
| Melhor cenário | Multi-fonte/lakehouse | Intermitente/exploração | Analytics em escala | Corporativo/isolamento | Consumo modelado e rápido |
| Concorrência | Alta (com tuning) | Alta (serverless) | Muito alta | Muito alta | Limitada à capacidade |
| Governança | Depende da impl. | IAM + logs | IAM + auditoria | Forte nativa | Workspace/RLS/Model governance |
| Operação | Alta exigência | Baixa operação | Baixa operação | Média | Baixa (com boas práticas) |
| Risco típico | Complexidade | Custo por full-scan | Custo por má modelagem | Custo sem FinOps | Modelos duplicados/Shadow BI |

---

## Nota importante sobre Power BI

Power BI **não substitui** a engine do lakehouse/warehouse.
Ele complementa como camada de consumo, e pode operar em:

- **Import (VertiPaq)**: performance alta e previsível, com governança do modelo.
- **DirectQuery**: “dados na fonte”, mas performance/custo dependem da engine e do design.

---

## 🔜 Próximo

➡️ [Framework de Maturidade](./06-framework-maturidade-serving.md)
