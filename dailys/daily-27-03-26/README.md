# Certificação: Formação Spark com Pyspark

Registro de conclusão do curso completo de Apache Spark utilizando a biblioteca PySpark. Este documento detalha a jornada de aprendizado, desde os fundamentos de RDDs até a orquestração de tarefas em ambientes distribuídos.

## Detalhes do Curso
- Instituição: Udemy
- Instrutor: Fernando Amaral
- Carga Horária: 11 horas
- Status: Concluído em Março de 2026

---

## Foco do Último Módulo: Execução em Cluster (Módulo 11)

No módulo de encerramento, o foco foi a transição do ambiente local para o processamento distribuído. Os principais tópicos dominados foram:

### 1. Arquitetura de Cluster
* Driver Program: Entendimento do ponto central que orquestra o SparkContext e gera o grafo de execução (DAG).
* Cluster Manager: Papel do gerenciador (Standalone, YARN ou Kubernetes) na alocação de recursos entre as aplicações.
* Workers e Executors: Como os nós escravos recebem, processam as tarefas e gerenciam o armazenamento de dados em cache.

### 2. Processamento Distribuído
* Particionamento: Estratégias para dividir grandes volumes de dados para processamento paralelo.
* Data Locality: A importância de processar o dado o mais próximo possível de onde ele está armazenado para reduzir latência de rede.
* Shuffle: Identificação e otimização de operações que exigem troca de dados entre os nós do cluster para evitar gargalos de performance.

### 3. Resiliência e Tolerância a Falhas
* Compreensão de como o Spark reexecuta tarefas em outros Workers caso um nó falhe, garantindo a integridade do pipeline de dados.

---

## Tecnologias e Ferramentas Utilizadas
* Linguagem: Python
* Engine: Apache Spark 3.x
* Bibliotecas: PySpark (SparkSQL, Dataframes)
* IDE: VS Code / Jupyter Notebooks
* Ambiente: Linux para configuração e gerenciamento de Workers

---

> O objetivo atual é aplicar esses conceitos de escalabilidade em integrações de sistemas complexos e automação de pipelines de dados.