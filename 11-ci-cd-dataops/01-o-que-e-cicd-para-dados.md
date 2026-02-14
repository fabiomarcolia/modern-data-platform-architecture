# O que é CI/CD para Dados

CI/CD para dados é a capacidade de entregar mudanças na plataforma com:

- velocidade
- previsibilidade
- rollback
- auditoria
- custo controlado

![CI/CD](../diagrams/assets/cicd-dados-fluxo.png)

---

## CI (Continuous Integration)

Rodar automaticamente no PR:
- lint/format
- testes unitários (código)
- testes de dados (amostra ou staging)
- validações de schema/contratos
- checks de segurança

## CD (Continuous Delivery/Deployment)

Após aprovação:
- aplicar migração/manifesto em STG
- validar impacto
- promover para PROD com gate
- monitorar SLO e custo

---

## Anti-pattern

“Merge direto na main e roda em produção”

Isso não é plataforma.
É risco operacional.
