# O que é Observabilidade de Dados

Observabilidade é a capacidade de **entender o estado interno** do sistema a partir de sinais.

Em dados, isso significa responder rápido:

- O que quebrou?
- Onde quebrou?
- Quem foi impactado?
- Como mitigar?
- Como evitar de novo?

![Observabilidade](../diagrams/assets/data-observability-camadas.png)

---

## Observabilidade ≠ Monitoramento

Monitoramento: “o job falhou”.
Observabilidade: “o job falhou + impacto + causa provável + ação recomendada”.

---

## Os 3 sinais clássicos (adaptados)

- **Métricas**: volumes, latência, sucesso, custo
- **Logs**: erros e contexto técnico
- **Traces/Lineage**: dependências e impacto

---

## Anti-patterns

- Alertas sem dono
- Métricas sem contexto
- “Corrigir depois” sem postmortem
- Sem lineage → impacto vira adivinhação

---

## 🔜 Próximo

➡️ [SLOs e SLAs](./02-slos-slas.md)
