# Daily Report - Engenharia de Dados | 30 de Março de 2026

## Resumo do Dia
Hoje o foco foi totalmente voltado para **Arquitetura de Dados no Google Cloud Platform (GCP)**. Realizei um mergulho técnico em simulações de cenários reais para escolha de ferramentas, otimização de custos e governança de dados em larga escala.
Além da Participação do treinamento do TecHub de Governança Inteligente de Dados para IA com Dataplex

---

## Principais Aprendizados

### Orquestração e Automação
* **Cloud Composer (Apache Airflow):** Consolidado como a ferramenta mestre para gerenciar fluxos complexos (DAGs) que envolvem múltiplas etapas e diferentes serviços (Storage -> Dataflow -> BQ).
* **CI/CD com Cloud Build:** Entendi como automatizar o deploy de pipelines do Dataflow a partir de gatilhos (triggers) no repositório, garantindo integração contínua com o mínimo de esforço manual.

### Processamento de Dados (Batch & Streaming)
* **Dataproc Serverless:** Aprofundamento na execução de jobs **PySpark** sem a necessidade de gerenciar infraestrutura de clusters, focando apenas no código e na lógica de transformação.
* **Dataflow (Apache Beam):** Diferenciação entre janelamento fixo (**Fixed Windows**) para relatórios por hora e janelas de sessão ou deslizantes. 
* **Arquitetura de Streaming:** Reforcei o padrão `Pub/Sub -> Dataflow -> BigQuery` para processamento em tempo real com garantia de entrega *exactly-once*.

### Armazenamento e Performance
* **BigQuery (Analytics):** Melhores práticas de **desnormalização** usando campos aninhados (`STRUCT`) e repetidos (`ARRAY`) para evitar JOINs pesados em tabelas de petabytes.
* **Bigtable:** Identificado como a solução ideal para dados de séries temporais financeiras de alta escala (chave-valor).
* **Cloud SQL:** Escolha padrão para sistemas transacionais (OLTP) de escala regional com baixa sobrecarga administrativa.

### Governança e Segurança (Dataplex)
* **Organização de Lakes:** Estruturação de zonas brutas (**Raw**) e zonas curadas (**Curated**) para facilitar a descoberta de dados.
* **Segurança no Storage:** Entendimento da natureza aditiva entre permissões **IAM** e **ACLs**, além da importância dos **Data Access Logs** para auditoria.
* **Gestão de Custos:** Implementação de políticas de **Ciclo de Vida** no Cloud Storage (Standard -> Coldline) para otimizar gastos com dados de auditoria de longo prazo.

---

## Tecnologias Exploradas
* ![GCP](https://img.shields.io/badge/Google_Cloud-4285F4?style=flat&logo=google-cloud&logoColor=white) **Google Cloud Platform**
* ![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=flat&logo=apache-spark&logoColor=white) **PySpark / Dataproc**
* ![BigQuery](https://img.shields.io/badge/BigQuery-669DF6?style=flat&logo=google-cloud&logoColor=white) **BigQuery & SQL**
* ![Airflow](https://img.shields.io/badge/Apache_Airflow-017CEE?style=flat&logo=apache-airflow&logoColor=white) **Cloud Composer**

---

## Próximos Passos
- Avançar no curso de Data Enginner do Google Skills