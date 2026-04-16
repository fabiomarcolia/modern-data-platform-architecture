# Feature Store ML

Feature Store não é “ferramenta bonita”. É **infraestrutura de consistência**.

Ela resolve um problema central:
**treino e produção usam exatamente a mesma definição de feature**.

![Feature Store](/assets/diagramas/feature-store-fluxo.png)

---

## O que é uma Feature Store

Uma Feature Store é o componente central de uma Modern Data Platform voltado para gerenciar e servir variáveis (features) para modelos de Machine Learning (ML). Ela funciona como um repositório centralizado que garante que os mesmos dados usados para o treinamento de um modelo estejam disponíveis para a predição em tempo real, resolvendo o problema de inconsistência entre ambientes (training-serving skew).

### Principais Pilares em uma Arquitetura Moderna

- Offline Store: Armazena o histórico completo das variáveis para treinamento e backtesting, geralmente sobre tecnologias como Delta Lake ou Data Warehouses na nuvem (Snowflake, BigQuery).

- Online Store: Mantém apenas os valores mais recentes para consultas de baixíssima latência (milissegundos) durante a inferência em produção, utilizando bancos chave-valor.

- Registro de Features: Um catálogo de metadados que permite a descoberta e reutilização de variáveis entre diferentes equipes, evitando o retrabalho de criar a mesma lógica várias vezes.

### Benefícios Estratégicos

- Reutilização: Permite que variáveis complexas, como "total de compras nos últimos 30 dias", sejam calculadas uma única vez e usadas em múltiplos modelos.

- Consistência: Garante que a lógica de transformação dos dados brutos seja idêntica tanto para o treinamento offline quanto para o serviço online.

- Prevenção de Data Leakage: Fornece valores históricos precisos para um momento específico no tempo (point-in-time correctness), evitando que o modelo "veja o futuro" durante o treino. 

### Ferramentas de Mercado
As plataformas modernas oferecem soluções integradas ou agnósticas:

- Plataformas de Nuvem: AWS SageMaker Feature Store e Google Vertex AI.

- Integradas (Lakehouse): Databricks Feature Store (integrada ao Delta Lake e MLflow).

- Especializadas/Open Source: Feast (agnóstica), Tecton e Hopsworks. 

---

### Em resumo uma Feature Store Entrega

1. **Reuso**
   - Features padronizadas para múltiplos modelos
2. **Consistência**
   - Mesma lógica para treino e inferência
3. **Versionamento**
   - Feature muda? Você sabe quando e por quê.
4. **Governança**
   - Feature sensível exige política e auditoria.

---

### Online vs Offline (sem confusão)

- **Offline**: para treino (histórico, snapshots)
- **Online**: para inferência (baixa latência, consistência)

A armadilha:
Offline bem feito e online improvisado → divergência silenciosa.

---

### Quando faz sentido investir

- Mais de 1 time de ML
- Mais de 2 modelos em produção
- Conflitos recorrentes de feature
- Necessidade de auditoria (financeiro/saúde)

---

### Anti-pattern

“Cada modelo cria suas features no próprio pipeline.”

Resultado:
- Retrabalho
- Divergência
- Baixa governança
- Alto risco

---

## 🔜 Próximo

➡️ [ML no Lakehouse](./03-ml-no-lakehouse.md)
