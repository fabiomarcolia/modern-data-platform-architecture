# Orquestração Orientada a Eventos

Nem toda orquestração precisa ser baseada em horário.

Event-driven é poderoso… quando justificado.

Esse modelo, ao invés de uma DAG iniciar em determinado horário, ela inicia com base em algum evento que ocorra, que pode ser em qualquer momento.

---

## Quando faz sentido

- Dados chegam de forma imprevisível
- Eventos críticos disparam ações
- Sistemas precisam reagir imediatamente

---

## Quando NÃO faz sentido

- Processamento diário previsível
- Pipeline batch simples
- Time sem maturidade operacional

---

## Riscos do event-driven mal desenhado

- Explosão de dependências
- Debug complexo
- Reprocessamento difícil
- Falta de rastreabilidade

---

## Arquitetura híbrida madura

Batch como base.
Eventos como gatilho específico.

Streaming não substitui disciplina arquitetural.

---

## SLAs vs SLOs

SLA: compromisso externo
SLO: meta interna

Exemplo:
- SLA: relatório disponível até 08:00
- SLO: 99% dos pipelines concluídos até 07:45

Sem SLO, não existe melhoria contínua.

---

## Perguntas de maturidade

- Temos métricas de confiabilidade?
- Sabemos taxa de falha histórica?
- Temos playbook de incidente?
- Pipeline é auditável ponta a ponta?

---

## 🔜 Próximo Capítulo

➡️ [6-Qualidade de Dados](../6-qualidade-de-dados)
