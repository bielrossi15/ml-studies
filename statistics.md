# Folha de cola para conceitos de estatística ML

## Entropia
- A **surpresa** esperada a cada vez que algo ocorrer em um sistema probabilístico, o **valor esperado da surpresa**;
- O valor pra um sistema eh o maior, 1, quando todas as possibilidades do sistema são iguais, então podemos usar para definir a distribuição de um sistema;
- Utilizada primariamente para quantificar a similaridade/diferença de um sistema probabilístico;
- Quanto maior a entropia, maior o valor de entropia do sistema;
- Parte matematica:
  - log(1/p(x)) -> surpresa de algo acontecer, por exemplo, a surpresa de tirar 5 em um dado viciado no número 6;
  - log(1/p(x)) pois eh o inverso da probabilidade e o log escala os valores;
  - (p(x) * quantidade de vezes que vai jogar o dado * surpresa(x) + p(y) * quantidade de vezes que vai jogar o dado * surpresa(y))/qtd de vzs = entropia;
  - cancelam as qtds de vezes
  - SUM(p(x) * log(1/p(x)) -> -SUM(p(x) * log(p(x));
