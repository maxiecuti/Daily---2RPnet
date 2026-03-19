#  Daily Update: Engenharia de Dados - 19/03/2026

##  Marcos de Aprendizado
* **Conclusão da Seção 5 - Curso PySpark (Udemy)**
    * Estudo de conectividade e ingestão de dados de fontes externas.
    * Configuração de pipelines híbridos envolvendo SQL e NoSQL.

---

##  Desafios Técnicos & Troubleshooting (Hands-on)

### 1. Camada Relacional (PostgreSQL + JDBC)
* **Desafio:** Erro de `relation does not exist` ao tentar carregar DataFrames via Spark.
* **Diagnóstico:** Inconsistência entre a existência física da tabela no banco e a chamada do Spark, além de restrições de permissão no sistema de arquivos.
* **Resolução:** * Normalização de permissões via `chmod 777` no Linux para execução de scripts DDL.
    * Validei a persistência do schema no Postgres através do terminal antes de realizar o `.load()` no PySpark.

### 2. Infraestrutura Linux & Administração de Sistemas
* **Desafio:** Falha crítica `Malformed entry` no gerenciador de pacotes `apt` durante a instalação do MongoDB.
* **Resolução:** * Troubleshooting de repositórios: remoção manual de listas de fontes corrompidas em `/etc/apt/sources.list.d/`.
    * Provisionamento do **MongoDB 7.0** utilizando chaves GPG modernas e repositórios oficiais assinados.

### 3. Ecossistema NoSQL (MongoDB)
* **Desafio:** Erros de pathing (`No such file or directory`) no utilitário `mongoimport`.
* **Resolução:** * Auditoria de diretórios com `find` e `whoami` para localizar os artefatos JSON.
    * Ingestão bem-sucedida de documentos BSON para a coleção de posts.

---

##  Integração Multi-Database com Spark
* **Dependency Injection:** Utilização da flag `--packages` para carregar o `mongo-spark-connector` em tempo de execução.
* **Data Flow:** Implementação de leituras via conector nativo, mapeando URIs de conexão para transformar dados semiestruturados em DataFrames.

```bash
# Comando de inicialização do PySpark com suporte ao ecossistema NoSQL
pyspark --packages org.mongodb.spark:mongo-spark-connector_2.12:3.0.1