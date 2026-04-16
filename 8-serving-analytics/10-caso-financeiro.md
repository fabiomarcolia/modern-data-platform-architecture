# Estudo de Caso — Financeiro

## O que não funciona e riscos

### Contexto
Instituição financeira com exigências regulatórias e auditoria frequente.
Indicadores de risco divergiam e o processo de auditoria era manual.

### Sintomas
- Divergência de métricas de risco
- Acesso inconsistentes a dados sensíveis
- Auditoria lenta e com baixa rastreabilidade
- Alto risco reputacional/regulatório

### Decisões estruturais
1. Classificar datasets (interno/sensível/regulado)
2. Aplicar RLS/CLS na camada de dados (não apenas no BI)
3. Camada semântica versionada (mudanças auditáveis)
4. Auditoria estruturada por engine + BI
5. FinOps integrado: custo por domínio e por dados regulados

### Resultado (exemplo)
- Auditoria automatizada e rastreável
- Redução de incidentes de acesso indevido
- Métricas de risco unificadas
- Sustentabilidade financeira do consumo analítico

### Lição
Em finanças, serving é também “controle de risco”. Performance vem depois.

---

## Casos de Sucesso

Estudos de caso sobre Serving Analytics no setor financeiro concentram-se em como a análise de dados em tempo real (ou quase real) é "servida" para alimentar produtos digitais, detectar fraudes ou otimizar a rentabilidade de clientes. Abaixo, os principais tipos de aplicação e exemplos reais: 

### 1. Detecção de Fraude e Risco em Tempo Real

A análise de dados é "servida" instantaneamente durante o checkout para prevenir perdas financeiras.

- Revolut (Sistema Sherlock): Utiliza modelos de Machine Learning para avaliar transações em menos de 50 milissegundos. O sistema decide se bloqueia a compra ou solicita verificação adicional do cliente.

- HSBC: Implementou o Dynamic Risk Assessment em parceria com o Google Cloud, reduzindo o volume de alertas falsos em 60% e aumentando a detecção de crimes reais em até 4 vezes. 

### 2. Rentabilidade e Segmentação de Clientes

Empresas utilizam analytics para entender o custo de servir cada perfil e ajustar precificação.

- Netflix: Aplica analytics para segmentação de lucratividade por assinante, comparando a receita gerada por usuário individual versus seu custo de manutenção. Isso informa decisões de precificação e pacotes (bundling).

- Consultoria B2B2C: Um estudo de caso demonstrou o uso do Método ABC (Custeio Baseado em Atividades) para estruturar os custos envolvidos em servir clientes finais através de aplicativos, identificando a rentabilidade real por produto.

### 3. Previsão de Fluxo de Caixa e Investimentos

A integração de dados contábeis permite previsões automatizadas que substituem planilhas manuais.

- J.P. Morgan & Prysmian: Implementaram soluções de AI cash-flow forecasting que, segundo o banco, "se pagam sozinhas" ao otimizar a gestão de liquidez diária.

- Tesla (Gigafactories): Utiliza modelos financeiros complexos para decidir sobre a construção de novas fábricas, analisando se o investimento sustenta as metas de longo prazo no mercado de veículos elétricos.

### Estrutura de Implementação
Para que o Serving Analytics seja eficaz, as empresas seguem geralmente estas etapas:

- Coleta e Limpeza: Inspeção rápida para identificar variáveis quantitativas (como saldo em conta) e qualitativas (como profissão).

- Modelagem Exploratória: Uso de tabelas dinâmicas ou dashboards para entender o perfil inicial do cliente antes de aplicar modelos avançados.

- Visualização e Ação: Tradução de termos técnicos para linguagem de negócios, facilitando a tomada de decisão

## Conclusão

Em resumo, o Serving Analytics transforma dados financeiros de "arquivos históricos" em ativos operacionais ativos.

O sucesso desses estudos de caso mostra que a vantagem competitiva não vem apenas de ter os dados, mas da baixa latência em entregá-los: seja para bloquear uma fraude em milissegundos, ajustar o limite de crédito no momento da compra ou prever o fluxo de caixa antes de uma crise de liquidez. No fim do dia, servir analytics no setor financeiro é sobre reduzir o tempo entre o evento e a decisão.

--- 

## 🔜 Próximo

➡️ [ML e IA](../9-ml-e-ia-integracao)
