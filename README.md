#### (Portuguese version below)

# Churn Prediction Project - Interconnect

## Description
This project was developed as part of a final sprint to predict customer churn for the telecommunications provider Interconnect. The task involved analyzing customer personal data, plans, and contracts to identify churn patterns and create a machine learning model. The goal is to provide insights that allow the company to offer promotional codes and special plans to retain at-risk customers. The dataset includes information on contracts, personal data, internet, and phone services.

## Prerequisites
To run this project, you will need the following libraries and tools:
- Python 3.8 or higher
- Libraries:
  - `pandas` (for data manipulation)
  - `numpy` (for numerical computations)
  - `matplotlib` and `seaborn` (for data visualization)
  - `scikit-learn` (for modeling)
  - `xgboost` (for the final model)
- Jupyter Notebook (to run the code)

## Usage

Open the `Interconnect.ipynb` file in Jupyter Notebook.

Run all cells in sequence to load the data, perform exploratory analysis, create features, and train the model.

The results, including charts and the AUC-ROC score, will be displayed in the cell outputs.

The final report is in the last cell, summarizing the steps and conclusions.

## Results

### Exploratory Analysis

We identified that new customers (contract duration < 100 days), with *Month-to-month* contracts and high `monthly_charges`, are more likely to churn. Customers with more services (average of 2–3) and a lower average ticket (~23) tend to have lower churn rates.

### Final Model

We used an `XGBoost Classifier` with `scale_pos_weight` adjusted for imbalance (~2.77), achieving an **AUC-ROC of 0.9286**. Features such as `contract_duration`, `num_services`, and `avg_ticket_per_service` were key.

### Conclusion

We recommend offering promotional codes, free streaming packages, or annual/biennial plans with discounts during the first 100 days, prioritizing customers with fewer services or high cost per service.

# Contributions

- **Author:** Thiago Zanin - thiagozanin.tz@gmail.com

Contributions are welcome! To suggest improvements or report bugs, open an *issue* in the repository or submit a *pull request* with proposed changes.


_____________________________________________________________________
_____________________________________________________________________
_____________________________________________________________________
_____________________________________________________________________

Versão em português

# Projeto de Previsão de Churn - Interconnect

## Descrição
Este projeto foi desenvolvido como parte de um sprint final para prever a rotatividade (churn) de clientes da operadora de comunicações Interconnect. A tarefa envolveu a análise de dados pessoais, planos e contratos de clientes para identificar padrões de churn e criar um modelo de machine learning. O objetivo é fornecer insights que permitam à empresa oferecer códigos promocionais e planos especiais para reter clientes em risco. O dataset inclui informações de contratos, dados pessoais, serviços de internet e telefonia.

## Pré-requisitos
Para executar este projeto, você precisará das seguintes bibliotecas e ferramentas:
- Python 3.8 ou superior
- Bibliotecas:
  - `pandas` (para manipulação de dados)
  - `numpy` (para cálculos numéricos)
  - `matplotlib` e `seaborn` (para visualização de dados)
  - `scikit-learn` (para modelagem)
  - `xgboost` (para o modelo final)
- Jupyter Notebook (para rodar o código)

## Uso

Abra o arquivo `Interconnect.ipynb` no Jupyter Notebook.

Execute todas as células em sequência para carregar os dados, realizar a análise exploratória, criar features e treinar o modelo.

Os resultados, incluindo gráficos e a pontuação AUC-ROC, serão exibidos nas saídas das células.

O relatório final está na última célula, resumindo os passos e conclusões.

## Resultados

### Análise Exploratória

Identificamos que clientes novos (duração de contrato < 100 dias), com contratos *Month-to-month* e `monthly_charges` altos são mais propensos ao churn. Clientes com mais serviços (média de 2-3) e ticket médio baixo (~23) tendem a ter menor rotatividade.

### Modelo Final

Utilizamos um `XGBoost Classifier` com `scale_pos_weight` ajustado para o desbalanceamento (~2.77), alcançando um **AUC-ROC de 0.9286**. Features como `contract_duration`, `num_services` e `avg_ticket_per_service` foram cruciais.

### Conclusão

Recomenda-se oferecer códigos promocionais, pacotes de streaming grátis ou planos anuais/bienais com descontos nos primeiros 100 dias, priorizando clientes com poucos serviços ou custos altos por serviço.

# Contribuições

- **Autor:** Thiago Zanin - thiagozanin.tz@gmail.com 

Contribuições são bem-vindas! Para sugerir melhorias ou reportar bugs, abra uma *issue* no repositório ou envie um *pull request* com as alterações propostas.
