# DuckDB, Polars e o Poder do Single Node

Nem todo processamento precisa ser distribuído.

Ferramentas modernas single-node conseguem:

- Processar dezenas de GB eficientemente
- Rodar análises locais rápidas
- Reduzir custo de infraestrutura
- Simplificar desenvolvimento

---

## Quando usar DuckDB

- Analytics exploratório
- Transformações intermediárias
- Jobs leves
- Processamento local ou serverless

---

## Quando usar Polars

- Transformações vetorizadas rápidas
- Pipelines Python otimizados
- Workloads menores e médios

---

## Trade-off

Single node:
- Simplicidade
- Baixo custo
- Menor complexidade operacional

Distribuído:
- Escala massiva
- Maior resiliência
- Maior complexidade

---

## Anti-pattern

“Já temos Spark, então vamos usar Spark para tudo.”

Ferramenta não deve ditar arquitetura.

---

## 🔜 Próximo

➡️ [Plataformas SQL-First](./sql-first-platforms.md)
