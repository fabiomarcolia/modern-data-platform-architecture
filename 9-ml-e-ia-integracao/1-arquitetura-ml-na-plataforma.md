# Arquitetura de ML na Plataforma

ML em produção é um **sistema**. Não um notebook.

Uma arquitetura de Machine Learning (ML) integrada a uma Modern Data Platform (MDP) baseia-se na unificação de dados para eliminar silos, permitindo que modelos de IA acessem informações estruturadas e não estruturadas em um único ecossistema. O pilar central dessa arquitetura é frequentemente o Data Lakehouse, que combina a escalabilidade de custo do Data Lake com a governança e performance do Data Warehouse. 

### Componentes Principais da Arquitetura
A estrutura segue geralmente o padrão de Arquitetura Medalhão, organizando o fluxo de dados para consumo por modelos de ML:

- Ingestão e Armazenamento (Bronze): Coleta de dados brutos (logs, APIs, IoT) em formatos abertos no Azure Data Lake Storage ou Amazon S3.

- Processamento e Limpeza (Silver): Transformação e validação dos dados utilizando ferramentas como Databricks, Azure Synapse, ou Spark preparando-os para o treinamento.

- Enriquecimento e Consumo (Gold): Dados agregados e prontos para o negócio, onde modelos de ML realizam inferências ou são alimentados para gerar insights preditivos.

- Camada de ML/AI (MLOps): Integração de ferramentas como Azure Machine Learning ou Amazon SageMaker para o ciclo de vida completo: experimentação, treinamento, catálogo de modelos e implantação. 

### Benefícios da Integração

- 1- Eliminação de Movimentação de Dados: Treinamento e inferência ocorrem diretamente sobre o armazenamento escalável, reduzindo latência e custos.

- 2- Governança Unificada: Uso de ferramentas como Azure Purview para garantir linhagem e segurança dos dados usados pela IA.

- 3- Escalabilidade Nativa: Capacidade de processar grandes volumes de dados para modelos complexos (como LLMs) usando infraestrutura sob demanda.


--- 

A arquitetura madura conecta o ciclo completo:

**Dados Curados → Features → Treino → Registro → Deploy → Monitoramento → Re-treino**

![ML End-to-End](/assets/diagramas/ml-na-plataforma-arquitetura.png)

---

## Por que isso importa

Sem arquitetura integrada, você cria:

- Modelos que “funcionam” no notebook e falham no real
- Drift invisível (dados mudam, modelo degrada)
- Decisões automatizadas sem auditoria
- Custo imprevisível (treino e inferência)

---

## Decisões que diferenciam senioridade

### 1) Separar pipeline de dados e pipeline de ML
- Pipeline de dados: contratos, qualidade, lineage
- Pipeline de ML: features, treino, validação, deploy

A integração existe, mas os objetivos são diferentes.

### 2) Definir “fonte certificada” para features
Feature não nasce em tabela bruta.
Feature nasce em dados curados, com contrato.

### 3) Reprodutibilidade como requisito
Você precisa conseguir responder:

- “Qual dataset e qual versão gerou este modelo?”
- “Quais features e quais parâmetros foram usados?”

---

## Anti-patterns (que viram incidente)

- Treinar em tabela bruta “para ganhar velocidade”
- Feature calculada de um jeito no treino e de outro no serving
- “Atualiza o modelo quando der” (sem SLO e sem monitoramento)
- LLM/RAG acessando dado sensível sem política

---

## Checklist de prontidão (rápido)

- Existe contrato de dados para os datasets usados?
- Existe ownership de features por domínio?
- Existe registro de modelos e versionamento?
- Existe monitoramento de drift?
- Existe custo por modelo/predição visível (FinOps)?

---

## 🔜 Próximo

➡️ [Feature Store](2-feature-store.md)
