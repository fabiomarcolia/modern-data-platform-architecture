# MLOps Integrado + Observabilidade

MLOps não é “deploy de modelo”. É **operação contínua**.

---

## Ciclo sustentável

Treino → Validação → Deploy → Monitoramento → Feedback → Re-treino

---

## O que monitorar (de verdade)

### 1) Drift de dados
- distribuição mudou?
- missing aumentou?
- cardinalidade mudou?

### 2) Drift de modelo
- performance degradou?
- taxa de erro aumentou?
- thresholds ficaram defasados?

### 3) Saúde operacional
- latência
- disponibilidade
- fila / backlog
- erros por versão

### 4) Impacto e segurança
- decisões anômalas
- outliers críticos
- acesso indevido

---

## SLOs recomendados

- Latência P95 de inferência
- Disponibilidade do endpoint
- Tempo máximo para detectar drift
- Tempo máximo para rollback

---

## 🔜 Próximo

➡️ [FinOps para ML & IA](./07-finops-ml-ia.md)
