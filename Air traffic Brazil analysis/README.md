# **Projeto 02 - Air traffic Brazil analysis**

[Notebook do projeto](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/blob/main/Air%20traffic%20Brazil%20analysis/Projeto%202%20AED2.ipynb)

## **Descrição:**
O projeto tem como objetivo a análise do tráfego aério brasileiro e seus aeroportos, onde os relacionados à análise de redes devem ser aplicados.
Onde as análises a serem aplicadas estão listadas a seguir.

## **Estudo sobre assortatividade:**
Para esse estudo calculamos o coeficiente de assortatividade e com resultado desse calculo podemos definir se a rede é assortativa ou não.

`Coeficiente de assortatividade = 0.36728130173582757`

E por se aproximar de 1, é assortativa e foi gerado um gráfico para visualizar as conexões entre os aeroportos.

![Conexões aeroportos](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/blob/main/Air%20traffic%20Brazil%20analysis/imagens/plot01.png)

## **Análise bivariada:**
Essa análise é realizada utilizando a correlação com o grau dos nós em relação a média do grau de seus vizinhos.

**Brasil**

`Grau de assortatividade = -0.2017097172979742`

![Brasil](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/blob/main/Air%20traffic%20Brazil%20analysis/imagens/plotbrasil.png)

**Região Norte**

`Grau de assortatividade = -0.22193985877089423`

![Norte](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/blob/main/Air%20traffic%20Brazil%20analysis/imagens/plotnorte.png)

**Região Nordeste**

`Grau de assortatividade = -0.33375735918340366`

![Nordeste](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/blob/main/Air%20traffic%20Brazil%20analysis/imagens/plotnordeste.png)

**Região Sudeste**

`Grau de assortatividade = -0.3687746079424212`

![Sudeste](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/blob/main/Air%20traffic%20Brazil%20analysis/imagens/plotsudeste.png)

**Região Sul**

`Grau de assortatividade = -0.40181381306857755`

![Sul](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/blob/main/Air%20traffic%20Brazil%20analysis/imagens/plotsul.png)

**Região Centro-Oeste**

`Grau de assortatividade = -0.3542839902086467`

![Centro-Oeste](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/blob/main/Air%20traffic%20Brazil%20analysis/imagens/plotcentro.png)

Tivemos como resultado coesficientes negativos, representando que os aeroportos de uma região devem estar conectados a outros aeroportos de outras regiões.

## **Componentes conectados:**
Para essa análise agrupamos os aeroportos por região e realizamos uma contagem de todos os aeroportos por 
região, após isso realizamos outra contagem dos aeroportos conectados com um mesmo componente. Com essas contagens realizadas podemos
saber a porcentagem de componentes conectados por região.

**Quantidade de aeroportos por região**

![Quantidade de aeroportos por região](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/blob/main/Air%20traffic%20Brazil%20analysis/imagens/contagem01.png)

**Regiões que pertencem a um componente**

![Regiões que pertencem a um componente](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/blob/main/Air%20traffic%20Brazil%20analysis/imagens/contagem02.png)

**Porcentagens de componentes conectados por região**

`Centro-Oeste: 98.88%`

`Nordeste: 100.0%`

`Norte: 98.44%`

`Sudeste: 99.14%`

`Sul: 100.0%`

## **Caminho mais curto:**

Selecionamos aeroportos aleatórios da base de dados para realizar essa análise. Para cada região foi pego um aeroporto e realizada a rota que deveria cumprir. Abaixo temos 
um exemplo do funcionamento do caminho mais curto:

**Aeroportos**

NORTE: SBCJ

SUL: SSUM

NORDESTE: SBFN

CENTRO-OESTE: SWFE

SUDESTE: SNJR

**Rota: SBCJ -> SSUM -> SBFN -> SWFE -> SNJR**

**Caminho mais curto entre as rotas**

SBCJ -> SSUM (SBCJ -> SBCT -> SSUM)

SSUM -> SBFN (SSUM -> SBCT -> SBFN)

SBFN -> SWFE (SBFN -> SBAR -> SBCY -> SWFE)

SWFE -> SNJR (SWFE -> SBCY -> SBBH -> SNJR)

Rota completa: (SBCJ -> SBCT -> SSUM -> SBCT -> SBFN -> SBAR -> SBCY -> SWFE -> SBCY -> SBBH -> SNJR)

Com essas informações foi possível gerar um gráfico contendo os aeroportos e as conexões entre eles.

![Mapeamento de aeroportos](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/blob/main/Air%20traffic%20Brazil%20analysis/imagens/rota.png)

## **Coeficiente de clustering:**

Esse coeficiente mede a aproximidade de um nó ou uma rede de uma topologia estrela. Quando o coeficiente é igual a 1, a rede possui uma
topologia estrela onde todos os elementos estão conectados entre si.

**Brasil**

`Média de agrupamento = 0.623050800236936`

**Centro-Oeste:**

`Média de agrupamento = 0.5979416718387066`

**Nordeste:**

`Média de agrupamento = 0.43807384418290285`

**Norte:**

`Média de agrupamento = 0.6159653188854737`

**Sudeste:**

`Média de agrupamento = 0.6186700538769274`

**Sul:**

`Média de agrupamento = 0.5979416718387066`

## **Referências:**
[Repositório da disciplina](https://github.com/ivanovitchm/datastructure)

[dataset flights brazil](github.com/alvarofpp/dataset-flights-brazil)
