# Conceitos de Lakehouse

Lakehouse não é “data lake com marketing”.

É a combinação de:

- Armazenamento aberto (object storage)
- Tabelas transacionais (Iceberg/Delta)
- Engines desacopladas
- Governança transversal

---

## 📐 Diagrama Oficial

![Arquitetura Evolutiva](../diagrams/assets/evolutionary-architecture.png)

---

## O que diferencia Lakehouse de Data Lake

Data Lake tradicional:
- Arquivos soltos
- Sem controle transacional
- Alto risco de inconsistência

Lakehouse:
- Versionamento de tabela
- Schema evolution controlado
- Time travel
- Snapshot isolation

---

## Erro comum

Acreditar que usar Iceberg automaticamente cria maturidade.

Sem:
- contratos
- compactação
- estratégia de particionamento
- monitoramento

… você apenas sofisticou o problema.
