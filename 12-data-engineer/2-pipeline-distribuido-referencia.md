
# Pipeline Distribuído de Referência

Os pipelines distribuídos em uma Modern Data Platform (MDP) são sistemas que permitem o processamento de grandes volumes de dados de forma paralela e escalável em múltiplos nós ou clusters. Diferente dos modelos tradicionais monolíticos, eles se baseiam na nuvem para oferecer elasticidade e eficiência

---
![Pipeline Distribuido](../assets/diagramas/orquestracao.png)
---

### 1. Ingestão e Movimentação de Dados 

A ingestão em plataformas modernas foca na automação e no suporte a múltiplos formatos (estruturados e não estruturados).

- Batch (Lote): Ferramentas como Fivetran e Airbyte automatizam a extração de dados de SaaS e bancos de dados através de conectores prontos.

- Streaming (Tempo Real): Utilizam sistemas de mensageria distribuída como o Apache Kafka e o Confluent para processar fluxos de dados à medida que ocorrem. 

### 2. Processamento e Transformação Distribuída

O coração do pipeline distribuído é a capacidade de dividir tarefas complexas entre várias máquinas simultaneamente. 

- Spark no Databricks: O Databricks utiliza o Apache Spark para processamento em larga escala, permitindo que transformações pesadas sejam executadas em clusters distribuídos de forma transparente para o usuário.

- ELT (Extract, Load, Transform): Em plataformas como Snowflake e Google BigQuery, a transformação ocorre dentro do próprio warehouse distribuído, aproveitando seu poder de processamento paralelo maciço.

### 3. Orquestração de Workflows

Para gerenciar a dependência entre as etapas do pipeline em um ambiente distribuído, utilizam-se orquestradores modernos:

- Apache Airflow: O padrão de mercado para criar DAGs (Directed Acyclic Graphs) que coordenam tarefas complexas.

- Mage: Uma alternativa emergente com foco em experiência de desenvolvedor (DX) e integração nativa com machine learning.

- Prefect e Dagster: Ferramentas que oferecem maior flexibilidade e visibilidade sobre o estado das execuções em tempo real. 

### 4. Armazenamento: Lakehouse

A arquitetura moderna frequentemente adota o modelo Lakehouse, que combina o baixo custo dos Data Lakes (como Amazon S3 ou Azure Data Lake) com a performance e governança dos Data Warehouses. Tecnologias como o Delta Lake garantem transações ACID e integridade dos dados mesmo em pipelines distribuídos altamente concorrentes. 

--- 

## Resumo de Componentes Envolvidos

- Orquestrador (Airflow / Dagster)
- Engine distribuída (Spark / Flink)
- Storage columnar (Iceberg / Delta)
- Engine de consulta (Trino / Athena)
- Monitoramento contínuo

## Vantagens de uma arquitetura moderna

- Escalabilidade Automática: Capacidade de escalar recursos para cima ou para baixo com base no volume de dados, otimizando custos.

- Tempo Real e Batch: Suporte para processamento de fluxo (streaming) e processamento em lote (batch).

- Resiliência e Observabilidade: Monitoramento ativo para detectar falhas precocemente e garantir a confiabilidade dos dados.

- Acessibilidade: Ferramentas de baixo código ou baseadas em notebooks (como Mage ou Databricks) facilitam o desenvolvimento por engenheiros de dados e analistas.

## 🔜 Próximo

➡️ [Maturidade de Engenharia](3-maturidade-engenharia-de-dados.md)

