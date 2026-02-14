# BI em Escala Corporativa (inclui Power BI)

BI em escala não é “ter muitos dashboards”.
É **sustentabilidade operacional** com confiança.

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
