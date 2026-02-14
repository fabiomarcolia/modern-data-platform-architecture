# FinOps para ML & IA (custo por predição e por resposta)

FinOps em IA é onde muita empresa “perde o controle” sem perceber.

A regra é simples:
**se você não mede custo por decisão, você não controla custo.**

---

## Onde o custo aparece

### Treinamento
- compute (GPU/CPU)
- armazenamento de datasets
- experimentos repetidos

### Inferência (online/batch)
- custo por chamada
- pico de concorrência
- latência exigida

### RAG/LLM
- custo por token
- custo de embeddings/indexação
- custo de recuperação + geração
- custo de logs e auditoria

---

## Modelo prático de gestão

1. **Visibilidade**
   - custo por modelo
   - custo por endpoint
   - custo por área (centro de custo)
2. **Orçamento**
   - limites por time/produto
3. **Otimização**
   - cache de respostas
   - compressão de contexto
   - top-k e filtros melhores
4. **Políticas**
   - uso permitido vs proibido
   - “gates” para modelos caros

---

## Métricas que impressionam liderança

- Custo por predição
- Custo por 1.000 respostas (RAG)
- Custo por usuário ativo
- % de chamadas com “valor” (ex.: resolução real)
- Custo de auditoria por decisão automatizada

---

## 🔜 Próximo

➡️ [Framework de Maturidade de IA](./08-framework-maturidade-ia.md)
