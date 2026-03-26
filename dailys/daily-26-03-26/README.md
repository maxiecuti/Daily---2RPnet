# Daily Report - Engenharia de Dados (PySpark)
**Data:** 26/03/2026  
**Contexto:** Módulo 11 - Construção e Configuração de Clusters Spark

---

## O que foi feito ontem?
- Finalização do Módulo 10, com foco em manipulação de DataFrames e Spark SQL.
- Tratamento de exceções de importação no `pyspark.pandas` causadas por incompatibilidade de versões entre Pandas 3.12 e o núcleo do Spark.
- Estabilização do ambiente local através do ajuste de variáveis de ambiente e bibliotecas de suporte como PyArrow.

## O que foi feito hoje?
- **Infraestrutura de Cluster:** Início da configuração de uma arquitetura Master-Slave (Standalone Mode).
- **Configuração do Master:** - Ativação do nó mestre no IP `192.168.56.101`.
    - Customização do arquivo `spark-env.sh` a partir do template original para definir o `SPARK_MASTER_HOST`.
- **Virtualização:** - Processo de clonagem de máquinas virtuais no VirtualBox para criação do nó Worker (Slave1).
    - Configuração de adaptadores de rede em modo Host-only para isolamento do tráfego de dados.
- **Diagnóstico:** Execução de testes de conectividade via terminal utilizando comandos `ip addr` e `ping`.

## Impedimentos e Desafios
- **Falha de Comunicação entre Nós:** Identificado erro de `Destination Host Unreachable` durante a tentativa de conexão do Slave1 (.102) com o Master (.101).
- **Análise Técnica:** O problema aponta para um conflito de endereçamento MAC originado na clonagem da VM ou bloqueio de pacotes ICMP/TCP pelo firewall (`ufw`) do sistema operacional.
- **Ações Corretivas:** Revisão das configurações de rede no VirtualBox, renovação de IDs de hardware (MAC) e verificação das regras de entrada nas portas 7077 e 8080.

## Próximos Passos
- Estabelecer o "handshake" entre Master e Slave para visualização do nó como `ALIVE` no Spark UI.
- Escalonar o cluster com a adição de um segundo Worker.
- Migrar o processamento de DataFrames locais para o ambiente de cluster distribuído.

---
*Status: Em desenvolvimento (Módulo 11)*