# Daily Update: Conclusão das Seções 8 e 9 (Spark Streaming & Otimização)

Hoje finalizei dois módulos fundamentais na minha jornada de Engenharia de Dados, avançando do processamento em tempo real para a arquitetura de alta performance.

## Evolução Técnica

### Seção 8: Structured Streaming & Sinks
* **Processamento Incremental:** Implementei pipelines de leitura contínua com `.readStream`, permitindo a ingestão de dados em tempo real.
* **Micro-batching com JDBC:** Desenvolvi funções customizadas utilizando `.foreachBatch()` para persistência de dados no **PostgreSQL**, superando desafios de integração e sintaxe.
* **Resiliência:** Configurei `checkpointLocation` e utilizei `.awaitTermination()` para garantir a tolerância a falhas e a estabilidade dos scripts em produção.

### Seção 9: Performance e Arquitetura de Dados
* **Particionamento Inteligente:** Utilizei `.partitionBy()` para organizar fisicamente os dados no disco, otimizando o *I/O* através da técnica de **Partition Pruning**.
* **Bucketing e Shuffling:** Implementei `.bucketBy()` para minimizar o movimento de dados entre executores (**Shuffle**), otimizando drasticamente a performance de Joins em tabelas de alta cardinalidade.
* **Gestão de Cache:** Explorei o uso de `StorageLevel` para controle granular da memória RAM e Disco, prevenindo erros de *Out of Memory* (OOM) na VM.

## Desafios Superados (Troubleshooting)
* **Resolução de Syntax Errors:** Depuração de encadeamento de métodos JDBC em scripts Python standalone.
* **Spark SQL:** Correção de erros `TABLE_OR_VIEW_NOT_FOUND` através do registro de Views Temporárias (`createOrReplaceTempView`).
* **Environment Debugging:** Gestão de variáveis e caminhos de arquivos JAR no ambiente Linux via terminal interativo.

---

## Próximo Passo
Com a base de streaming e otimização concluída, o próximo objetivo é aplicar essas técnicas em cenários de Big Data real, focando na análise de planos de execução (DAG) e monitoramento de performance.

---
*Status: Seções 8 e 9 Concluídas ✅*