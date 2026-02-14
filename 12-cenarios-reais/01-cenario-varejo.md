# Cenário Varejo Completo

Problema típico:
- Ruptura de estoque
- Previsão inconsistente
- Custo de consulta elevado

Arquitetura:
- Ingestão contínua (CDC + APIs)
- Lakehouse com particionamento por data/loja
- Serving otimizado para BI
- ML para previsão
- RAG para consulta de políticas internas
- Observabilidade + FinOps

Impacto esperado:
- Redução de ruptura
- Menor custo por consulta
- Decisão orientada por dados confiáveis
