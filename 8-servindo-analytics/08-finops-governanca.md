# Integração Executiva: FinOps + Governança (Cap. 07)

FinOps controla custo.
Governança controla risco.
Serving executa consumo.

Quando não estão integrados:
- Custo explode silenciosamente
- Acesso é descontrolado
- Auditoria vira retrabalho
- Responsabilidade se dilui

---

## Modelo integrado (simples e acionável)

Política de Acesso (Governança)  
→ Limite de Consumo (FinOps)  
→ Execução na Engine (Serving)  
→ Auditoria + KPIs Executivos

---

## Controles recomendados

1. Orçamento por domínio + classificação de sensibilidade  
2. Limite de concorrência por área (ou por workspace)  
3. Alertas para consultas acima de X custo (por engine)  
4. Revisão trimestral de acesso + consumo (governança + finanças)  
5. KPI mensal de “custo por valor” (dashboards críticos)

---

## Indicadores executivos integrados

- Custo por domínio com classificação (interno/sensível/regulado)
- Custo de dados regulados vs não regulados
- Incidentes de acesso + impacto financeiro
- ROI analítico por área (quando possível)

---

## Perguntas que um CDO deveria exigir resposta

- Estamos consumindo dado de forma sustentável?
- Quem é responsável pelo custo por área?
- Existe risco regulatório associado ao consumo?
- Estamos extraindo valor proporcional ao investimento?

---

## 🔜 Próximo

➡️ [Estudo de caso — Varejo](./09-caso-varejo.md)
