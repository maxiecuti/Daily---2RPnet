# Daily Report - 25 de março de 2026

## Atividades Realizadas

### Estudo e Desenvolvimento
* **Início do Módulo 10:** Iniciei os estudos do módulo focado em outros aspectos e integrações do ecossistema de dados.
* **Manipulação de Dados com Pandas:** Prática com a biblioteca Pandas para análise exploratória. Realizei a leitura de arquivos CSV utilizando `read_csv`, configuração de separadores e inspeção inicial de estruturas de dados com `head` e `type`.
* **Configuração de Ambiente Jupyter:** Instalação e execução do Jupyter Notebook em ambiente Linux. Configuração do `findspark` para permitir que o Jupyter localize e utilize o motor do Apache Spark na máquina virtual.
* **Integração Spark e Pandas:** Implementação da lógica de conversão de DataFrames do Pandas para DataFrames do Spark via `createDataFrame`.

## Desafios e Bloqueios

### Problemas Técnicos
* **Gerenciamento de Pacotes no Linux:** Restrições do sistema operacional na instalação de pacotes via `pip` (erro de ambiente gerenciado externamente), resolvido com o uso de flags de exceção no terminal.
* **Dependências de Conversão:** Erro de importação (`PySparkImportError`) durante a conversão de tipos de dados devido à ausência do pacote `PyArrow`, necessário para otimizar a troca de dados entre Python e JVM.
* **Instabilidade da Spark Session:** Erros de comunicação `Py4JNetworkError` reportados devido a processos pendentes e limitações de memória da VM, solucionados após o reinício do Kernel.

## Status do Módulo
* **Progresso:** Módulo 10 iniciado. O conteúdo não foi concluído devido ao tempo dedicado à resolução de problemas de infraestrutura e configuração do ambiente Jupyter/Spark.

## Próximos Passos
* Finalizar os tópicos teóricos e práticos restantes do Módulo 10.
* Realizar testes de performance comparando o processamento em Pandas versus Spark.
