# Arquitetura de ML na Plataforma

ML em produção é um **sistema**. Não um notebook.

A arquitetura madura conecta o ciclo completo:

**Dados Curados → Features → Treino → Registro → Deploy → Monitoramento → Re-treino**

![ML End-to-End](../diagrams/assets/ml-na-plataforma-arquitetura.png)

---

## Por que isso importa

Sem arquitetura integrada, você cria:

- Modelos que “funcionam” no notebook e falham no real
- Drift invisível (dados mudam, modelo degrada)
- Decisões automatizadas sem auditoria
- Custo imprevisível (treino e inferência)

---

## Decisões que diferenciam senioridade

### 1) Separar pipeline de dados e pipeline de ML
- Pipeline de dados: contratos, qualidade, lineage
- Pipeline de ML: features, treino, validação, deploy

A integração existe, mas os objetivos são diferentes.

### 2) Definir “fonte certificada” para features
Feature não nasce em tabela bruta.
Feature nasce em dados curados, com contrato.

### 3) Reprodutibilidade como requisito
Você precisa conseguir responder:

- “Qual dataset e qual versão gerou este modelo?”
- “Quais features e quais parâmetros foram usados?”

---

## Anti-patterns (que viram incidente)

- Treinar em tabela bruta “para ganhar velocidade”
- Feature calculada de um jeito no treino e de outro no serving
- “Atualiza o modelo quando der” (sem SLO e sem monitoramento)
- LLM/RAG acessando dado sensível sem política

---

## Checklist de prontidão (rápido)

- Existe contrato de dados para os datasets usados?
- Existe ownership de features por domínio?
- Existe registro de modelos e versionamento?
- Existe monitoramento de drift?
- Existe custo por modelo/predição visível (FinOps)?

---

## 🔜 Próximo

➡️ [Feature Store](./02-feature-store.md)
