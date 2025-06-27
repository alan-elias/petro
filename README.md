Modelagem e Previsão da Demanda de Petróleo e Derivados nos EUA
Este projeto explora a modelagem e previsão da demanda de petróleo e seus derivados (gasolina e destilados médios) nos EUA, com foco em técnicas de séries temporais e Machine Learning. Utilizamos dados históricos de demanda (product_supplied_thousandbarrel) fornecidos pela U.S. Energy Information Administration (EIA) e variáveis exógenas como o preço.

## 🚀 Linguagem e Dataviz
- Python via Google Colab
- Power BI

## 📊 Etapas da Modelagem

Coleta e Preparação de Dados:
Carregamento dos dados históricos de demanda e preço.

### Análise Exploratória de Dados (EDA):
Visualização da série temporal para identificar tendências, sazonalidade e anomalias.

## 📈 Modelos Aplicados
Exploramos diferentes classes de modelos para capturar a complexidade da demanda.

1. Holt-Winters (Suavização Exponencial Tripla)
Ajustado aos dados de treino com parâmetros de tendência e sazonalidade (aditiva ou multiplicativa) com foco na captura os padrões internos da série, como o pico de demanda no verão.

Limitação: Não incorpora variáveis exógenas diretamente.

2. SARIMAX (Seasonal AutoRegressive Integrated Moving Average with eXogenous Regressors)
Modelo estatístico robusto para séries temporais que permite a inclusão de variáveis exógenas, como o preço.

Aplicação:

Análise de Estacionariedade: Utilização de testes ADF e gráficos ACF/PACF para determinar as ordens de diferenciação.
O preço foi incluído como um regressor externo para aprimorar a previsão e foco em capturar padrões temporais e sazonais complexos e a influência de fatores externos.

3. XGBoost (Extreme Gradient Boosting)
Aplicação de Machine Learning baseado em árvores que é excelente para capturar relações não lineares e interações complexas entre as features e a variável alvo buscando uma alta precisão na previsão e capacidade de identificar a importância das features para entender os principais impulsionadores da demanda.

## 📊 Avaliação de Desempenho
Para cada modelo, a performance foi avaliada utilizando métricas padrão de regressão em séries temporais:
MAE (Mean Absolute Error): Média dos erros absolutos, que indica o erro médio em unidades da demanda.
RMSE (Root Mean Squared Error): que penaliza de maneira mais rígida erros maiores.

Compação gráfica para observar: Real vs Projetado e compreender ajuste do modelo.

Análise de Resíduos (para SARIMAX): Gráficos de diagnóstico para verificar se os erros do modelo se assemelham a "ruído branco", indicando um bom ajuste.

Próximos Passos e Melhorias Contínuas
Adicionar mais variáveis exógenas como temperatura e indicadores econômicos, além de explorar a combinação de modelos que adicionará valor à tomada de decisão.
