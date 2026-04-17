# ✅ Checklist de Sustentabilidade (90 dias)

Objetivo: reduzir incidentes, estabilizar custo e aumentar confiança.

---

Para construir uma estratégia de sustentabilidade em plataformas de dados modernas, o foco deve migrar de apenas "funcionar" para a eficiência de recursos (GreenOps) e financeira (FinOps). 

Veja um checklist estruturado para os primeiros 90 dias, focado em Observabilidade Sustentável:


### Dias 1-30: Diagnóstico e Visibilidade (Fase de Auditoria)

O objetivo é entender onde os recursos (energia, processamento e armazenamento) estão sendo desperdiçados. 

- Mapeamento de Linhagem: Implementar Data Lineage para identificar tabelas e pipelines "órfãos" que processam dados nunca utilizados.

- Inventário de Ativos: Catalogar todos os datasets e identificar ativos com baixa frequência de uso para possível arquivamento.

- Métricas de Emissões: Configurar dashboards que rastreiem o carbono equivalente por deployment e o consumo de energia por usuário/serviço.

- Identificação de "Bad Queries": Monitorar queries de baixo desempenho que consomem excesso de CPU de forma recorrente. 

Foco é em visibilidade:

    - Inventário de ativos críticos
    - Mapear consumidores (BI/ML)
    - Métricas básicas (sucesso, latência, freshness)
    - Custo por domínio (mínimo viável)
    - Dono por domínio


### Dias 31-60: Otimização e "Ganhos Rápidos" (Fase de Ação)
Foco em eliminar o desperdício imediato identificado na fase anterior.

- Limpeza de Armazenamento: Implementar políticas de ciclo de vida (Lifecycle Policies) para mover dados frios para camadas de armazenamento de baixo custo/energia.

- Redimensionamento (Rightsizing): Ajustar o tamanho de clusters de processamento (Spark, Snowflake, BigQuery) com base nos dados de utilização real.

- Automação de Horários: Configurar o desligamento automático de ambientes de desenvolvimento e homologação fora do horário comercial.

- Deduplicação de Dados: Reduzir a redundância de dados no transporte entre múltiplos destinos usando ferramentas como RudderStack ou Segment para evitar processamento duplicado. 

Objetivo é garantir o controle:

    - SLOs para ativos críticos
    - Playbooks para P0/P1
    - Alertas por custo (top queries/pipelines)
    - Revisão de dashboards caros e pouco usados
    - Política de acesso consistente

### Dias 61-90: Governança e Cultura (Fase de Sustentação)
Institucionalizar práticas para garantir que a plataforma permaneça eficiente a longo prazo. 

- Alertas de Sustentabilidade: Configurar alertas de observabilidade não apenas para falhas, mas para anomalias de custo e picos inesperados de consumo de recursos.

- SLA de Frescor (Freshness): Definir SLAs de atualização de dados realistas; processar dados em tempo real quando o negócio exige apenas D-1 economiza energia massiva.

- Treinamento de Equipe: Educar engenheiros sobre o impacto ambiental de decisões de infraestrutura e arquitetura de dados.

- Relatórios ESG: Integrar as métricas de observabilidade de dados nos relatórios oficiais de sustentabilidade da empresa.

---


## 61–90 dias (otimização)

- Backlog mensal de otimização (FinOps)
- Compaction e lifecycle no lakehouse
- Materializações para serving
- Postmortems sistemáticos
- Relato executivo mensal (KPIs + tendências)

---

## 🔜 Próximo

➡️ [Caso: custo explodiu](8-caso-custo-explodiu.md)
