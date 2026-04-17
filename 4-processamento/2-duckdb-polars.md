# DuckDB, Polars e o Poder do Single Node

Nem todo processamento precisa ser distribuído, como Spark

Ferramentas modernas single-node conseguem:

- Processar dezenas de GB eficientemente
- Rodar análises locais rápidas
- Reduzir custo de infraestrutura
- Simplificar desenvolvimento

---

### Quando usar DuckDB

- Analytics exploratório
- Transformações intermediárias
- Jobs leves
- Processamento local ou serverless

![DuckDB](../assets/diagramas/duckdb.png)
#### [💡Saiba mais e como começar a usar DuckDB](https://duckdb.org/)
---

### Quando usar Polars

- Transformações vetorizadas rápidas
- Pipelines Python otimizados
- Workloads menores e médios

![Polars](../assets/diagramas/polars.png)
#### [💡Saiba mais e como começar a usar Polars](https://pola.rs/)

---

### DuckDB vs Polars
![alt text](<../assets/diagramas/polar vs duckdb.png>)

-> Nem sempre a decisão é simples

![alt text](<../assets/diagramas/polar vs duckdb2.png>)

💡Analise certinho o cenário e o que precisa realmente ser revolvido.

---

### Polars e DuckDB juntos | Combinam muito bem onde cada um tem de melhor

![Polars e DuckDB Juntos](../assets/diagramas/polas-duckdb-juntos.png)

💡 uma imagem vale mais que 1000 palavras. Essa imagem pode simplificar melhor onde cada um é melhor.

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

➡️ [Plataformas SQL-First](3-sql-first-platforms.md)
