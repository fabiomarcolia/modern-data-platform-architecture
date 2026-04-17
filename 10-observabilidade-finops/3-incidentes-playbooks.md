# Incidentes: Triage, Impacto e Playbooks

Incidente em dados é inevitável.

O diferencial é **tempo de resposta** e **aprendizado**.

![Incidente](/assets/diagramas/ciclo-incidente-dados.png)

---

A gestão de incidentes de dados envolve identificar, analisar e responder a eventos que comprometem a confidencialidade, integridade ou disponibilidade de dados pessoais ou confidenciais. Conforme a Resolução CD/ANPD nº 15/2024, isso inclui ações voluntárias ou acidentais. 

### Triage (prioridade em 3 perguntas)

A triagem (triage) é a fase de detecção e análise inicial, crucial para separar alarmes falsos de ameaças reais e priorizar a resposta

- 1. Afeta decisão executiva?
- 2. Afeta cliente/receita?
- 3. Afeta compliance/risco?

- Identificação: Detecção automática (SIEM/XDR) ou manual (relato de usuário) de anomalias.

- Classificação Inicial:

    - Violação de Confidencialidade: Acesso indevido a dados pessoais (ex: vazamento).
    - Violação de Integridade: Alteração não autorizada de dados.
    - Violação de Disponibilidade: Dados tornados inacessíveis (ex: ransomware).

- Avaliação Rápida (Triagem):

    - Que tipo de dado foi afetado? (Pessoal, sensível, financeiro, sigiloso?)
    - Quem foi afetado? (Funcionários, clientes?)
    - Qual a escala? (Quantos registros?

---

### Impacto (o que medir)

O impacto determina a urgência da resposta e a necessidade de notificação legal (conforme a LGPD)

- Dashboards quebrados
- Datasets afetados
- Times impactados
- Decisões possivelmente erradas
- Custo gerado durante a falha

- Risco ou Dano Relevante: Se o incidente puder acarretar dano aos titulares, a notificação à ANPD e aos titulares é necessária, idealmente em até 72 horas.

- Graus de Impacto:

    - Baixo: Dados públicos, sem risco direto ao titular.
    - Médio: Dados pessoais (nome, e-mail) expostos internamente.
    - Alto: Dados sensíveis (CPF, saúde, financeiro) expostos publicamente.

- Consequências: Multas da LGPD (até 2% do faturamento), perda de confiança, danos à reputação.

---

### Playbook mínimo

Os playbooks são roteiros passo a passo (step-by-step) para garantir uma resposta consistente e rápida, muitas vezes automatizada via ferramentas SOAR.

- Quem é o dono?
- Como pausar propagação?
- Como rollback?
- Como comunicar?
- Como validar correção?

Exemplo de Playbook para Vazamento de Dados (Data Breach):

- 1- Detecção e Alerta: Identificação de exfiltração de dados (alerta SIEM/DLP).

- 2- Contenção:

    - 1. Isolar sistemas afetados da rede.
    - 2. Revogar credenciais comprometidas.
    - 3. Bloquear IPs suspeitos.

- 3- Análise e Investigação:

    - 1. Identificar o "ponto de entrada" (phishing, erro de configuração, ataque interno).
    - 2. Determinar os dados exatos que foram copiados ou acessados.

- 4- Erradicação:

    - 1. Remover backdoors ou malware.
    - 2. Corrigir a vulnerabilidade de software.

- 5- Recuperação:

    - 1. Restaurar sistemas a partir de backups seguros.
    - 2. Monitorar para novas atividades suspeitas.

- 6. Pós-Incidente:

    - 1. Elaborar relatório final (post-mortem).
    - 2. Revisar o playbook com base nas lições aprendidas.

---

### Melhores Praticas

- Linha do tempo
- Causa raiz
- Mitigação
- Prevenção
- Métricas de melhoria

1- Automação: Use ferramentas SOAR para automatizar a triagem de alertas e reduzir o impacto financeiro.

2- Documentação: A legislação exige que a empresa esteja preparada para demonstrar a gestão de incidentes.

3- RACI: Utilize uma matriz RACI (Responsável, Accountable, Consulted, Informed) para definir papéis claros no tratamento.

---

## 🔜 Próximo

➡️ [Métricas de Plataforma](4-metricas-plataforma.md)
