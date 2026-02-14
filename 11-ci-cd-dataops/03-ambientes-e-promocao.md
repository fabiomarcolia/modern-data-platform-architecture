# Ambientes e Promoção (DEV → STG → PROD)

Sem ambientes, você não tem “plataforma”.
Você tem “deploy direto no cliente”.

![Ambientes](../diagrams/assets/promocao-ambientes.png)

---

## Objetivo de cada ambiente

- **DEV**: experimentar e construir
- **STG**: validar com dados similares ao PROD
- **PROD**: operar com SLO, auditoria e FinOps

---

## O que promove entre ambientes?

- código (pipelines/jobs)
- modelos/manifestos (dbt, DAGs, configs)
- schemas e contratos
- políticas (acesso, classificação)
- documentação (mudanças de regra)

---

## Gate de promoção (o que muda o jogo)

- testes passaram
- contratos passaram
- aprovação de owner
- rollback definido
- janela de deploy (se necessário)

---

## 🔜 Próximo

➡️ [Gates](./04-gates-testes-contratos.md)
