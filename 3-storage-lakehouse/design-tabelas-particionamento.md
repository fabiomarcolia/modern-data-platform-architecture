# Design de Tabelas & Particionamento

Particionamento errado é dívida técnica invisível.

---

## Regra prática

Particione por:
- Colunas usadas em filtros frequentes
- Baixa a média cardinalidade
- Padrões previsíveis de consulta

---

## Anti-patterns

- Particionar por ID único
- Particionar por alta cardinalidade
- Particionar por tudo

---

## Hidden Partitioning (Iceberg)

Iceberg abstrai particionamento,
mas isso não elimina responsabilidade de design.

Você ainda precisa pensar em:

- Distribuição de dados
- Frequência de acesso
- Padrão de consultas

---

## Pergunta de liderança

Seu particionamento foi desenhado para leitura ou para ingestão?
