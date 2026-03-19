# Relatório de Atividades Técnicas — 18 de Março de 2026

O foco das atividades de hoje foi a expansão do ambiente de desenvolvimento local, com ênfase na administração de sistemas de banco de dados relacionais e na resolução de conflitos de infraestrutura em ambiente Linux.

### 1. Implementação e Configuração de SGBD (PostgreSQL)
Iniciei a instalação e configuração do **PostgreSQL** no Ubuntu Noble (24.04). Durante o processo, gerenciei a atualização de repositórios via `apt-get` e a instalação do pacote `postgresql-contrib`. O objetivo principal foi estabelecer uma camada de persistência transacional para complementar os estudos de processamento distribuído realizados anteriormente com Apache Spark.

### 2. Automação de Scripts via CLI (Metacomando \i)
Explorei a operacionalização do utilitário `psql`, especificamente o uso do metacomando `\i` (*input*). Esta funcionalidade permite a execução de scripts SQL complexos a partir de arquivos externos (`.sql`), facilitando a automação de processos de **DDL (Data Definition Language)** e a carga inicial de dados (*seed*) para ambientes de teste e desenvolvimento.

### 3. Gestão de Permissões e Segurança de Arquivos (Linux)
Durante a execução de scripts externos, realizei o *troubleshooting* de erros de **Permission Denied**. Apliquei conceitos avançados de permissões de sistema de arquivos do Linux (`chmod`), compreendendo a necessidade de isolamento de privilégios entre o usuário do sistema (`vboxjukarla`) e o usuário do serviço de banco de dados (`postgres`). Optei pela utilização de diretórios temporários públicos (`/tmp`) para garantir a fluidez na ingestão de dados, mantendo a integridade das políticas de acesso do sistema operacional.

### 4. Integração Spark SQL e Consultas Relacionais
Reforcei a prática em **Spark SQL**, focando na criação e manipulação de **Temporary Views**. Realizei exercícios de comparação entre a sintaxe declarativa SQL e a API programática de DataFrames, aplicando operações de **Join (Inner, Full e Left)** e agregações para análise exploratória de dados estruturados.