# Batch vs Streaming

A pergunta correta não é:
“Devemos usar streaming?”

A pergunta correta é:
“Existe impacto de negócio que justifique streaming?”

---

## 📐 Diagrama — Batch como fundação

![Batch Analytics — Arquitetura](../diagrams/assets/batch-analytics.png)

---

## Batch (padrão seguro)

Use Batch quando:
- SLA é diário ou horário
- Volume é previsível
- Reprocessamento é crítico
- Complexidade precisa ser controlada

Vantagens:
- Simplicidade operacional
- Reprocessamento mais seguro
- Menor custo cognitivo

---

## 📐 Diagrama — Streaming consciente

![Streaming — Arquitetura](../diagrams/assets/streaming-architecture.png)

---

## Streaming (quando realmente necessário)

Use Streaming quando:
- Decisão precisa ser em tempo real
- Eventos críticos impactam receita
- Latência é diferencial competitivo

Cuidado:
- Debug é mais complexo
- Reprocessamento exige estratégia
- Observabilidade precisa ser madura

---

## Anti-pattern

“Vamos fazer tudo em streaming porque é moderno.”

Streaming sem necessidade é dívida técnica acelerada.

---

## 🔜 Próximo

➡️ [Padrões de CDC](./padroes-cdc.md)
