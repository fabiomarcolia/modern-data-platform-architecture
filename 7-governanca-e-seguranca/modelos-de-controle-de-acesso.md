# Modelos de Controle de Acesso

Controle de acesso não é dar permissão.
É definir política.

---

## RBAC vs ABAC

### RBAC (Role-Based Access Control)

- Acesso baseado em função
- Simples de implementar
- Escala até certo ponto

Problema:
Explode em quantidade de roles conforme complexidade aumenta.

---

### ABAC (Attribute-Based Access Control)

- Baseado em atributos (domínio, sensibilidade, país, etc.)
- Mais flexível
- Escala melhor em ambientes complexos

Exemplo:
Usuário pode acessar dados apenas se:
- Pertencer ao domínio X
- Estiver na região Y
- Dataset for classificado como interno

---

## Erro estrutural comum

“Criamos uma role para cada exceção.”

Isso gera:
- Complexidade
- Risco
- Auditoria impossível

---

## Perguntas estratégicas

- Quem aprova concessão de acesso?
- Existe segregação por domínio?
- Temos política clara de revogação?
- Acesso é revisado periodicamente?

---

## Governança madura implica

- Políticas declarativas
- Automação de permissões
- Versionamento de políticas
- Auditoria automática

---

## 🔜 Próximo

➡️ [Segurança em Nível de Linha e Coluna](./seguranca-nivel-linha-coluna.md)
