# Estudo de Caso — Varejo

## Contexto
Rede com centenas de lojas e múltiplos times (Comercial, Operações, Financeiro).
Dashboards de vendas divergiam entre áreas e o custo de consultas crescia mês a mês.

## Sintomas
- “Receita” diferente por time
- Picos de lentidão em horário comercial
- Custo imprevisível (full scans recorrentes)
- Shadow BI (planilhas paralelas)

## Decisões estruturais
1. Definir métricas oficiais na camada semântica
2. Criar datasets curados por domínio (vendas, estoque, margem)
3. Materializar agregações diárias para relatórios executivos
4. Estabelecer política de consumo (FinOps): alertas e limites
5. Power BI: modelo corporativo com governança e revisão de relatórios

## Resultado (exemplo)
- Redução relevante de custo por consulta (por eliminação de full scans)
- Queda de conflitos de métricas
- Tempo de carregamento estabilizado para painéis críticos
- Governança aplicada ao consumo (sem travar o negócio)

## Lição
Serving não é “performance”. É confiança + custo + governança.
