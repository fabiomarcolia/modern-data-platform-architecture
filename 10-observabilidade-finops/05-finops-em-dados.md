# FinOps em Dados (modelo prático)

FinOps é disciplina para transformar custo em decisão.

Objetivo:
**evitar que consumo e processamento virem caixa-preta financeira.**

![FinOps](../diagrams/assets/finops-dados-alavancas.png)

---

## 3 alavancas principais

### Consulta (Serving/BI/Engines)
- reduzir full scans
- materializar agregações
- cache
- limites por domínio

### Pipelines (processamento)
- reduzir recomputação
- schedule inteligente
- right-sizing

### Storage (lakehouse)
- compaction
- lifecycle policies
- evitar duplicação

---

## Modelo de gestão

1. Visibilidade: custo por domínio/consulta/pipeline
2. Orçamento: limites e alertas
3. Otimização: backlog mensal de economia
4. Políticas: gates para workloads caros
5. Relato executivo: KPIs e tendências

---

## 🔜 Próximo

➡️ [FinOps + Governança](./06-finops-governanca.md)
