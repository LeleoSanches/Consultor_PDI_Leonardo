# Case Consultor PDI em Inteligência Artificial
- - - 
Desenvolvido por: **Leonardo Goshi Sanches**
- - -

## Descrição dos arquivos
    1. dataset.ipynb: Jupyter notebook com objetivo de buscar o dataset IRIS e obter as informações gerais da amostragem
    2. data_exploration.ipynb: Exploração e análise dos dados.
    3. model.ipynb: Modelo de Machine Learning para o problema enunciado.
    4. requirements.txt: Bibliotecas utilizadas no desenvolvimento.
- - - 
# Sobre o dataset IRIS
![iris2](https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Machine+Learning+R/iris-machinelearning.png)

A amostragem IRIS é um exemplo clássico em ciência de dados. Sendo um dataset **supervisionado**, ela contém 150 amostras de **comprimento** e **largura** das **Pétalas** e **Sépalas** de cada flor. São 3 classes balanceadas: **Versicolor**, **Setosa** e **Virginica**.

- - -
# Overview do desenvolvimento

## 1. dataset.ipynb

O dataset utilizado neste projeto é distribuído pelo próprio **sklearn**, isso facilita a manipulação dos arquivos. Também faço uma breve descrição do problema e demonstro como estão formatado os dados. Por fim, este notebook serve como referência na obtenção do dataset, então os jupyters a seguir utilizam ele para manipular os dataframes.

## 2. data_exploration.ipynb

Este notebook tem como objetivo realizar a análise do dataset **Iris**. Primeiramente, faço a análise de outliers e verifico que não há nenhum dado que necessita de correção. Seguindo assim, também procuro as correlações entre as variáveis e para isso realizo algumas plotagens que indicam as características de interesse. Como reforço na busca de correlações, é feito o mapa de calor dos valores.

Seguindo na linha de análise exploratória, faço a busca de estruturas multi-dimencionais no dataset utilizando a técnica das **Curvas de Andrews**. Em um cenário onde o dataset é **não-supervisionado**, esta técnica poderia acusar quantas classes existem.

Para **Análise de Importância das Variáveis** utilizo 3 técnicas principais para o problema: **Chi-square**, **Análise de Variância** e **Análise de informação Mutua**. O Resultado concorda com a literatura, demonstrando uma forte correlação entre as **Pétalas** e uma correlação média no **Comprimento da Sépala**.

Por fim, realizo a **Análise de componentes principais** (**PCA**), também uma técnica **não-supervisionada**, mas que trás ótimos resultados na diminuição de dimensionalidade do problema. Uma vez confirmada a existềncia de correlações entre as variáveis, é válido a utilização desta técnica, pois ela reduz o tamanho do dataset calculando os autovetores. 

## 3. model.ipynb

Após a análise exploratória, é valido a construção de modelos de Machine Learning que façam a classificação das flores em relação a amostragem comentada anteriormente. O dataset **IRIS**, como já citado, é uma amostragem **Supervisionada** e é necessário que a escolha dos modelos comportem esse tipo de dado. Os modelos escolhidos para desenvolvimento foram: **Suport Vector Machine** e **Gaussian Naive Bayes**. Para o treinamento, faço a separação entre o dataset de **train** e **test**, sendo **70%** para este e **30%** para aquele.

Para utilização do modelo Gaussiano, é necessário que os dados tenham uma distribuição do tipo **Normal**. Para isso, faço o cálculo estatístico **Teste de Shapiro** que nos diz se determinado conjunto de dados tem distribuição Gaussiana.

Como métrica dos modelos, faço a escolha de utilizar a **Acurácia** e a **Matriz de Confusão**, pois ambas revelam o quão o modelo se ajustou aos dados. Os modelos escolhidos se ajustaram muito bem ao problema, ambos tiveram resultados iguais na classificação. 

Por fim, o resultado das classificações foram excelentes, sendo o **SVM** uma técnica interessante para casos de classificação onde a amostragem pode ter dependência não-linear e o **GaussianNB** que se ajusta muito bem em problemas da vida real.

- - -

# Deploy do dashboard

Com objetivo de tornar esta análise mais palpável, foi realizado o upload do projeto no **Binder**.

**O Link do projeto**: (Iris)[https://mybinder.org/v2/gh/LeleoSanches/Consultor_PDI_Leonardo/HEAD]

