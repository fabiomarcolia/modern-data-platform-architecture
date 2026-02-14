# GitHub Actions: Pipeline Base (exemplo)

Abaixo um exemplo minimalista e realista para PR:

```yaml
name: ci-dados
on:
  pull_request:
    branches: [ "main" ]

jobs:
  validar:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - name: Setup Python
        uses: actions/setup-python@v5
        with:
          python-version: "3.11"

      - name: Instalar dependências
        run: |
          pip install -r requirements.txt

      - name: Lint
        run: |
          ruff check .

      - name: Testes
        run: |
          pytest -q
```

---

## Evolução (nível plataforma)

- adicionar job de “data checks” (staging)
- adicionar “contract checks”
- adicionar “build artifacts” (containers)
- adicionar “deploy” com aprovação de ambiente

---

## 🔜 Próximo

➡️ [Secrets e Segurança](./07-secrets-e-seguranca.md)
