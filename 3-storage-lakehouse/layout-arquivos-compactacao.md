# Layout de Arquivos & Compactação

Small files são o câncer silencioso do Lakehouse.

---

## O problema

- Muitos arquivos pequenos
- Alto overhead de leitura
- Metadados inflados
- Performance degradada

---

## Causas comuns

- Micro-batches excessivos
- Streaming mal configurado
- Escritas concorrentes descoordenadas

---

## Estratégias de mitigação

- Compaction periódica
- Controle de tamanho de arquivo (target file size)
- Balanceamento de escrita

---

## Pergunta crítica

Sua estratégia considera custo de leitura ou apenas velocidade de ingestão?

---

## 🔜 Próximo Capítulo

➡️ 04-processing/
