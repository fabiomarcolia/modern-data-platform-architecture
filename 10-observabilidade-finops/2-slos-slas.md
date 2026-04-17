# SLOs, SLAs e SLIs para Dados

SLOs (Objetivos de Nível de Serviço) e SLAs (Acordos de Nível de Serviço) para dados definem metas de qualidade e confiabilidade, como tempo de atualização e integridade, garantindo que os dados sejam confiáveis para decisões de negócios. Eles baseiam-se em SLIs (indicadores) para monitorar e manter a confiança, estabelecendo métricas claras. 

- SLO = objetivo interno de confiabilidade (engenharia).
- SLA = compromisso com o consumidor (negócio).

### Conceitos Principais 

- SLI (Service Level Indicator): A métrica técnica que mede o que está acontecendo (ex: % de pipelines concluídos no horário).

- SLO (Service Level Objective): A meta interna (o alvo) baseada no SLI (ex: 
 das tabelas atualizadas até 08:00).

- SLA (Service Level Agreement): O contrato formal com o cliente, geralmente com penalidades financeiras se o SLO não for atingido (ex: 
 de falhas de dados por mês). 

### Exemplos de SLOs para Dados:

- Frescor (Freshness): Dados do dashboard de vendas atualizados 
 das vezes até 06:00 AM.

- Integridade (Completeness): Menos de 
 de registros nulos em colunas críticas (ex: ID_Cliente).

- Precisão (Accuracy): Taxa de erro nos dados financeiros.

- Volume: O tamanho da tabela diária não deve variar mais que 
 em relação à média dos últimos 7 dias. 

### Benefícios de SLAs/SLOs de Dados:

- Confiança: Aumenta a confiança dos usuários nos dados, evitando decisões baseadas em informações erradas.

- Responsabilidade: Define claramente quem é o proprietário dos dados e quem responde pelas falhas.

- Priorização: Ajuda equipes de dados a focar na estabilidade dos pipelines mais importantes (usando error budgets).

---

## Exemplos de SLOs úteis

- Disponibilidade do dataset crítico: 99,5%
- Latência de atualização: até 2h (P95)
- Atraso máximo permitido (freshness): 4h
- Taxa de falhas de pipeline: < 0,5%/dia
- Incidentes críticos: < 2/mês

---

## Definição recomendada

1. Identificar datasets/dashboards críticos
2. Definir consumidores (quem sofre)
3. Definir janela de medição (semana/mês)
4. Definir erro orçamentário (error budget)
5. Criar alerta + playbook

---

## Error Budget (o que impressiona liderança)

Se o error budget estoura:
- congela mudanças não críticas
- prioriza confiabilidade

---

Serving maduro (Cap. 08) pede SLO.
ML/IA (Cap. 09) pede SLO.

--- 

## 🔜 Próximo

➡️ [Incidentes e Playbooks](3-incidentes-playbooks.md)
