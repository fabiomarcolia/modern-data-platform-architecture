# Feature Store (de verdade)

Feature Store não é “ferramenta bonita”. É **infraestrutura de consistência**.

Ela resolve um problema central:
**treino e produção usam exatamente a mesma definição de feature**.

![Feature Store](../diagrams/assets/feature-store-fluxo.png)

---

## O que uma Feature Store entrega

1. **Reuso**
   - Features padronizadas para múltiplos modelos
2. **Consistência**
   - Mesma lógica para treino e inferência
3. **Versionamento**
   - Feature muda? Você sabe quando e por quê.
4. **Governança**
   - Feature sensível exige política e auditoria.

---

## Online vs Offline (sem confusão)

- **Offline**: para treino (histórico, snapshots)
- **Online**: para inferência (baixa latência, consistência)

A armadilha:
Offline bem feito e online improvisado → divergência silenciosa.

---

## Quando faz sentido investir

- Mais de 1 time de ML
- Mais de 2 modelos em produção
- Conflitos recorrentes de feature
- Necessidade de auditoria (financeiro/saúde)

---

## Anti-pattern

“Cada modelo cria suas features no próprio pipeline.”

Resultado:
- Retrabalho
- Divergência
- Baixa governança
- Alto risco

---

## 🔜 Próximo

➡️ [ML no Lakehouse](./03-ml-no-lakehouse.md)
