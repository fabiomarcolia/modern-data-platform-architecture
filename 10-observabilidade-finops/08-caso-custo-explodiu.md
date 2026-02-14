# Caso — “Custo explodiu”

## Sintoma
Athena/BigQuery batendo recorde de custo e ninguém entende por quê.

## Causa típica
- Full scans recorrentes
- Dashboards duplicados
- Queries sem partição/filtro
- Times sem orçamento

## Intervenção de plataforma
1. Medir top queries por custo
2. Identificar dashboards responsáveis
3. Criar materializações (agregações diárias)
4. Alertas e limites por domínio
5. Desativar ativos mortos

## Resultado esperado
- custo previsível
- consumo disciplinado
