# Evolução de Schema

Schema evolution é inevitável.

A questão é:
Sua plataforma absorve mudança ou quebra com ela?

---

## Tipos de mudança

- Adição de coluna (mais comum)
- Remoção de coluna (mais perigoso)
- Mudança de tipo
- Mudança semântica

---

## Estratégias seguras

- Schema versionado
- Camada Curada como buffer
- Contrato de dados explícito
- Testes de compatibilidade

---

## Anti-patterns

- Alterar tabela diretamente em produção
- Permitir BI consumir direto da Raw
- Não comunicar mudança para consumidores

---

## Perguntas essenciais

- Quem aprova mudança de schema?
- Existe contrato formal?
- Há backward compatibility?

---

## 🔜 Próximo Capítulo

➡️ 03-storage-lakehouse/
