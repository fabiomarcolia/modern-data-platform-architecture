# Estudo de Caso — Varejo (IA com plataforma)

## Contexto
Rede varejista com previsão de demanda e abastecimento.
A empresa sofria com ruptura e excesso de estoque ao mesmo tempo.

## Problema real
- Modelo treinado “na marra” com features inconsistentes
- Drift sazonal derrubava performance
- Times diferentes tinham pipelines duplicados
- Custo de inferência crescia sem controle

## Decisões de plataforma
1. Dados curados com contratos (vendas, estoque, promoções)
2. Feature Store para features críticas (sazonalidade, promo, elasticidade)
3. Dataset de treino por janela (snapshots) para reprodutibilidade
4. Monitoramento semanal de drift + alertas
5. FinOps: custo por predição e limites por área
6. Serving: batch para planejamento + online para ajustes

## Resultado (exemplo de impacto)
- Redução de ruptura
- Redução de excesso de estoque
- Menos retrabalho entre times
- Previsibilidade de custo

## Lição
Varejo não precisa de “modelo melhor” primeiro.
Precisa de **features consistentes + monitoramento + custo controlado**.
