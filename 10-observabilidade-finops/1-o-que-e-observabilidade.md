# O que é Observabilidade de Dados

Observabilidade é a capacidade de **entender o estado interno** do sistema a partir de sinais.

Em dados, isso significa responder rápido:

- O que quebrou?
- Onde quebrou?
- Quem foi impactado?
- Como mitigar?
- Como evitar de novo?

![Observabilidade](/assets/diagramas/data-observability-camadas.png)

---
É uma abordagem holística que utiliza automação para monitorar, rastrear e analisar a saúde, o desempenho e a confiabilidade dos dados em toda a sua jornada (pipeline). Ao contrário do monitoramento tradicional, ela fornece visibilidade completa para detectar anomalias, como quedas de volume, esquemas quebrados ou dados imprecisos antes que afetem decisões críticas

### Pilares e Funcionalidades Principais
A observabilidade de dados geralmente se baseia em três pilares fundamentais, frequentemente citados em contextos de engenharia de dados e sistemas: 

- Logs: Registros detalhados de eventos de dados.

- Métricas: Medições quantitativas sobre a saúde dos pipelines.

- Rastreamentos (Traces): Acompanhamento do fluxo dos dados para identificar gargalos e falhas de integração.

As ferramentas de observabilidade de dados oferecem monitoramento em tempo real, alertas proativos e automação para resposta a incidentes, garantindo que os dados sejam confiáveis e governados

### Benefícios da Observabilidade de Dados

- 1- Confiabilidade: Detecta automaticamente dados ausentes ou imprecisos, melhorando a qualidade.

- 2- Redução de Tempo de Inatividade: Identifica problemas de pipeline antes que eles causem interrupções significativas.

- 3- Governança e Conformidade: Auxilia no cumprimento de normas de privacidade, identificando violações de segurança.

- 4- Eficiência Operacional: Proporciona uma visão clara do fluxo, facilitando a tomada de decisões informadas e otimizando o desempenho. 

### Diferença entre Observabilidade e Monitoramento

Enquanto o monitoramento informa se um sistema está funcionando ou não (baseado em métricas pré-definidas), a observabilidade de dados permite entender o comportamento interno do sistema ao analisar as saídas, facilitando a descoberta da causa raiz de problemas complexos.

- Monitoramento: “o job falhou”.
- Observabilidade: “o job falhou + impacto + causa provável + ação recomendada”.

---

### Os 3 sinais clássicos (adaptados)

- **Métricas**: volumes, latência, sucesso, custo
- **Logs**: erros e contexto técnico
- **Traces/Lineage**: dependências e impacto

---

### Anti-patterns

- Alertas sem dono
- Métricas sem contexto
- “Corrigir depois” sem postmortem
- Sem lineage → impacto vira adivinhação

---

## 🔜 Próximo

➡️ [SLOs e SLAs](2-slos-slas.md)
