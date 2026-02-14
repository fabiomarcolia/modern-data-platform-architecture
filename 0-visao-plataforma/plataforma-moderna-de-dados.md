# Plataforma Moderna de Dados

Uma Plataforma Moderna de Dados é um sistema estruturado que permite:

- Confiabilidade contínua
- Evolução arquitetural
- Escala organizacional
- Controle de custo
- Governança integrada

Não se trata de tecnologia específica, mas de desenho sistêmico.

---

## Componentes Estruturais

### 1. Camadas claras

- Raw (imutável, auditável)
- Curado (confiável, versionado)
- Serving (consumo analítico e operacional)

Sem essa separação, a plataforma degrada rapidamente,
pois regras de negócio passam a se misturar com ingestão e consumo.

---

### 2. Contratos e Semântica

Uma plataforma madura define:

- Métricas oficiais
- Definições versionadas
- Responsabilidade por domínio

Anti-pattern clássico:
Cada área calcula a mesma métrica de forma diferente.

---

### 3. Operação e Confiabilidade

Plataforma exige:

- SLAs e SLOs claros
- Monitoramento de freshness, volume e erros
- Playbooks de incidentes
- Backfills seguros e reprocessamento controlado

Sem operação, existe apenas pipeline — e pipeline não sustenta crescimento.

---

## Diferença entre Stack Moderna e Plataforma Madura

Stack Moderna:
- Iceberg
- Spark
- Airflow
- Power BI

Plataforma Madura:
- Decisões documentadas
- Custos previsíveis
- Donos claros de dados
- Evolução controlada

---

## Perguntas que revelam maturidade

- Conseguimos reprocessar qualquer período com segurança?
- Existe dono para cada dataset?
- Sabemos custo por domínio?
- Conseguimos desligar um pipeline sem impacto sistêmico?

---

## 🔜 Próximo passo

Continue para:  
➡️ [Por que não apenas ferramentas](./por-que-nao-apenas-ferramentas.md)
