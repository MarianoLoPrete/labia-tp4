<strong>
CENTRO FEDERAL DE EDUCAÇÃO TECNOLÓGICA DE MINAS GERAIS<br>
ENGENHARIA DE COMPUTAÇÃO<br>
LABORATÓRIO DE INTELIGÊNCIA ARTIFICIAL<br>
Prof. Flávio Cruzeiro
</strong>

# Trabalho Prático 4: Lógica _Fuzzy_, RNA e WEKA
<strong>
por Pedro Felipe Froes e Saulo Antunes
</strong>

## Parte 1: Lógica _Fuzzy_
A lógica _fuzzy_ (ou lógica difusa) é uma lógica que procura modelar o racicíonio implementando conjuntos _fuzzy_, que mapeiam o grau de pertinência de uma variável a esse conjunto. Ao contrário da lógica booleana tradicional, cujos valores de falso e verdadeiro são 0 e 1, respectivamente, na lógica _fuzzy_ uma variável pode assumir qualquer valor escalar entre 0 e 1 através do seu grau de pertinência ao conjunto.

A seguir, foram modelados dois problemas utilizando a lógica _fuzzy_ a fim de exemplificar possíveis aplicações para essa lógica.

### Problema 1: Capturando um Pokémon

Na franquia Pokémon, o processo de captura de um Pokémon envolve principalmente a _catch rate_ do mesmo (uma taxa de captura, única para cada Pokémon) e o quão enfraquecido ele se encontra (quanto menor for seu HP, mais enfraquecido ele está). Combinadas, elas influenciam _capture rate_, ou seja, na chance de capturar ou não o Pokémon.

A _catch rate_ possui intervalo de 0 a 255, com o intervalo de 0 a 100 sendo considerada baixa, 50 a 200 média, e 150 a 255, alta.

<center>
![](fuzzy/pokemon/img/catchrate.png)
###### _Catch rate_ do Pokémon
</center>

Já o HP do Pokémon foi modelado no intervalo de 0 a 100, onde de 0 a 40 o Pokémon está fraco, 20 a 80 representa um estado regular, e de 60 a 100 o Pokémon está saudável.

<center>
![](fuzzy/pokemon/img/hp.png)
###### HP do Pokémon
</center>

A saída _capture rate_ é dada em porcentagem e modelada analisando as duas variáveis de entrada aplicadas no conjunto de regras. De 0 a 30% a chance de captura está mais inclinada para a falha, de 20% a 80% representa uma chance neutra, e acima de 70% há uma chance alta de capturar o Pokémon em questão.

<center>
![](fuzzy/pokemon/img/capturerate.png)
###### _Capture rate_ do Pokémon
</center>

O conjunto de regras que combina as variáveis de entrada e saída é:

* se **_catch rate_ é _high_** e **_HP_ é _weak_**, então **_capture rate_ é _successful_**;
* se **_catch rate_ é _high_** e **_HP_ é _regular_**, então **_capture rate_ é _successful_**;
* se **_catch rate_ é _high_** e **_HP_ é _healthy_**, então **_capture rate_ é _neutral_**;
* se **_catch rate_ é _medium_** e **_HP_ é _weak_**, então **_capture rate_ é _successful_**;
* se **_catch rate_ é _medium_** e **_HP_ é _regular_**, então **_capture rate_ é _neutral_**;
* se **_catch rate_ é _medium_** e **_HP_ é _healthy_**, então **_capture rate_ é _fail_**;
* se **_catch rate_ é _low_** e **_HP_ é _weak_**, então **_capture rate_ é _neutral_**;
* se **_catch rate_ é _low_** e **_HP_ é _regular_**, então **_capture rate_ é _fail_**;
* se **_catch rate_ é _low_** e **_HP_ é _healthy_**, então **_capture rate_ é _fail_**.

<center>
![](fuzzy/pokemon/img/surface.png)
###### Gráfico de superfície
</center>

Além do gráfico de superfície acima, é possível visualizar algumas possíveis situações diferentes para as variáveis de entradas e suas respectivas saídas. Para exemplificar, a entrada do HP foi deixada em 50, enquanto variou-se a _catch rate_ do Pokémon.

<center>
![](fuzzy/pokemon/img/catchrate_low.png)
###### _catch rate_ baixa, HP médio
</center>

<center>
![](fuzzy/pokemon/img/catchrate_medium.png)
###### _catch rate_ média, HP médio
</center>

<center>
![](fuzzy/pokemon/img/catchrate_high.png)
###### _catch rate_ alta, HP médio
</center>

### Problema 2:

## Parte 2: RNA

