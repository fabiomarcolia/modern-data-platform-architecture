# BI em Escala Corporativa (inclui Power BI)

BI em escala não é “ter muitos dashboards”.
É **sustentabilidade operacional** com confiança.

Isso tem a ver com a capacidade de uma organização de expandir seus processos de análise de dados para atender a um grande volume de usuários, fontes de dados crescentes e demandas de processamento complexas, sem perda de performance ou confiabilidade. 

[BI em Escala](03-bi-em-escala.md)

--- 

Diferente de um projeto de BI isolado, o BI em escala exige uma estrutura que suporte o crescimento contínuo de forma sustentável através de:

1. Arquitetura e Infraestrutura Robustas

- Processamento Distribuído: Utilização de ferramentas como Apache Spark ou Hadoop para lidar com os "5 Vs" do Big Data (Volume, Velocidade, Variedade, Veracidade e Valor).

- Nuvem (Cloud BI): Plataformas como o Google Cloud e Microsoft Azure permitem escalar recursos computacionais conforme a demanda.
Data Lakes e Warehousing: Centralização de dados dispersos em repositórios únicos para facilitar a governança e o acesso em larga escala. 

2. Governança e Autonomia (Self-Service BI)

- Para escalar, a TI deixa de ser o único gargalo. Ferramentas como Power BI, Tableau e Looker permitem que diferentes departamentos criem seus próprios insights.

- Cultura de Dados: Envolver a equipe e definir metas claras é essencial para que o uso do BI se torne parte do cotidiano corporativo.

3. Gerenciamento de Performance

- Escalas em Gráficos: Em grandes volumes, a visualização precisa ser cuidadosa. O uso de escalas logarítmicas ou o ajuste correto do eixo zero evita distorções em dados com grandes discrepâncias.

- Automação de ETL: Processos automatizados de Extração, Transformação e Carga (ETL) garantem que os dados estejam sempre atualizados para milhares de usuários simultâneos. 

Desafios Comuns

- Segurança: Manter o sigilo e a integridade das informações em um ambiente com muitos acessos.

- Custo: Ferramentas como o Power BI possuem diferentes níveis de licenciamento (Pro, Premium) baseados na capacidade e no número de usuários. 

---

## Arquitetura madura de consumo

Lakehouse Curado  
→ Camada Semântica  
→ Engine de Consulta  
→ Ferramenta de BI (ex.: Power BI)  
→ Usuário

---

## Onde o Power BI entra (de forma madura)

Power BI pode operar em 2 modos principais:

### Import (VertiPaq)
- Modelagem e performance excelentes
- Custo previsível por capacidade/licença
- Exige disciplina de atualização e governança do modelo

### DirectQuery (consulta na engine)
- Dados sempre “no real-time” (dependendo da fonte)
- Performance depende da engine e do design
- Exige otimização e governança de queries

Regra prática:
- Import para performance e “padrão corporativo” quando possível
- DirectQuery para casos justificados (latência, volumes, restrições)

---

## Problemas comuns em escala

- Dashboards lendo tabelas brutas
- Métricas duplicadas em relatórios diferentes
- Falta de controle de acesso por domínio
- Queries caras sem governança (custo explode)

---

## Indicadores de maturidade

- Tempo médio de carregamento (por dashboard crítico)
- % de dashboards usando camada semântica
- Custo por consulta / por dashboard
- Incidentes de divergência de métrica
- % de relatórios ativos vs “abandonados”

---

## 🔜 Próximo

➡️ [Engines de Consulta](./04-engines-de-consulta.md)
