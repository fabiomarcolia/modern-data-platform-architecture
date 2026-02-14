# FinOps aplicado a Serving

FinOps em Serving significa controlar custo de consumo analítico com disciplina arquitetural.

---

## 1) Visibilidade (o mínimo)

Você precisa saber:
- Custo por dashboard
- Custo por área
- Top consultas mais caras
- Crescimento mensal de consumo

Sem visibilidade, não existe gestão.

---

## 2) Responsabilidade (accountability)

Definir:
- Dono por domínio
- Orçamento por área
- Política de consumo
- Aprovação para workloads pesados

Serving sem accountability vira centro de custo invisível.

---

## 3) Otimização técnica (onde a economia acontece)

- Materializações estratégicas
- Agregações pré-calculadas
- Particionamento eficiente
- Cache bem aplicado
- Controle de full-scan
- Revisão de dashboards “caros” e pouco usados

---

## 4) Governança de consumo (regras claras)

- Limite de concorrência
- Alertas para consultas acima de X custo
- Revisão periódica de acesso + consumo
- Desativação de ativos não utilizados

---

## Indicadores FinOps (práticos)

- Custo por usuário ativo
- Custo por dashboard crítico
- Custo por domínio
- % de queries otimizadas
- % de consumo com “valor claro”

---

## 🔜 Próximo

➡️ [FinOps + Governança](./08-finops-governanca.md)
