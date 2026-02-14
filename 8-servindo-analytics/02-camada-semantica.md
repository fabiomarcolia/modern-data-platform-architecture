# Camada Semântica como Infraestrutura

Camada semântica é a definição central das regras de negócio que sustentam decisões.

Ela define:
- Métricas oficiais
- Dimensões padronizadas
- Regras de cálculo versionadas
- Convenções e dicionários

Sem camada semântica:
- Cada time calcula “Receita” de um jeito
- Dashboards divergem silenciosamente
- Correções viram “corrida” e nunca terminam

---

## Quando implementar

Implemente quando:
- Times discutem números com frequência
- Métricas variam entre dashboards
- Consumo analítico está crescendo
- Há necessidade de governança no nível lógico

---

## Componentes essenciais

- **Métrica única por definição**
- Versionamento explícito
- Responsável por domínio (ownership)
- Documentação centralizada
- Processo de mudança (aprovado e auditável)

---

## Critérios de avaliação (práticos)

- % de dashboards usando métricas oficiais
- Frequência de “conflito de números” por mês
- Tempo para alterar uma regra de negócio
- Impacto histórico: consegue recalcular com consistência?

---

## 🔜 Próximo

➡️ [BI em Escala](./03-bi-em-escala.md)
