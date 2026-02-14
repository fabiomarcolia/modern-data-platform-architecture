# Deploy & Rollback de Pipelines

Deploy em dados precisa ser reversível.

Porque:
- pipeline falha
- schema muda
- custo explode
- board quebra

---

## Estratégias de rollback

- **Rollback de código**: reverter commit/tag
- **Rollback de dados**: snapshot/time travel
- **Rollback de schema**: migrações reversíveis
- **Fallback**: último dataset válido

---

## Playbook mínimo (P0)

1. Pausar propagação
2. Restaurar último estado válido
3. Comunicar impacto
4. Postmortem
5. Ação preventiva (gate novo)

---

## 🔜 Próximo

➡️ [GitHub Actions Base](./06-github-actions-base.md)
