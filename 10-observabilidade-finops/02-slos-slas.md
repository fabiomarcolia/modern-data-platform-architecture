# SLOs e SLAs para Dados

SLO = objetivo interno de confiabilidade (engenharia).
SLA = compromisso com o consumidor (negócio).

Serving maduro (Cap. 08) pede SLO.
ML/IA (Cap. 09) pede SLO.

---

## Exemplos de SLOs úteis

- Disponibilidade do dataset crítico: 99,5%
- Latência de atualização: até 2h (P95)
- Atraso máximo permitido (freshness): 4h
- Taxa de falhas de pipeline: < 0,5%/dia
- Incidentes críticos: < 2/mês

---

## Definição recomendada

1. Identificar datasets/dashboards críticos
2. Definir consumidores (quem sofre)
3. Definir janela de medição (semana/mês)
4. Definir erro orçamentário (error budget)
5. Criar alerta + playbook

---

## Error Budget (o que impressiona liderança)

Se o error budget estoura:
- congela mudanças não críticas
- prioriza confiabilidade

---

## 🔜 Próximo

➡️ [Incidentes e Playbooks](./03-incidentes-playbooks.md)
