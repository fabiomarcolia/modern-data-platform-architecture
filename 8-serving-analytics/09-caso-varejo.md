# Estudo de Caso — Varejo

## O que não funciona

### Contexto
Rede com centenas de lojas e múltiplos times (Comercial, Operações, Financeiro).
Dashboards de vendas divergiam entre áreas e o custo de consultas crescia mês a mês.

### Sintomas
- “Receita” diferente por time
- Picos de lentidão em horário comercial
- Custo imprevisível (full scans recorrentes)
- Shadow BI (planilhas paralelas)

### Decisões estruturais
1. Definir métricas oficiais na camada semântica
2. Criar datasets curados por domínio (vendas, estoque, margem)
3. Materializar agregações diárias para relatórios executivos
4. Estabelecer política de consumo (FinOps): alertas e limites
5. Power BI: modelo corporativo com governança e revisão de relatórios

### Resultado (exemplo)
- Redução relevante de custo por consulta (por eliminação de full scans)
- Queda de conflitos de métricas
- Tempo de carregamento estabilizado para painéis críticos
- Governança aplicada ao consumo (sem travar o negócio)

### Lição
Serving não é “performance”. É confiança + custo + governança.
---

## Casos de Sucesso

Abaixo, detalhamos estudos de caso e aplicações práticas de analytics no varejo brasileiro:

### Principais Estudos de Caso no Brasil
- Magazine Luiza (Magalu): Referência em transformação digital, a empresa utiliza Big Data para integrar o varejo físico e virtual, personalizando a jornada de compra e otimizando a logística de entrega.

- Grupo Pão de Açúcar (GPA): Utiliza sistemas de relacionamento para fidelizar clientes por meio de análise de dados, permitindo ofertas personalizadas baseadas no histórico de compras.

- Amaro: Exemplo de estratégia omnichannel, onde o analytics é usado para unificar a experiência do cliente entre o app e os "Guide Shops", focando na fidelização.

- Grupo Pereira (Bate Forte Atacadista): Implementou cultura de dados e Big Data para otimizar processos internos e melhorar a eficiência do modelo de atacarejo.

- Adidas Brasil: Foco em analytics aplicado ao atendimento ao cliente para identificar estratégias de gestão de público e melhoria de conversão. 

### Aplicações de Serving Analytics no Varejo

No contexto de "serving" (servir o dado), as principais funcionalidades incluem:

- Recomendações Hiperpersonalizadas: Rastreio do comportamento em tempo real para sugerir produtos específicos durante a navegação.

- Precificação Dinâmica: Monitoramento constante de tendências e concorrência para ajustar preços automaticamente.

- Otimização de Estoque: Integração de dados de lojas físicas e online para evitar rupturas e excesso de produtos.

- Prevenção de Fraudes: Análise de padrões de pagamento em milissegundos para detectar atividades suspeitas no checkout.

### Benefícios Observados

- Eficiência Operacional: Identificação de gargalos em ciclos de produção e logística.

- Tomada de Decisão Ágil: Transformação de dados brutos em visualizações interativas para gestores de loja.

- Fidelização: Redução do custo de aquisição ao focar em clientes já existentes com ofertas assertivas

## Conclusão

Serving Analytics no varejo refere-se à camada de entrega de dados processados em tempo real para alimentar aplicações, sistemas de recomendação ou painéis de decisão operacional. 

---

## 🔜 Próximo

➡️ [Estudo de caso Financeiro](10-caso-financeiro.md)