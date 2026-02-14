# Contratos de Dados

Contrato de dados define:

- Estrutura esperada
- Regras de validação
- Responsabilidade por mudança
- Processo de aprovação

Sem contrato, existe dependência frágil.

---

## O que um contrato deve conter

- Esquema versionado
- Regras de validação obrigatórias
- SLA de atualização
- Dono do dataset
- Política de evolução

---

## Evolução controlada

Mudança de schema deve:

1. Ser comunicada
2. Ser versionada
3. Garantir compatibilidade (quando necessário)
4. Ter janela de transição

---

## Impacto organizacional

Contratos reduzem:

- Conflitos entre times
- Quebra silenciosa de dashboards
- Incidentes recorrentes

---

## Anti-pattern

“Alteramos a tabela e avisamos depois.”

Isso não é evolução.
É ruptura.
