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
