# Casos reais: o que dá errado

Em projetos reais de CI/CD e DataOps, as falhas geralmente não ocorrem por falta de ferramentas, mas por gaps de processo, cultura e complexidade técnica. Abaixo estão os problemas mais comuns relatados por especialistas e equipes de engenharia.

--- 

### 1. O Pipeline "Mente" (Falsa Sensação de Segurança)

Um erro crítico é o pipeline passar (ficar "verde") mesmo quando o sistema não está seguro para deploy. 

- O que dá errado: Testes passam, mas o ambiente de produção quebra por variáveis de ambiente ausentes, incompatibilidade de versões de dependências ou esquemas de banco de dados desalinhados.

- Caso Real: Deploys que funcionam em staging, mas falham em produção porque a URL do banco de dados estava "hardcoded" ou o firewall de produção bloqueava o tráfego que o ambiente de teste permitia. 

### 2. A "Dívida de Dados" no DataOps

Diferente do software puro, o DataOps lida com o estado e a qualidade dos dados, o que gera gargalos específicos.

- O que dá errado: Pipelines de dados que não validam a qualidade na entrada. O código do pipeline está correto, mas os dados estão "sujos", causando falhas silenciosas em relatórios de BI ou modelos de IA.

- Refresh de Dados: Equipes que usam dados de teste desatualizados (ex: refrescados apenas uma vez por ano). Isso gera falsos positivos (erros que não existem) ou falsos negativos (bugs reais que não aparecem no teste). 

### 3. Complexidade Excessiva e "Culture of Copy-Paste"

Muitos projetos falham ao tentar automatizar tudo de uma vez ou copiar scripts sem entender o contexto. 

-  O que dá errado: Pipelines tão complexos que ninguém na equipe consegue depurá-los quando quebram. Isso gera frustração e faz com que os desenvolvedores ignorem falhas, o famoso "acostumar-se com o vermelho".

- Gargalo Humano: Falta de alinhamento entre DevOps e Desenvolvedores. Às vezes, o time de DevOps assume a implementação sem ouvir as necessidades reais de quem desenvolve, criando um sistema frágil e sem "dono" claro. 

### 4. Falhas de Segurança (DevSecOps Ignorado)

A automação pode acelerar a propagação de vulnerabilidades se não houver verificações integradas. 

- O que dá errado: Exposição de credenciais (secrets) em logs de build ou variáveis de ambiente sem proteção.

- Exemplo: Pipelines que sofrem ataques de Server-Side Request Forgery (SSRF) por rodar códigos customizados ou ter permissões excessivas em instâncias de nuvem. 

### 5. Falta de Observabilidade e Feedback Loop

Se o pipeline falha e a única ação é "tentar de novo", o projeto está fadado ao erro recorrente. 

- O que dá errado: Ausência de métricas de performance do próprio pipeline (tempo de build, taxa de sucesso). Sem análise de tendências, os gargalos de latência e consumo de recursos só são percebidos quando o sistema já está lento demais para os usuários. 


## Casos Clássicos

- 1) “Mergei e quebrou o board”
Causa: sem gate de freshness e sem SLO do dashboard crítico.

- 2) “Custo dobrou em 1 semana”
Causa: query nova sem partição, sem alerta e sem orçamento.

- 3) “Modelo piorou e ninguém viu”
Causa: sem monitoramento de drift, sem rollback de versão.

- 4) “Vazamento de credencial”
Causa: secret no repo/notebook.

---

## Conclusão

Para evitar esses cenários, recomenda-se começar com pipelines simples, priorizar a visibilidade (monitoramento) e garantir que a automação seja acompanhada por uma mudança na cultura da equipe.

## 🔜 Próximo

➡️ [Engenharia de Dados](12-engenharia-de-dados.md)


