# Daily Update: Engenharia de Dados & Machine Learning - 20/03/2026

## Conclusão da Seção 6: Aplicações Standalone e Automação
Hoje fechei um ciclo importante na minha formação. Deixei de lado o modo interativo do Spark Shell para construir aplicações robustas e reutilizáveis.

### Key Technical Deliverables:
* **Desenvolvimento de Scripts (.py):** Migração total para código persistente, permitindo versionamento e auditoria.
* **Parametrização Dinâmica:** Implementação dos módulos `sys` e `getopt` para captura de argumentos via CLI (`-i` input, `-o` output, `-t` type).
* **Gestão de Dependências:** Dominei a injeção de drivers JDBC (PostgreSQL) e pacotes Maven (MongoDB) via `spark-submit`.
* **Troubleshooting de Ambiente:** Resolução de conflitos de indentação (TabError) e normalização de paths no ecossistema Linux.



---

## Início da Seção 7: Introdução ao Machine Learning (PySpark MLlib)
Subi o nível! Agora o foco é transformar grandes volumes de dados em inteligência preditiva.

### O Desafio do Churn (Taxa de Cancelamento)
Iniciei os estudos teóricos e práticos sobre a predição de Churn, um dos problemas mais críticos para empresas que buscam retenção de clientes.

* **O que é Churn?** Identificação de clientes que estão prestes a abandonar o serviço/produto.
* **Feature Engineering:** Entendimento de como variáveis comportamentais (frequência de uso, reclamações) pesam mais que dados estáticos.
* **Métricas de Performance:** Aprendi por que o **Recall** é a métrica "rei" no Churn: é preferível um falso positivo (tentar reter quem não ia sair) do que um falso negativo (perder um cliente sem notar).



---

## Stack Utilizada hoje:
* **Engine:** Apache Spark 3.x
* **Linguagem:** Python 3.12 (PEP 8 Standards)
* **Banco de Dados:** PostgreSQL (Relacional) & MongoDB (NoSQL)
* **Ambiente:** Linux VM (Ubuntu)

---

## Próximo Passo:
Iniciar a construção do primeiro Pipeline de ML no Spark, focando na vetorização de características e treinamento de um modelo de Classificação para os dados de Churn.