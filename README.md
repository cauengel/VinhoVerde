# VinhoVerde

## a. Como foi a definição da sua estratégia de modelagem?
#### Eu decidi por uma abordagem a partir de técnicas de regressão, ao invés de uma classificação de 11 classes (0 à 10) como estratégia para esse problema de aprendizagem supervisionada.
#### Também decidi como estratégia a divisão do problema em 2 partes distintas (um subset para vinhos brancos e um subset para vinhos tintos), a partir dos resultados obtidos pelos dados do EDA (análise exploratória) realizado e da aplicação de testes de hipótese T (teste para média) que embasaram essa subdivisão.
## b. Como foi definida a função de custo utilizada?
#### A função de custo utilizada foi a RMSE (root-mean-square error), pois ela é uma das principais métricas utilizas para modelos de regressão e é consonante com a abordagem proposta.
## c. Qual foi o critério utilizado na seleção do modelo final?
#### O modelo final que utiliza Random Forest foi selecionado porque apresentou o menor valor de RMSE para os dados de vinhos brancos e tintos.
## d. Qual foi o critério utilizado para validação do modelo? Por que escolheu utilizar este método?
#### Para validar o modelo foi realizada a comparação dos resultados das RMSEs obtidas com os modelos de machine learning aplicados em comparação a RMSE obtida a partir de um método simples de controle, no caso, a aplicação da média da variável qualidade como resposta. Eu decidi utilizar este método como baseline pois não dispunha de valores de referência de desempenho para o problema.
## e. Quais evidências você possui de que seu modelo é suficientemente bom?
#### A partir dos resultados obtidos com os modelos aplicados não é possível concluir que o modelo apresenta bons resultados, haja visto que ele obteve performance pouco superior ao critério de validação utilizado, citado acima.
#### Com o intuito de obter um melhor desempenho do modelo, foi realizado um teste adaptando-se os dados para um problema de classificação binária da variável target qualidade. Nesse testes os vinhos com score igual ou superior à 7 foram classificados como bons e os vinhos com score inferior à 7 foram classificados como ruins, ao invés do score de 0 à 10 original. Ao realizar tal adaptação os resultados foram bastante satisfatórios. Tal abordagem não foi incluída no notebook, pois ela extrapolava os limites do desafio proposto e não tinha informação se a mesma seria permitida.  
