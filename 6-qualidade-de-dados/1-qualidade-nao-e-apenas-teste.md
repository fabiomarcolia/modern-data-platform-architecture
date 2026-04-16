# Qualidade não é apenas teste

Muitas equipes confundem qualidade com:
- Testes unitários
- Validações simples de NULL
- Checagem básica de schema

Isso é o mínimo.

Qualidade real envolve:

- Confiabilidade
- Observabilidade
- Contrato explícito
- Responsabilidade clara

---

## Dimensões da Qualidade

1. Freshness  
Dados estão atualizados no tempo esperado?

2. Volume  
Mudanças abruptas indicam falha ou comportamento legítimo?

3. Integridade  
Chaves, duplicidades, consistência referencial.

4. Consistência Semântica  
A métrica mantém o mesmo significado ao longo do tempo?

---

## Métricas de Qualidade

Métricas de qualidade de dados são indicadores essenciais para medir a confiabilidade, precisão e utilidade das informações, garantindo tomadas de decisão corretas. Exemplo:

- Completude (Completeness): Mede a porcentagem de registros que possuem todos os dados obrigatórios, ex: "95% dos perfis de clientes possuem CPF".

- Precisão (Accuracy): Avalia se o dado representa a realidade, ex: se o endereço no banco de dados corresponde ao local físico onde o cliente reside.

- Consistência (Consistency): Verifica a uniformidade entre sistemas ou tabelas, ex: o status do cliente é "Ativo" tanto no CRM quanto no sistema de faturamento.

- Validade (Validity): Confirma se os dados seguem as regras de negócio e formatos definidos, ex: e-mails com formato usuario@dominio.com ou datas num formato único.

- Atualidade/Tempestividade (Timeliness): Mede se o dado está disponível no tempo necessário para uso, ex: dados de vendas atualizados a cada 15 minutos.

- Unicidade/Duplicação (Uniqueness): Porcentagem de registros que não são duplicados, ex: "0% de duplicatas na tabela de produtos".

- Razoabilidade/Integridade (Reasonableness): Verifica se os dados estão dentro de limites lógicos, ex: uma data de nascimento não pode estar no futuro ou uma idade maior que 120 anos.

- Tempo de Inatividade dos Dados (Data Downtime): Tempo que dados incorretos ou indisponíveis ficam acessíveis antes de serem corrigidos. 

- O monitoramento dessas métricas, como taxas de erro e valores nulos (NULLs), é fundamental para a integridade dos sistemas. 

---

## Anti-pattern clássico

“Se o pipeline rodou sem erro, está tudo certo.”

Pipeline pode rodar perfeitamente… com dados errados.

---

## Perguntas de liderança

- Temos métricas de qualidade visíveis?
- Incidentes de dados são auditáveis?
- Existe SLA de confiabilidade?

## 🔜 Próximo

➡️ [Contratos de Dados](2-contratos-de-dados.md)
