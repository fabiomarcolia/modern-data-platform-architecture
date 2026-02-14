# Gerenciamento de Secrets e Segurança

Regra de ouro:
**se está no repo, já vazou.**

---

## Boas práticas

- usar GitHub Secrets / Vault / Secret Manager
- rotacionar credenciais
- princípio do menor privilégio (IAM)
- separar credenciais por ambiente (DEV/STG/PROD)
- logs sem dados sensíveis (redaction)

---

## Anti-patterns

- `.env` commitado
- chave em notebook
- credencial compartilhada por time
- token com acesso total

---

## 🔜 Próximo

➡️ [Release e Versionamento](./08-release-versionamento.md)
