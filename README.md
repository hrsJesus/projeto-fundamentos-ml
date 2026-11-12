# Previsão de rotatividade de clientes

Projeto final da formação **Fundamentos de Machine Learning — ADA, turma 1733**. O objetivo é explorar dados de clientes bancários e comparar modelos para identificar clientes que cancelaram seus serviços (*churn*).

## Conteúdo

- [`projeto.ipynb`](./projeto.ipynb): análise exploratória, preparação dos dados, criação de variáveis, treinamento e avaliação dos modelos.
- [`bank-customer-churn-prediction.csv`](./bank-customer-churn-prediction.csv): base utilizada no projeto.

## Como executar

Abra `projeto.ipynb` no Jupyter Notebook ou JupyterLab e execute as células em ordem. Mantenha o arquivo CSV na mesma pasta do notebook.

Bibliotecas utilizadas: `pandas`, `numpy`, `matplotlib`, `seaborn` e `scikit-learn`.

## Modelos e resultados

O notebook compara uma árvore de decisão com KNN, usando uma divisão estratificada de 80% para treino e 20% para teste. O KNN utiliza dados padronizados; a árvore limita a profundidade e considera o desbalanceamento das classes.

Na execução registrada, a árvore obteve F1 de **0,606** e ROC-AUC de **0,826**; o KNN obteve F1 de **0,444** e ROC-AUC de **0,765**. A escolha de métricas importa: a base tem menos clientes que cancelaram do que clientes que permaneceram, então acurácia isolada não descreve o desempenho completo.

As importâncias das variáveis apresentadas no notebook são específicas à árvore treinada e não indicam causalidade.
