# 🚗 Predição de Preços de Carros

Este projeto consiste em um modelo de Machine Learning desenvolvido para prever o preço de veículos com base em suas características técnicas (como potência do motor, dimensões, consumo, etc.).

O objetivo principal é demonstrar o uso de pipelines de dados, seleção automática de features e modelagem preditiva para um problema de regressão.

## 🛠 Tecnologias Utilizadas

* **Python 3**
* **Pandas & Numpy:** Manipulação e análise de dados.
* **Scikit-Learn:** Construção do pipeline, seleção de features e modelo de Machine Learning.
* **Matplotlib/Seaborn:** Visualização de correlações.

## O Pipeline do Projeto

O projeto segue um fluxo estruturado de processamento:

1.  **Análise Exploratória:** Estudo da correlação de Pearson para entender quais variáveis impactam mais o preço (ex: `enginesize`, `curbweight`).
2.  **Feature Selection Inteligente:** Uso do `SelectFromModel` com um *Random Forest* auxiliar para filtrar automaticamente as colunas mais relevantes, descartando ruídos abaixo da mediana de importância.
3.  **Modelagem:** Treinamento de um **Random Forest Regressor** (com 300 árvores) para realizar a predição.
4.  **Tratamento de Dados:** Aplicação de transformação logarítmica (Log Transform) no preço para normalizar a distribuição e reduzir o impacto de outliers (carros de luxo).

## Resultados Obtidos

O modelo foi avaliado com dados de teste (20% do dataset), apresentando as seguintes métricas:

| Métrica | Valor Aprox. | Descrição |
| :--- | :--- | :--- |
| **R² Score** | 0.9584 | Indica alta capacidade explicativa do modelo sobre a variação de preços. |
| **MAE** | $1286.32 | Erro médio absoluto. |
| **RMSE** | $1812.92 | Raiz do erro quadrático médio (penaliza erros maiores). |
| **MAPE** | 0.93% | Erro percentual médio. |

*Obs: A diferença entre o RMSE e o MAE indica a presença de outliers (carros de alto valor) que são naturalmente mais difíceis de prever com exatidão.*

## Como Executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/rafaelprubio/RegressaoPrecoCarros.git
2. Instale as dependências:
   ```bash
   cd RegressaoPrecoCarros
   
   pip install -r requirements.txt
4. Execute o script principal:
   ```bash
   python appstreamlit2.py
