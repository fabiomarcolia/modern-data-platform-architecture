# Padrões de CDC (Change Data Capture)

CDC não é ferramenta.
É estratégia de sincronização confiável.

---

## Quando CDC é necessário

- Sincronizar OLTP com Lakehouse
- Evitar cargas full frequentes
- Manter histórico consistente

---

## Estratégias comuns

1. Log-based CDC  
   - Exemplo: Debezium  
   - Baixo impacto na origem  
   - Alta fidelidade de eventos

2. Trigger-based  
   - Impacta banco origem  
   - Mais simples, menos escalável

3. Timestamp-based  
   - Simples  
   - Pode perder eventos em casos extremos

---

## Decisão que separa senior de executor

Você precisa responder:

- Como reprocessar 6 meses atrás?
- Como lidar com deleções?
- Como tratar duplicidade?
- Como versionar schema com CDC?

---

## Impacto operacional

CDC mal desenhado gera:
- Inconsistência silenciosa
- Problemas de idempotência
- Quebra de downstream

---

## 🔜 Próximo

➡️ [Evolução de Schema](./evolucao-de-schema.md)
