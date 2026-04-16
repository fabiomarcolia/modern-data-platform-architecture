# Caso — “Custo explodiu”

Um dos cenários mais comuns na era do Cloud com Data Lake ou Lakehouse,  é a "explosão" dos custos após a migração para uma Modern Data Platform  . Enquanto a promessa é agilidade e escalabilidade, a falta de governança resulta frequentemente em faturas imprevisíveis e muito superiores às expectativas.

Vejamos casos típicos de mercado sobre como esses custos disparam e como contê-los.

### 1. O Caso: Por que o custo explodiu?

A mudança de CAPEX (investimento em hardware local) para OPEX (custo operacional na nuvem) transfere a responsabilidade financeira da TI para os times de dados, que muitas vezes não têm cultura de gestão de custos. 

Principais causas da explosão de custos:

- "Lift and Shift" sem otimização: Mover arquiteturas antigas (ETL) para a nuvem sem adequá-las ao modelo ELT (Extract, Load, Transform) gera processamento ineficiente e caro.

- Consultas SQL Ineficientes: Uma única consulta mal escrita em uma tabela de TBs (terabytes) pode custar centenas de dólares.

- Armazenamento e Computação não gerenciados: Manter dados brutos desnecessários no Data Lake por longo tempo e deixar clusters de computação ligados 24/7.

- Falta de Governança (DataOps): Criação desenfreada de esquemas, tabelas temporárias e dashboards que rodam queries a cada 5 minutos sem necessidade.

- CDC (Change Data Capture) caro: Pipelines de atualização contínua de dados podem custar muito caro se reescreverem partições inteiras de dados para atualizar uma única linha.

### 2. Exemplos de Impacto Financeiro

- Invasão de Conta Cloud: Acesso indevido à AWS pode criar milhares de instâncias EC2, gerando prejuízos imediatos de centenas de milhares de reais.

- Queima de Caixa em IA: A alta demanda por treinamento de modelos e processamento (GPUs) pode levar ao estouro orçamentário, com empresas de IA queimando bilhões em energia e computação.

### 3. Como Resolver: Estratégias de FinOps (Financial Operations)

Para controlar o custo, é necessário implementar uma cultura de FinOps na plataforma de dados:

- Monitoramento e Alertas: Configurar alertas de custo imediatos. Se o gasto diário exceder X%, os administradores devem ser notificados.

- Particionamento e Clustering: Organizar os dados em partições e clusters para evitar que as queries leiam tabelas inteiras (full-table scans), reduzindo o uso de computação.

- Materialized Views: Usar materialized views para pré-calcular agregações de relatórios frequentemente acessados, eliminando cálculos redundantes e caros.

- Automação de Suspensão: Configurar o desligamento automático de computação (warehouse/clusters) quando não houver queries ativas.

- Ciclo de Vida de Dados: Mover dados frios (pouco usados) para camadas de armazenamento mais baratas (ex: S3 Glacier) e eliminar dados brutos redundantes.

---

## Exemplos de sintoma comuns de problemas 

Athena/BigQuery batendo recorde de custo e ninguém entende por quê.

### Gatilhos Comuns para a Explosão de Custos

- Consultas Ineficientes: Consultas SQL mal escritas que processam terabytes de dados desnecessários ou que não utilizam filtros adequados.

- Problema dos "Small Files": No Databricks, gravar muitos arquivos pequenos aumenta o custo de metadados e torna as leituras ineficientes, disparando o valor da fatura.

- Configurações de Atualização: Dashboards configurados para atualizar a cada 10 minutos, mesmo sendo visualizados apenas uma vez ao dia, geram um custo de computação contínuo e invisível.

- Falta de Limpeza (Vacuuming): Acúmulo de versões antigas de dados em tabelas Delta sem a execução de comandos de limpeza (VACUUM) gera custos de armazenamento crescentes.

### Causas típicas
- Full scans recorrentes
- Dashboards duplicados
- Queries sem partição/filtro
- Times sem orçamento

### Intervenção de plataforma
1. Medir top queries por custo
2. Identificar dashboards responsáveis
3. Criar materializações (agregações diárias)
4. Alertas e limites por domínio
5. Desativar ativos mortos

### Resultado esperado
- custo previsível
- consumo disciplinado

## 🔜 Próximo

➡️ [Incidentes em dados](09-caso-incidente-board.md)

