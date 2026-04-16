# Expectativas e Monitoramento

Ferramentas ajudam.
Arquitetura sustenta.

A combinação de Expectations (Expectativas) e Monitoramento de Dados é a espinha dorsal da moderna Engenharia de Dados, garantindo que as informações confiáveis alimentem análises e sistemas de IA.

Expectations (estilo Great Expectations) são asserções declarativas — testes automatizados que definem o que você espera dos seus dados (ex: "esta coluna não deve ser nula", "este valor deve estar entre 0 e 100"). O monitoramento é o processo contínuo de rastrear esses dados, aplicando as expectativas para garantir conformidade, qualidade e integridade ao longo do tempo. 

1. O que são Data Expectations?

- As expectativas funcionam como testes unitários para os dados, definindo os padrões de conformidade antes, durante ou depois da carga (ETL/ELT). 

- Conformidade: Verificam se os dados seguem a estrutura esperada (tipos de dados, ausência de valores nulos, formatos válidos).

- Regras de Negócio: Validam regras específicas (ex: "data de fim deve ser posterior à data de início").
Estatísticas: Monitoram distribuições, outliers e desvios nas métricas. 

2. Monitoramento de Dados e Observabilidade

- Diferente do monitoramento tradicional de TI, que foca na infraestrutura (servidor up/down), o monitoramento de dados foca no conteúdo e comportamento. 

- Observabilidade de Dados: É a capacidade de visualizar o estado e o comportamento dos dados, identificando a causa raiz de problemas em pipelines complexos.

- Monitoramento de Qualidade: Utiliza ferramentas para rastrear métricas como completude, precisão, consistência e atualidade. 

3. Ferramentas e Implementação

- Great Expectations (GE): Ferramenta líder para criar, validar e documentar dados automaticamente. Oferece "Data Docs" que transformam expectativas em documentação técnica.

- dbt-expectations: Uma extensão para dbt (data build tool) que permite aplicar testes de qualidade de dados diretamente na camada de transformação.

- Databricks Expectations: Utiliza SQL para aplicar validações de dados diretamente em views e tabelas de streaming.

- Outras ferramentas: Talend (integração), Soda, e plataformas de observabilidade como Monte Carlo e Metaplane. 

4. Melhores Práticas

- Automação na Ingestão: Implementar validações automáticas de dados no momento em que entram no sistema.

- Qualidade baseada em IA: Utilizar machine learning para identificar anomalias que as regras estáticas podem ignorar.

- Governança Ativa: Definir claramente a propriedade dos dados e integrar métricas de qualidade aos KPIs de negócio.

- Detecção de Schema Drift: Monitorar alterações na estrutura dos dados (remoção de colunas, mudança de tipo) que podem quebrar pipelines downstream.

- Data Lineage: Rastrear o fluxo do dado da origem ao destino para impacto analysis. 

---

## Expectations estruturadas

Expectations devem validar:

- Range aceitável
- Percentual de NULL
- Integridade referencial
- Cardinalidade inesperada
- Distribuição fora do padrão

---

## Monitoramento contínuo

Monitorar apenas falha é imaturidade.

Monitorar:

- Tendência de volume
- Drift estatístico
- Anomalias históricas
- Degradação gradual

---

## Data Drift

Drift ocorre quando:

- Perfil estatístico muda
- Distribuição altera silenciosamente
- Modelo de ML degrada

Sem monitoramento de drift,
você descobre o problema tarde demais.

---

## Indicadores estratégicos

- Taxa de falha por domínio
- Tempo médio de resolução
- Frequência de incidentes
- Percentual de pipelines com coverage de qualidade

---

## 🔜 Próximo Capítulo

➡️ [Governança e Segurança](../7-governanca-e-seguranca)
