# Checklist DataOps (30/60/90)

## 0–30 dias
- PR template + CODEOWNERS
- lint/testes unitários no CI
- ambientes definidos (mesmo que simples)
- secrets fora do repo

## 31–60 dias
- gates de qualidade de dados em STG
- contratos de dados para datasets críticos
- rollback definido e testado
- releases com tags

## 61–90 dias
- promoção automatizada com aprovação
- observabilidade ligada a deploy
- FinOps por domínio/pipeline
- postmortem recorrente e melhoria contínua
