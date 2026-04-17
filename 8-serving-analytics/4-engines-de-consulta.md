# Engines de Consulta: o que são, como avaliar e decidir

Uma engine de consulta é o motor que executa SQL (ou equivalente) sobre seus dados.
Ela define:

- Performance percebida pelo usuário
- Custo por consulta / por dashboard
- Limites de concorrência
- Governança no acesso (políticas + auditoria)
- Modelo operacional (serverless, cluster, híbrido)

Serving não é BI.
Serving é BI + engine + semântica + governança + custo.

---

## Tipos de engine (com exemplos)

### 1) Engine distribuída (SQL federado / lakehouse)
**Trino/Presto**
- O que é: engine distribuída, ótima para múltiplas fontes e grande volume.
- Quando faz sentido: consumo diverso, multi-times, necessidade de padronizar acesso SQL.
- Atenção: exige maturidade operacional (tuning, catálogo, observabilidade).

### 2) Serverless por consulta (pay-per-query)
**Athena**
- O que é: engine serverless para consultar dados em object storage (ex.: S3), pagando por volume processado.
- Quando faz sentido: workloads intermitentes, exploração e BI com controle.
- Atenção: sem governança de queries, custo explode com facilidade.

### 3) MPP gerenciado (warehouse/analytics engine)
**BigQuery**
- O que é: engine MPP gerenciada, com foco em SQL em escala e pouca operação.
- Quando faz sentido: alta demanda analítica, time enxuto, necessidade de agilidade.
- Atenção: custo pode subir com queries mal desenhadas e falta de disciplina de modelagem.

### 4) Data warehouse corporativo com recursos avançados
**Snowflake**
- O que é: DW com separação de compute e storage, elasticidade e governança forte.
- Quando faz sentido: ambientes corporativos multi-time, isolamento, performance previsível e auditoria.
- Atenção: elasticidade sem FinOps vira custo recorrente alto.

---

## Como decidir (checklist prático)

### A) Modelo de custo
- Pagamos por dados escaneados (Athena/BigQuery em certos modos)?
- Pagamos por cluster ligado (Trino self/managed)?
- Pagamos por compute elástico (Snowflake)?
↳ Pergunta executiva: “Sabemos custo por área e por dashboard?”

### B) Concorrência e experiência
- Quantos usuários simultâneos?
- Pico em horários específicos?
- Precisa de cache/materialização?
↳ “O que acontece quando 200 pessoas abrem o painel às 9h?”

### C) Governança e auditoria
- Controle de acesso nativo?
- Auditoria estruturada?
- Integração com catálogo/linhagem?
↳ “Conseguimos provar quem acessou o quê e quando?”

### D) Operação e maturidade do time
- Time sustenta tuning/cluster?
- Existe observabilidade e SLO?
- Existe playbook de incidentes?
↳ “Se falhar, quem resolve e em quanto tempo?”

---

## Anti-patterns (os que mais custam caro)

- “Usuário pode escrever qualquer query”
- BI lendo direto de tabelas brutas
- Sem política de materialização/cache
- Sem limites de consumo por área (FinOps inexistente)

---

## 🔜 Próximo

➡️ [Matriz Comparativa (inclui Power BI)](5-matriz-engines-powerbi.md)
