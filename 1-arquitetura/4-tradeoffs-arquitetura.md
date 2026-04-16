# Trade-offs Arquiteturais

Arquitetura é decisão sob restrição.

Quem foge de trade-off vira refém do acaso.

---

## 📐 Diagrama Oficial (BI como infraestrutura crítica)

![BI Corporativo — Arquitetura](/assets/diagramas/bi-corporate.png)

---

## 4 eixos de trade-off (práticos)

### 1. Portabilidade vs Integração
- Portabilidade reduz lock-in
- Integração profunda aumenta produtividade no curto prazo

### 2. Simplicidade vs Flexibilidade
- Simplicidade escala melhor para times menores
- Flexibilidade exige maturidade operacional

### 3. Centralização vs Domínios
- Centralização padroniza
- Domínios aceleram (mas exigem contratos)

### 4. Custo vs Performance
- performance tem custo (compute, storage, engenharia)
- o objetivo é performance “suficiente” para o negócio

---

## Anti-patterns de liderança

- “vamos reescrever tudo” para resolver dívida
- “streaming para tudo” por status
- “cada área faz do seu jeito” sem contratos

---

## Perguntas que líderes deveriam fazer

- Qual a consequência de um reprocessamento mal feito?
- Quem paga o custo desta decisão?
- Quem é dono do dado e do pipeline?
- Como voltamos atrás se der errado?

---

## 🔜 Próximo Capítulo

- [2-Ingestão](../2-ingestao)
