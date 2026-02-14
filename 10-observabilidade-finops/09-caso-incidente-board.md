# Caso — “Dados quebraram o board”

## Sintoma
Reunião executiva com números errados ou dashboard indisponível.

## Causa típica
- pipeline atrasado
- mudança de schema sem aviso
- falta de SLO e monitoramento

## Intervenção de plataforma
1. Definir SLO para o ativo crítico
2. Alertar antes da reunião (freshness/latência)
3. Playbook: rollback/último snapshot válido
4. Postmortem + prevenção (contratos/testes)
5. Comunicação executiva objetiva

## Resultado esperado
- confiança recuperada
- menos incidentes P0
