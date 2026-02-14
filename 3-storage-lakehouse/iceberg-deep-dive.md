# Iceberg — Deep Dive

Iceberg é mais que um formato.

É uma camada de abstração sobre arquivos físicos que fornece:

- Snapshot isolation
- Schema evolution
- Hidden partitioning
- Time travel

---

## Estrutura Interna (simplificada)

- Data files (Parquet/ORC)
- Manifest files
- Metadata files
- Snapshot log

Metadata cresce conforme a tabela cresce.

---

## Metadata Explosion

Problema:
- Muitos commits pequenos
- Pequenos arquivos frequentes
- Falta de compactação

Impacto:
- Consultas lentas
- Alto consumo de metadados
- Custos inesperados

Mitigação:
- Compaction jobs periódicos
- Limitar frequência de commits
- Estratégia clara de ingestão

---

## Time Travel na prática

Permite:
- Reproduzir estado anterior
- Auditar mudanças
- Recuperar erros humanos

Mas cuidado:
- Retenção longa aumenta custo
- Snapshot excessivo aumenta metadata
