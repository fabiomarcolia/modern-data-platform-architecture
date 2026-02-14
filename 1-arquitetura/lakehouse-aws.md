# Lakehouse na AWS

AWS costuma ser escolhida quando a empresa quer:
- flexibilidade de engine
- forte governança
- arquitetura modular

Mas essa flexibilidade cobra preço:
↳ mais decisões, mais operação.

---

## 📐 Diagrama Oficial (Batch como fundação)

![Batch Analytics — Arquitetura](../diagrams/assets/batch-analytics.png)

---

## Componentes típicos (exemplo, não receita)

- **S3**: storage base (camadas Raw/Curado/Serving)
- **Tabelas Iceberg**: versionamento e evolução de schema
- **Catálogo**: Glue Data Catalog (metadados)
- **Query**: Athena/Trino para consumo
- **Governança**: Lake Formation + IAM
- **Orquestração**: Airflow/Step Functions (depende do contexto)

---

## Decisões que evitam dor

### Small files (o inimigo silencioso)
Sinais:
- consultas ficam lentas sem motivo aparente
- custo sobe com varreduras excessivas
- metadados explodem

Mitigação:
- política de compactação
- particionamento consciente
- evitar escrita “micro-batch” descontrolada

---

### Particionamento (onde o custo mora)
Anti-pattern:
- particionar por colunas de alta cardinalidade
- particionar por “tudo”

Regra prática:
- particione por campos usados em filtros frequentes
- pense em leitura, não em escrita

---

## Quando AWS Lakehouse é a escolha certa

- muitos consumidores diferentes (multi-times)
- necessidade forte de governança e auditoria
- ecossistema heterogêneo (várias engines)
- preocupação real com lock-in

---

## 🔜 Próximo tópico

➡️ Continue para: [Plataforma Moderna na GCP](./plataforma-moderna-gcp.md)
