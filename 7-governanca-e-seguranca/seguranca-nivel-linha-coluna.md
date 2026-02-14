# Segurança em Nível de Linha e Coluna

Nem todo acesso é binário.

Em ambientes corporativos, é comum precisar:

- Mascarar colunas sensíveis
- Filtrar linhas por região
- Restringir dados por unidade de negócio

---

## Row-Level Security (RLS)

Permite filtrar registros com base em contexto.

Exemplo:
Usuário da região Sul só visualiza dados da região Sul.

---

## Column-Level Security (CLS)

Permite restringir colunas específicas.

Exemplo:
Campo de CPF visível apenas para área autorizada.

---

## Risco comum

Implementar segurança apenas no BI.

Se a segurança não estiver na camada de dados,
ela pode ser burlada.

---

## Arquitetura correta

Segurança deve existir:

- No storage
- No catálogo
- No engine de consulta
- Na camada semântica

---

## Perguntas de maturidade

- Segurança é aplicada no dado ou na ferramenta?
- Temos política uniforme multi-engine?
- Conseguimos provar quem acessou o quê?

---

## 🔜 Próximo

➡️ [Classificação, Auditoria e Rastreabilidade](./classificacao-auditoria-rastreabilidade.md)
