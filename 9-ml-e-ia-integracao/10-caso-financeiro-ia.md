# Estudo de Caso — Financeiro (IA com risco e auditoria)

## Contexto
Instituição financeira com decisão automatizada (crédito/fraude).
Regulação e auditoria são parte do sistema.

## Problema real
- Modelos com baixa explicabilidade
- Dados sensíveis sem política clara
- Auditoria manual e lenta
- Risco reputacional

## Decisões de plataforma
1. Classificação de dados (sensível/regulado)
2. RLS/CLS aplicado na camada de dados
3. Registro de modelos com owner e nível de risco
4. Auditoria de decisão automatizada (logs estruturados)
5. Monitoramento de drift e viés (quando aplicável)
6. FinOps: custo por decisão e por endpoint

## Resultado (exemplo)
- Auditoria automatizada e rastreável
- Redução de risco regulatório
- Transparência sobre decisões
- Controle de custo e previsibilidade

## Lição
Em finanças, IA sem governança não é inovação.
É risco.
