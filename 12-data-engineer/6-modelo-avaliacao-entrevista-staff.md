
# Modelo de Avaliação para Entrevistas (Staff / Principal Data Engineer)

Este modelo serve para:
- Candidato e Contratante
- Avaliar profundidade arquitetural (trade-offs)
- Verificar maturidade operacional (produção, SLO, incident response)
- Medir influência e liderança técnica (alignment e decisões)
- Treinar para entrevista

Um modelo de avaliação para posições de Staff ou Principal Data Engineer deve focar menos na sintaxe de código e mais em visão de arquitetura, impacto de negócio, liderança técnica e capacidade de resolver problemas ambíguos. Nesta senioridade, espera-se que o profissional defina padrões técnicos e influencie equipes inteiras.

---

## 1) Estrutura recomendada de entrevista (60–75 min)

1- **Contexto e escopo (5 min)**  
2- **Design de arquitetura (20–25 min)**  
3- **Operação em produção (15–20 min)**  
4- **FinOps e confiabilidade (10–15 min)**  
5- **Influência e liderança (10 min)**  

---

## 2) Questões “de verdade” (Staff-level)

### Arquitetura & trade-offs
- “Descreva uma arquitetura lakehouse que suporte BI + ML + GenAI. Onde você colocaria governança e por quê?”
- “Quando **não** usar Spark? Cite um caso real e a alternativa.”
- “Flink vs micro-batch: quais requisitos mudam sua decisão?”
- “Como você desenha **schema evolution** sem quebrar consumidores?”

### Produção & confiabilidade
- “Defina SLOs para pipelines e explique como operar error budgets.”
- “Explique como você garante idempotência e replay seguro.”
- “Como você lida com backfills sem derrubar serving/BI?”
- “Qual sua abordagem para incidentes e RCA (post-mortem)?”

### Qualidade & contratos
- “Testes não bastam. Como contratos de dados mudam o jogo?”
- “Como você mede a qualidade como produto (KPIs)?”

### FinOps
- “Como você mede **custo por domínio** e faz chargeback/showback?”
- “Quais otimizações você aplicaria antes de ‘comprar mais compute’?”
- “Como prevenir ‘surpresas’ de custo em engines SQL?”

### Liderança técnica
- “Como você escreve ADRs que reduzem conflitos e aumentam alinhamento?”
- “Como você influencia times sem autoridade formal?”
- “Como decide o que padronizar vs o que permitir autonomia?”

---

## 3) Rubrica de avaliação (0–4)

| Critério | 0 | 1 | 2 | 3 | 4 |
|---|---|---|---|---|---|
| Trade-offs | Não compara | Compara superficial | Compara com exemplos | Decide com dados/risco | Decide e cria padrão |
| Produção | Ignora operação | Logs básicos | Alertas básicos | SLO + incident response | Error budget + melhoria contínua |
| FinOps | Não considera | Cita custo | Mede custos | Custo por domínio | Otimiza e governa custos |
| Governança | Ad-hoc | RBAC básico | Catálogo/linhagem | Contratos e políticas | Governança federada madura |
| Influência | Individual | Ajuda time | Lidera iniciativas | Define padrões | Move a org (multi-times) |

---

## 4) Exercício prático (take-home opcional)

        - Desenhe uma arquitetura que suporte ingestão CDC + lakehouse + serving + BI + observabilidade + FinOps.
        Liste 5 trade-offs e como mitigaria riscos.


---


# Modelo Prático de Avaliação

- Nome do Candidato: ___________________
- Entrevistador: ___________________
- Data: __/__/__

- Pontuação (1-5):

    1. Insuficiente (Abaixo da senioridade)

    2. Abaixo do Esperado (Senior, mas não Staff)

    3. Atende ao Esperado (Staff/Principal)

    4. Acima do Esperado

    5. Excepcional (Referência no mercado)
---


    
- 1- Arquitetura e Design de Sistemas (Peso Alto)
    
    - Foco: Capacidade de projetar sistemas distribuídos escaláveis, resilientes e de alto desempenho.
    
    - Critérios:
        - Sabe escolher entre Data Lakehouse (ex: Delta/Iceberg) vs Data Warehouse.
        - Projeta sistemas para alta volumetria e baixa latência (Streaming vs Batch).
        - Considera custos, segurança (IAM, redes) e conformidade (LGPD) no design.
        - Demonstra domínio de modelagem de dados (Star Schema, Data Vault) para cenários complexos.
    
     Notas/Exemplos: __________ (Pontuação: _ /5) 

---

- 2- Excelência Técnica e Qualidade (Peso Alto)
    - Foco: Engenharia de dados de alta qualidade, automação e otimização.

    - Critérios: 
        - Domínio avançado de SQL (Window Functions, CTEs) e Python/Scala para grandes volumes.
        - Implementa camadas de dados de forma robusta (Bronze, Silver, Gold).
        - Define estratégias de teste de pipeline, linhagem de dados e governança.
        - Resolve desafios de data skew e otimiza partições em frameworks como Spark.
    
    Notas/Exemplos: __________ (Pontuação: _ /5) 

---

- 3-  Liderança Técnica e Influência (Peso Alto)

    - Foco: Capacidade de guiar outros engenheiros, definir padrões e resolver conflitos técnicos.
    - Critérios:
        - "Mentoria" de engenheiros seniores e plenos.
        - Experiência em propor e aprovar mudanças arquiteturais importantes.
        - Gerenciamento de débitos técnicos e alinhamento de visão com stakeolders.
        - Habilidade de traduzir requisitos de negócio vagos em projetos técnicos estruturados.

    Notas/Exemplos: __________ (Pontuação: _ /5) 
---

- 4-  Comportamental, Ambiguidade e Visão de Negócio (Peso Médio)

    - Foco: Adaptabilidade, pensamento crítico e impacto nos resultados da empresa.
    - Critérios:
        - Aprende novas tecnologias rapidamente e adapta-se a mudanças de prioridade.
        - Demonstra senso de dono (ownership) sobre a estabilidade dos dados.
        - Comunica conceitos técnicos complexos para stakeholders não técnicos.

    Notas/Exemplos: __________ (Pontuação: _ /5) 
---

- Resumo da Avaliação

    - Pontuação Média (Técnica): ___ / 5
    - Pontuação Média (Liderança/Soft Skills): ___ / 5
    - Recomendação: ( ) Forte Contratação ( ) Contratação ( ) Não Contratar

---
    
## Perguntas Sugeridas para a Entrevista

- 1. Cenário de Ambiguidade: "Descreva o projeto de dados mais complexo que você liderou. Como você garantiu a escalabilidade e a qualidade dos dados desde o início?"

- 2. Trade-offs Arquiteturais: "Como você decidiria entre usar Kafka/Flink para processamento em tempo real vs Spark Structured Streaming?"

- 3. Influência Técnica: "Conte sobre um momento em que você precisou convencer uma equipe a adotar um novo padrão de arquitetura que eles inicialmente resistiram."

- 4. Gestão de Crise/Débito Técnico: "Descreva um pipeline de dados que falhou criticamente na produção. Como você investigou, resolveu e evitou que acontecesse novamente?"

- 5. Modelagem e Custo: "Como você abordaria a modelagem de dados para um cenário de 'Big Data' onde o custo de armazenamento é uma preocupação crítica?" 
---

## Importante

- Candidato: Nâo decore, tem que ter experiência e contexto. Um entevistador experiênte conseguirá identificar falta de experiência. No Caso, o recomendado é explicar: "Conhece o conceito/Ferramenta, mas não tive muito experiência prática. 

- Entrevistador: Respostas muito técnicas e focada em ferramentas, pode indicar falta de experiência em soluções reais, indicando apenas cursos e leitura, sem aplicação real.

## 🔜 Próximo

➡️ [Engenharia de Dados na Prática]()