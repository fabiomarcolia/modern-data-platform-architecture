# Evolução de Schema

A evolução de schema em um Data Lakehouse é a capacidade de alterar a estrutura de uma tabela (como adicionar colunas ou mudar tipos de dados) ao longo do tempo sem a necessidade de reprocessar ou reescrever todos os dados existentes. Ela permite que o sistema se adapte automaticamente a novos requisitos de negócio ou mudanças em fontes de dados externas. 

## Principais Conceitos e Funcionamento

- Schema Enforcement (Imposição): É o mecanismo de segurança que impede a gravação de dados que não seguem o esquema definido, evitando a corrupção do "lake".

- Schema Evolution (Evolução): Permite que mudanças intencionais sejam incorporadas. Quando habilitada, o sistema atualiza os metadados da tabela para incluir as novas colunas ou alterações detectadas durante uma operação de escrita.

- Formatos de Tabela Abertos: Tecnologias como Delta Lake, [Apache Iceberg](https://risingwave.com/glossary/schema-evolution-in-data-lakehouses/) e Apache Hudi são fundamentais para gerenciar essas mudanças de forma transacional (ACID).

## Alterações Suportadas
As ferramentas modernas de Lakehouse, como o Databricks Lakehouse ou o [Microsoft Fabric](https://learn.microsoft.com/pt-br/fabric/data-engineering/lakehouse-schemas), geralmente suportam as seguintes evoluções: [1, 7, 8, 9] 

* Adição de novas colunas: O tipo mais comum e seguro de evolução.
* Mudança de tipos de dados: Frequentemente restrito a mudanças compatíveis (ex: de Integer para Long).
* Renomeação e Exclusão: Suportadas por alguns formatos (como Iceberg), mas podem exigir cautela para não quebrar consultas existentes. [2, 5, 7, 10] 

## Benefícios no Ciclo de Vida de Dados

   1. Agilidade: Permite que equipes de dados adicionem novas métricas rapidamente sem downtime.
   2. Confiabilidade: Evita falhas de pipeline causadas por pequenas mudanças nos dados de origem através de opções como o mergeSchema do Spark.
   3. Governança e Linhagem: Facilita o rastreamento de como os dados mudaram ao longo do tempo, muitas vezes integrada com recursos de "viagem no tempo" (Time Travel). 

## 🔜 Próximo

- [Evolução de Schema](4-evolução-de-schema)

