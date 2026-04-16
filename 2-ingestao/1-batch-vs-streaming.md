# Batch vs Streaming

A pergunta correta não é:
“Devemos usar streaming?”

A pergunta correta é:
“Existe impacto de negócio que justifique streaming?”

---

## 📐 Diagrama — Batch como fundação

![Batch Analytics — Arquitetura](/assets/diagramas/batch-analytics.png)

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

![Streaming — Arquitetura](/assets/diagramas/streaming-architecture.png)

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

➡️ [Padrões de CDC](2-padroes-cdc.md)
