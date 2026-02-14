# Gates: Testes, Contratos e Qualidade

Gate é o que impede um PR de virar incidente.

---

## Tipos de gate (práticos)

### 1) Qualidade do código
- lint + format
- testes unitários

### 2) Qualidade dos dados
- checks de volume (anomalias)
- checks de null/unique/range
- freshness

### 3) Contratos de dados
- schema esperado
- colunas obrigatórias
- tipos e invariantes

### 4) Segurança e compliance
- secrets nunca no repo
- scanning de vulnerabilidade
- acesso mínimo

---

## O ponto “senior”

Não é sobre ferramenta.
É sobre **política** e **responsabilidade**.

---

## 🔜 Próximo

➡️ [Deploy e Rollback](./05-deploy-e-rollback.md)
