# Regressao_linear

1-Comecei importando a base fetch_california_housing e fazendo seus devidos ajustes.
2-Criei as variáveis X e Y para começar a visualizar e separar a base em treino e teste.
3-Seguindo com o tratamento da base, com o #Seaborn fiz um #plot de um gráfico para relacionar todas as colunas da base com a coluna alvo (MedHouseVal) da base. Tudo isso para buscar colunas que tinham uma boa correlação e identificar #outliers.
4-Notei que a coluna AveRooms (número médio de cômodos) continha valores muito acima da média. Então, coloquei seus dados em um #boxplot para averiguar melhor a situação dessa coluna.
5-No diagrama de boxplot de AveRooms, vemos dois pontos muito acima dos demais. Podemos retirar estes da nossa base de dados.
6-Com o método #corr, podemos buscar quais variáveis têm maior correlação com a variável alvo. E colocando esses dados em um heatmap fica mais visual.
7-Verificando se existem valores nulos, se todos os tipos da base estão conforme os dados que iremos trabalhar e se não existem valores duplicados, podemos dar início ao modelo de regressão.
8-Iniciando com a separação dos modelos. Com a biblioteca #Scikit_Learn, vamos importar o train_test_split. Usando as variáveis X e y que criamos, vamos separar nossa base em TREINO e TESTE.
9-Importando da Scikit-Learn o #LinearRegression, começo a criar o modelo de regressão usando apenas a coluna x_train.MedInc para treinar o modelo. Vi que ele apresentou um score de 47% para os dados de treino e teste, mas esse era o melhor?
10-Coloquei o nome das colunas em uma lista e avaliei o score de cada coluna no treino e no teste. E foi provado que a coluna MedInc (média salarial dos moradores) era a que melhor se ajustava aos dados de treino e teste.
11-Em seguida, importei da Scikit-Learn o mean_absolute_error para avaliar o erro médio absoluto e o #mean_squared_error para avaliar o erro médio quadrático.
12-Notei que os erros estavam altos devido à presença de uma única coluna, então resolvi usar a regressão linear múltipla.
13-Fiz uma estrutura de repetição (for) relacionando duas colunas da base entre si e vi qual delas retornava um erro absoluto e quadrático menor. No final, a relação que trouxe o menor erro foi entre MedInc e HouseAge (idade do imóvel).
14-Resolvi então colocar todas as colunas dentro do modelo e os resultados dos erros vieram consideravelmente menores.
15-Veja que nosso erro médio absoluto é menor do que o da regressão linear, mas o erro quadrático médio é maior. Como o erro quadrático médio é mais sensível a outliers, isso pode indicar que há alguns outliers na base que estão diminuindo a desempenho deste modelo.
16-A árvore possui pontos mais dispersos do que a regressão linear, daí o erro quadrático médio maior da árvore comparado ao modelo de regressão linear.
