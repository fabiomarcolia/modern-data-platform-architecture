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

## Anti-pattern clássico

“Se o pipeline rodou sem erro, está tudo certo.”

Pipeline pode rodar perfeitamente… com dados errados.

---

## Perguntas de liderança

- Temos métricas de qualidade visíveis?
- Incidentes de dados são auditáveis?
- Existe SLA de confiabilidade?
