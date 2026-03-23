# Daily Update: Conclusão da Seção 7 - Machine Learning com PySpark

Hoje finalizei um dos módulos mais estratégicos da minha jornada de estudos, consolidando o fluxo completo de um projeto de **Data Science** distribuído com **Spark MLlib**.

## O que foi desenvolvido:

### 1. Engenharia de Atributos (Feature Engineering)
* **Vetorização:** Implementei o `VectorAssembler` para transformar colunas técnicas em vetores densos, preparando o dataset para o processamento matemático.
* **Automação com RFormula:** Evoluí o pipeline utilizando `RFormula` (`Exited ~ .`), automatizando a indexação de variáveis categóricas e a montagem de vetores em um único estágio.

### 2. Modelagem Preditiva
* **Regressão:** Treinei um modelo de **Linear Regression** para predição de performance (HP) e explorei a robustez do **Random Forest Regressor**.
* **Classificação:** Trabalhei em problemas de **Churn Analysis**, implementando algoritmos de **Decision Tree** e **Naive Bayes**.
* **Estratégia de Dados:** Apliquei o particionamento `randomSplit([0.7, 0.3])` para garantir a integridade da validação entre conjuntos de treino e teste.

### 3. Avaliação de Performance
* **Métricas de Regressão:** Utilizei o `RegressionEvaluator` (RMSE) para medir o erro médio das predições.
* **Métricas de Classificação:** Implementei o `BinaryClassificationEvaluator` (AUC-ROC) e o `MulticlassClassificationEvaluator` para validar a precisão dos modelos de classificação.

## Desafios Superados (Linux & Infra)
* **Resolução de Bugs de Ambiente:** Superei erros críticos de `IndentationError` e `TabError` ao editar scripts via terminal na VM Linux, padronizando a sintaxe e garantindo a execução via `spark-submit`.
* **Conectividade:** Configurei drivers JDBC externos para garantir o fluxo de dados entre bancos relacionais e o ambiente de ML.

---

## Próximo Passo
Com os fundamentos de ML consolidados, o próximo foco é a **Seção 8**, onde irei aprofundar na otimização de modelos e na orquestração de **ML Pipelines**.