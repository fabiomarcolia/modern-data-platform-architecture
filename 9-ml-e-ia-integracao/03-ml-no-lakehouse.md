# ML no Lakehouse (sem hype)

Lakehouse pode ser excelente para ML, mas só quando você entende os trade-offs.

O valor real do lakehouse para ML:

- **Histórico preservado** (time travel)
- **Dados curados + features** no mesmo lugar
- **Redução de cópias** entre ambientes
- **Governança centralizada**

---

## Onde dá errado

- “Treina direto no lake” sem controle de versões
- Feature engineering sem particionamento e sem contrato
- Tabelas com small files e metadata explosiva (impacta ML e BI)
- Time de ML criando “shadow datasets” fora da plataforma

---

## Padrão recomendado

1. Dados curados (contratos + qualidade)
2. Features materializadas (particionadas e versionadas)
3. Dataset de treino por janela (snapshot)
4. Registro do dataset de treino (para auditoria e reprodutibilidade)

---

## Perguntas de arquitetura

- Como garantimos reprodutibilidade do dataset de treino?
- Qual é a estratégia de backfill de features?
- O time consegue sustentar metadata/compaction?
- Existe SLO de disponibilidade de features?

---

## 🔜 Próximo

➡️ [LLMs & RAG Corporativo](./04-llm-e-rag-corporativo.md)
