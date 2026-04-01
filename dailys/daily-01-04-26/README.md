# Daily Log - Engenharia de Dados e GCP | 01/04/2026

## Resumo do Dia
Hoje os estudos avançaram para a camada de Transformação e Governança dentro do ecossistema Google Cloud, focando em como tornar os pipelines de dados mais inteligentes, performáticos e confiáveis.

---

## Arquitetura e Ingestão Moderna
Saímos do modelo tradicional de transporte de dados para entender padrões de processamento em escala.

* **Arquitetura ELT (Extract, Load, Transform):** Aprofundamento no conceito de carregar dados brutos diretamente no BigQuery para utilizar seu poder de processamento massivo nas transformações via SQL, garantindo mais flexibilidade e agilidade no pipeline.
* **Ferramenta bq CLI:** Prática com a ferramenta de linha de comando dedicada ao BigQuery para criação de datasets, tabelas e automação de carga de dados (Load Jobs).
* **BigQuery Data Transfer Service:** Exploração do serviço para agendamento e automação de ingestão de dados de fontes externas (SaaS, Cloud Storage e outros datasets).

---

## Governança e Qualidade com Dataform e BigLake
O foco principal foi entender como escalar a engenharia de dados mantendo a organização e a segurança.

* **BigLake:** Estudo da unificação entre Data Lake e Data Warehouse. O BigLake permite aplicar governança e controle de acesso a nível de linha e coluna em arquivos no Cloud Storage como se fossem tabelas nativas do BigQuery.
* **Dataform (Workflow SQL):**
    * Implementação de fluxos de trabalho SQL estruturados e versionados.
    * Uso de Linguagem Procedural no BigQuery (Scripts, variáveis e lógica de controle) para fluxos complexos.
    * **Asserções (Assertions):** Configuração de testes automáticos de qualidade de dados (Unique, Non-null, Logic checks) para impedir que dados corrompidos cheguem aos consumidores finais.

---

## Aplicação Prática e Insights
A combinação de Dataform e Asserções se conecta diretamente com a estratégia de Observabilidade Proativa que venho desenhando. 

> Insight: Enquanto as asserções do Dataform garantem a integridade técnica (campos nulos ou duplicados), a camada de IA proposta atuará na integridade de negócio (anomalias de comportamento), criando uma malha de proteção completa para os dados dos clientes.

---

## Próximos Passos
- Finalizar os Labs de BigLake Qwik Start.
- Estruturar o primeiro workflow no Dataform simulando uma carga de dados financeiros.
- Documentar os padrões de asserções mais críticos para o cenário da Digio.

---
