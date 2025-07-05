# Projeto de Análise de Dados e Machine Learning: Previsão de Preços de Imóveis

A problemática escolhida para este projeto é a previsão de preços de imóveis. Este é um
desafio comum e de grande relevância no mercado imobiliário, tanto para compradores e
vendedores quanto para investidores e instituições financeiras. A capacidade de prever com
precisão o valor de um imóvel pode impactar diretamente decisões de investimento,
estratégias de precificação e avaliação de riscos.

# Coleta de Dados

Para este projeto, utilizamos o dataset público "Housing Prices Dataset" disponível na
plataforma Kaggle. https://www.kaggle.com/datasets/yasserh/housing-prices-dataset

O dataset, originalmente nomeado Housing.csv inclui as seguintes colunas principais, que representam
as características dos imóveis:

- price: Preço de venda do imóvel (variável alvo)
- area: Área do imóvel em metros quadrados
- bedrooms: Número de quartos
- bathrooms: Número de banheiros
- stories: Número de andares
- mainroad: Indica se o imóvel está localizado em uma rua principal (sim/não)
- guestroom: Indica se o imóvel possui um quarto de hóspedes (sim/não)
- basement: Indica se o imóvel possui porão (sim/não)
- hotwaterheating: Indica se o imóvel possui aquecimento de água (sim/não)
- airconditioning: Indica se o imóvel possui ar condicionado (sim/não)
- parking: Número de vagas de estacionamento
- prefarea: Indica se o imóvel está em uma área preferencial (sim/não)
- furnishingstatus: Status de mobiliário do imóvel (mobiliado/semi-mobiliado/não
mobiliado)

# Análise Exploratória de Dados (EDA)

Antes da modelagem, foi realizada uma Análise Exploratória de Dados (EDA) para
compreender a estrutura do dataset, identificar padrões, anomalias e relações entre as
variáveis. As principais etapas da EDA incluíram:

- Verificação de Valores Ausentes: Foi constatado que o dataset não possui valores
ausentes, o que simplifica a etapa de pré-processamento.

- Distribuição da Variável Alvo ( price ): A distribuição dos preços dos imóveis foi
visualizada através de um histograma, revelando a dispersão e a concentração dos
valores. Esta análise é crucial para entender a natureza da variável que estamos
tentando prever.

- Análise de Variáveis Categóricas: Variáveis como mainroad , guestroom , basement ,
hotwaterheating , airconditioning , prefarea e furnishingstatus foram examinadas para
entenentender a contagem de ocorrências de cada categoria. Isso ajuda a identificar a
relevância de cada característica na precificação dos imóveis.

- Relação entre Variáveis Numéricas e a Variável Alvo: Gráficos de dispersão, como
area vs. price , foram utilizados para visualizar a correlação entre as características
numéricas e o preço. Espera-se que áreas maiores, por exemplo, estejam associadas a
preços mais altos.

- Matriz de Correlação: Uma matriz de correlação foi gerada para identificar a força e a
direção das relações lineares entre todas as variáveis numéricas. Isso auxilia na seleção
de features e na compreensão de multicolinearidade.

# Construção e Avaliação do Modelo

Para a previsão dos preços dos imóveis, foi escolhido o modelo de Regressão Linear. Este é
um modelo simples, mas eficaz, para problemas de regressão, e serve como um bom ponto
de partida para demonstrar o processo de modelagem. O dataset foi dividido em conjuntos
de treino (80%) e teste (20%) para avaliar a capacidade de generalização do modelo em
dados não vistos.

Após o treinamento do modelo com os dados de treino, foram realizadas previsões no
conjunto de teste. A performance do modelo foi avaliada utilizando as seguintes métricas:

- Mean Squared Error (MSE): Mede a média dos quadrados dos erros entre os valores
previstos e os valores reais. Um MSE menor indica um modelo com melhor
desempenho.

- R-squared (R2): Indica a proporção da variância na variável dependente que é
previsível a partir das variáveis independentes. Um R2 mais próximo de 1 indica que o
modelo explica uma maior proporção da variância dos preços.
Além das métricas, foram geradas visualizações para comparar os preços reais com os
preços previstos e para analisar a distribuição dos resíduos (diferença entre valores reais e
previstos). Um gráfico de dispersão de Preços Reais vs. Preços Previstos idealmente mostraria
os pontos alinhados em uma diagonal, indicando previsões precisas. A análise dos resíduos
ajuda a identificar vieses ou padrões não capturados pelo modelo.

# Conclusão

Este projeto demonstrou a aplicação de técnicas de análise de dados e machine learning para prever preços de imóveis. O modelo de Regressão Linear apresentou um desempenho razoável, como indicado pelas métricas de avaliação e visualizações. Para melhorias futuras, poderíamos explorar:

- Engenharia de Features: Criar novas variáveis a partir das existentes.
- Outros Modelos: Experimentar modelos mais complexos como Random Forest, Gradient Boosting, ou redes neurais.
- Otimização de Hiperparâmetros: Ajustar os parâmetros do modelo para melhorar o desempenho.
- Validação Cruzada: Utilizar validação cruzada para uma avaliação mais robusta do modelo.

Este trabalho serve como um ponto de partida para projetos mais aprofundados em previsão de preços de imóveis, destacando a importância da análise de dados na tomada de decisões.
