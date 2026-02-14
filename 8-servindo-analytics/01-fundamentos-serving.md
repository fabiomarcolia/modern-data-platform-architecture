# Fundamentos de Serving

Serving é a camada responsável por transformar dados estruturados em **consumo confiável**.

Ele garante:
- Performance previsível
- Custo controlado
- Governança aplicada no consumo
- Métricas oficiais consistentes

Sem Serving estruturado:
- Métricas divergem
- Custo explode
- Confiança executiva desaparece
- O BI vira “disputa de números”

---

## Serving ≠ Dashboard

Dashboard é interface.

Serving é o **modelo operacional completo**:
- Modelo curado (camadas e contratos)
- Semântica centralizada (métricas oficiais)
- Engine adequada (consulta, cache, concorrência)
- Política de acesso aplicada (governança)
- Estratégia de custo (FinOps)

---

## Perguntas de liderança (rápidas e decisivas)

- Existe **métrica oficial** para “Receita”, “Margem” e “Churn”?
- Quanto custa “abrir o painel executivo” por mês?
- Quem aprova mudanças na regra de negócio?
- Quem é dono do dataset e do consumo?

---

## Níveis de maturidade (visão geral)

Nível 1 — BI direto em tabela bruta (alto risco)  
Nível 2 — Tabelas curadas centralizadas (melhora)  
Nível 3 — Camada semântica versionada (confiança)  
Nível 4 — Serving operacionalizado (SLO + FinOps + governança)  
Nível 5 — Serving como produto (Data as a Product + ROI)

---

## 🔜 Próximo

➡️ [Camada Semântica](./02-camada-semantica.md)
