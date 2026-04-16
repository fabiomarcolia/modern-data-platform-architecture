# Arquitetura de Referência

Uma plataforma madura precisa funcionar bem em 3 dimensões:

- **Entrega**: dados chegam e ficam disponíveis
- **Confiança**: qualidade, governança e semântica
- **Operação**: monitoramento, reprocessamento e custo previsível

Arquitetura não é sobre “qual ferramenta”.  
É sobre **contratos, camadas e decisões sustentáveis**.

---

## 📐 Diagrama Oficial

Este é o diagrama que representa a progressão de uma plataforma madura:

![Arquitetura Evolutiva da Plataforma](/assets/diagramas/evolutionary-architecture.png)

---

## Camadas mínimas (que sustentam escala)

1- **Ingestão**
- Batch como padrão
- Streaming apenas quando há justificativa

2- **Armazenamento (Lakehouse)**
- Raw imutável
- Curado como “fonte confiável”
- Serving para consumo (BI/ML/APIs)

3- **Processamento**
- SQL-first quando possível
- Spark quando necessário (e não por hábito)

4- **Orquestração**
- Backfills e idempotência como requisitos
- Observabilidade desde o começo

5- **Governança & Segurança**
- Acesso como política (não “favor”)
- Auditoria e classificação

---

## Decisões que definem maturidade

### Iceberg vs Delta (não existe resposta universal)

**Iceberg**
- Forte interoperabilidade
- Bom para ambientes multi-engine
- Evita lock-in

**Delta**
- Excelente integração com ecossistemas específicos
- Forte em ambientes mais controlados

↳ Trade-off: **portabilidade** vs **integração profunda**

---

### Quando NÃO usar Spark

Spark é excelente… quando você tem motivo.

Evite Spark quando:
- volume é pequeno/moderado
- complexidade operacional não compensa
- o time não sustenta operação (deploy, tuning, custo)
- SQL engines resolvem com menos fricção

↳ Senioridade é saber dizer “não” para complexidade.

---

## Anti-patterns (quase sempre fatais)

- Misturar Raw e Curado
- BI lendo direto da camada Raw
- Transformação sem versionamento (regras “no dashboard”)
- Time sem dono claro do dado (ownership difuso)

---

## 🔜 Próximo tópico

➡️ Continue para: [Lakehouse na AWS](./lakehouse-aws.md)
