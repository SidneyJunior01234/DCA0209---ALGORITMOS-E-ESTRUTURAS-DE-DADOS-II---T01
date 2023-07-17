# Wikipedia_Network_Analysis

# Descrição

Esse projeto tem como finalidade o estudo dos resultados para uma rede.

A rede que deve ser analisada é a gerada utilizando links de referência em uma página qualquer do Wikipedia e as métricas de estudos são:

### Data Processing

Onde é realizado o processamento dos dados com a sujestão do uso de pipeline e resultamos também em um GCC.

### Eccentricity

A Eccentricity é a distância máxima de um Node a todos outros de uma network.

![Eccentricity](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/assets/50020838/38a85ba4-759f-4bc5-89ef-61dd4de8ea75)

### Centrality Distribution: Degree

O plot nos diz que a maioria dos Nodes possuem até 25 Degrees.

![Centrality Distribution: Degree](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/assets/50020838/5bc4a468-5296-4519-96ce-a8126fb91041)

### Centrality Distribution: Probability Dense Function (PDF)

Agora temos uma real visualização de como está distribuindo o Degree da rede, sendo que a maioria dos nós estão concentrados em até 40 vizinhos/conexões.

![Centrality Distribution: Probability Dense Function (PDF)](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/assets/50020838/11798fc0-de4b-492a-a46c-dc3e1d154426)

### Centrality Distribution: Cumaltive Dense Function (CDF)

Podemos ter uma visualização similar considerando uma Cumaltive Dense Function (CDF). A CDF permite ver a porcentagem de Degree na forma acumulada.

![Centrality Distribution: Cumaltive Dense Function (CDF)](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/assets/50020838/216cc57b-374f-4bed-a2f7-32b86506098e)

###  Node Ranking: Degree, Closeness, Betweenness and Eigenvector Centrality:

### Degree Centrality

Degree Centrality é o número de conexões de um Node, a idéia é similar ao Degree. Muda o cálculo.

![Degree Centrality](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/assets/50020838/fee0813f-1753-4817-8f07-bb8f849de158)

### Closeness Centrality

Closeness Centrality é a métrica que informa a distância média de todos os Nodes para um Node.

![Closeness Centrality](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/assets/50020838/a902d1ae-7082-4b3a-8553-7e3bb493f026)

### Betwenness Centrality

O Betwenness Centrality informa a porcentagem de small paths (caminhos curtos) que um Node faz parte. Essa métrica da uma idéia de ponte. Se esse Node está sempre fazendo parte do fluxo da informação.

![Betwenness Centrality](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/assets/50020838/415b0e95-7577-4c8a-b2fe-7fa8e8266aa3)

### Eigenvector Centrality

Eigenvector (Auto-Vetor) Centrality verifica se um Node tem como vizinhos nós importantes. No plot temos uma região do grafo que tem uma importância muito maior para rede.

![Eigenvector Centrality](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/assets/50020838/b3e03fb6-cf9d-404e-bc49-d272a2b1e94a)

### All Together

![All Together](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/assets/50020838/0fe98180-f8bc-4c49-87d6-d6ac2b617f5c)

### Multi Variate Analysis

Na PDF [1,1] mostra uma grande quantidade de Nodes com baixo Betwenness. Poucos Nodes com um valor um pouco superior. Expõe os Hubs da network. Das outras três PDF de Degree [2,2], EigenVector [3,3] e Closeness [4,4], apenas Closeness tem relevância, sendo a maioria dos nós concentrada em cerca de 0.6.

Em [1,2] quando eu tenho um aumento no Degree, também é aumentada o Betwenness. Logo, quando eu atinjo um certo número de Degree ele passa a ser mais importante para o fluxo da network.

Em [1,3] e [1,4] esse formato de aumento de Betwenness é bem semelhante.

Em [2,3] quando eu tenho um crescimento do EigenVector, o Degree acaba crescendo de forma linear. Ou seja, quando mais um Node tem vizinhos importantes, mais vizinhos ele vai tendo.

Já em [2,4], o Degree tem um ganho quando o Closeness supera o valor de 0.5. Após ele atingir um alto valor de proximidade a todos os Nodes, ele passa a ter um ganho de Degree.

Esse mesmo movimento de crescimento visto em [2,4] é repetido para [3,4]. Quando a proximidade aumenta, ele passa a ter muitos vizinhos importantes. Os outros são apenas a mesma representação só que no formado do KDE bivariado.

![Multi Variate Analysis](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/assets/50020838/97221845-9f47-4327-bcea-ca76e83e3e54)

### Core Decomposition

Nosso GCC tem 34 níveis até chegar o núcleo da network. Eles estão concentrados no centro do grafo. Possível visualizar alguns Nodes do K-Shell.

![Core Decomposition](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/assets/50020838/e3612c86-ad93-4301-9b47-ebb882b70047)

### GCC vs K-Core

Como falado anteriormente, o uso de escala Log permite comparar networks com tamanhos diferentes. Na distribuição do 34-Core o núcleo da rede não segue o padrão obtido na GCC. Enquanto a GCC tem o formato de uma Gaussiana (estão concentrados Nodes em torno da mediana apesar de um pouco deslocado a esquerda), a 34-Core está totalmente concentrada em torno da média. Um bom exercício seria descobrir qual foi o K-Core que fez a distribuição ficar similar a GCC.

![GCC vs K-Core](https://github.com/SidneyJunior01234/DCA0209---ALGORITMOS-E-ESTRUTURAS-DE-DADOS-II---T01/assets/50020838/bd985f4b-4f1f-4461-85b0-bc270502c143)

# Wikipedia Network Deploy

Github [Wikipedia Network Deploy](https://github.com/SidneyJunior01234/wikipedia_network_deploy#readme)

# Participantes

[Ana Beatriz Fontes Ferreira](https://github.com/bfontes)

[Sidney Alves dos Santos Junior](https://github.com/SidneyJunior01234)

[Vilson Rodrigues Câmara Neto](https://github.com/vilsonrodrigues)
