# 7 Aprendizado indutivo

## Como desenvolver um data set para decision tree



demonstrado por [Arvore de decisão](file:///workspace/637f30eb-b9d0-4f04-8d4e-54781b057ad2/wJ4bgwTIhN)

## Sistema ID3

consiste em um par de atributo-valor

onde um atrubuto como: temperatura recebe -> {quente|morno|frio}

exemplo de dataset:

![](imagens/fQ0ceSHIVxWwmXY-T0pqGEze8jlFlw68okLUhjI_NAc=.png)

Gerando uma arvore mais ou menos assim:

![](imagens/ZmK-t2C7qqMn72STRFD2j0LdMq4C-KaoU_2BObbJuM8=.png)

## Função de ganho

Definida por:

$$
\sum_{v\in valores(A)}\dfrac{|Sv|}{|S|}Entropia(SV)
$$

Sendo:

* S o treinamento inicial
* A é o atributo a ser classificado
* Sv conjunto de treinamento quando A for igual a v





