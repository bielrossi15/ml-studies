# Modelos de ML 

## Random Forest
- Feitas de decision trees, arvores que escolhem dados e fazem comparaçõoes dado certos treshold, dado escolhido baseado na variável que vai separar melhor os dados;
- Bagging: bootstrapping the data + using the aggregate to make a decision;
- Out-of-bag error: classificar erroneamente uma saaample do dataset out-of-bag (teste);
#### Passos
- 1 Criar um dataset baseado no atual, bootstrapped dataset (selecionado randomicamente);
- 2 Criar uma decision tree do dataset bootstrapped, mas só considerando um número específico de variáveis para o nó raiz (colunas) para decidir qual vamos usar;
- 3 Nos nós inferiores, selecionamos depois um número X de variáveis para decidir qual usar;
- Faz isso N vezes para criar N decision trees;
- Passa o dado novo pelas N decision trees e escolhe o resultado que possui mais aparições;
#### Preencher valores que faltam
- Primeiro, ver a label e utilizar valores placeholders baseado em outros campos que possuem aquela mesma label (utilizar media, valores que mais aparecem, etc);
- Depois calcular  similaridade com outras colunas, passando por uma random forest criada com esses dados e vendo quais caem nos mesmos nós que a linha que queremos;
- É utilizada uma matriz de proximidades para dizer em quantas decision trees os pares foram considerados similares, e por último dividimos os valores pela quantidade de árvores;
- Para achar os valores que vamos substituir, calculamos a frequencia do valor * peso do valor, sendo peso = qtd de aparições na amtriz de proximidade / soma de proximidades;
- Fazemos novamente até convergir;
#### Matriz de proximidade
- 1 - matriz de proximidade = distância;
- Podemos usar a distância pra criar um heatmap e um MDS plot paara dizer quanto cada linha está ligada com a outra;
