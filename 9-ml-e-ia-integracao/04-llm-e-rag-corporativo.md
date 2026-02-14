# LLMs & RAG Corporativo (arquitetura, risco e custo)

RAG corporativo é **plataforma**, não prompt.

Uma arquitetura madura responde 3 perguntas:

1. **Que dado o modelo pode ver?** (Governança)
2. **Quanto custa responder?** (FinOps)
3. **Como auditar o que aconteceu?** (Risco/Compliance)

![RAG](../diagrams/assets/rag-governanca-finops.png)

---

## Fluxo arquitetural recomendado

1. Curadoria e classificação das fontes
2. Indexação vetorial com versionamento
3. Recuperação com filtros de permissão (policy)
4. Prompt assembly controlado
5. Observabilidade: qualidade, latência, custo, auditoria

---

## Riscos que líderes precisam entender

- **Vazamento**: o modelo “vê” o que não deveria
- **Alucinação**: resposta convincente e errada
- **Custo**: crescimento de uso sem orçamento
- **Shadow AI**: times criando RAG fora da governança

---

## Boas práticas que impressionam (porque quase ninguém faz)

- Versionar embeddings e índices
- Logar prompts/recuperação (com redaction quando necessário)
- Medir taxa de “resposta sem evidência”
- Controlar custo por área/assistente (FinOps)
- Aplicar RLS/CLS também no contexto recuperado

---

## 🔜 Próximo

➡️ [Governança em IA](./05-governanca-em-ia.md)
