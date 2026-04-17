# O que é CI/CD para Dados

CI/CD para Dados (muitas vezes inserido no contexto de DataOps) é a aplicação de práticas de engenharia de software — Integração Contínua e Entrega Contínua — ao ciclo de vida dos dados.

É a capacidade de entregar mudanças na plataforma com:

- velocidade
- previsibilidade
- rollback
- auditoria
- custo controlado

Sendo a automação dos processos de desenvolvimento, teste e implantação de pipelines de dados, modelos de machine learning e consultas SQL. Ele utiliza ferramentas como Git, Airflow e DBT para garantir que as mudanças no código de dados sejam integradas e lançadas em produção de forma contínua, confiável e com qualidade.

![CI/CD](/assets/diagramas/cicd-dados-fluxo.png)

Diferente do software tradicional, onde o foco é apenas o código, em dados o CI/CD precisa garantir a integridade do código (SQL, Python), da infraestrutura (pipelines) e da qualidade dos próprios dados.
---

### CI (Continuous Integration)


    - CI (Integração Contínua): Integra alterações de código de dados automaticamente várias vezes ao dia, executando testes de unidade para validar a lógica antes da fusão.

Rodar automaticamente no PR:
- lint/format
- testes unitários (código)
- testes de dados (amostra ou staging)
- validações de schema/contratos
- checks de segurança


### CD (Continuous Delivery/Deployment)

Após aprovação:
- aplicar migração/manifesto em STG
- validar impacto
- promover para PROD com gate
- monitorar SLO e custo

---

## Como funciona na prática:

- CI (Integração Contínua): Toda vez que um engenheiro de dados altera uma transformação (como um modelo no dbt Labs), um processo automatizado é disparado. Ele realiza:

    - Linting: Checa se o código segue padrões.

    - Testes de Unidade: Valida a lógica das transformações.

    - Testes de Qualidade de Dados: Garante que a alteração não vai gerar valores nulos ou duplicados em colunas críticas.

- CD (Entrega/Implantação Contínua): Se os testes passarem, as mudanças são automaticamente (ou após aprovação) aplicadas ao ambiente de produção. Isso pode significar:

    - Atualizar tabelas no Snowflake ou BigQuery.

    - Publicar novas versões de pipelines no Azure Data Factory ou Apache Airflow. 

### Principais Ferramentas

As equipes de dados utilizam plataformas de automação como GitHub Actions, GitLab CI/CD ou Azure Pipelines para orquestrar essas etapas. 


## Anti-pattern

“Merge direto na main e roda em produção”

- Isso não é plataforma.
- É risco operacional.

## 🔜 Próximo

➡️ [Branchin e PRs](2-branching-e-prs.md)