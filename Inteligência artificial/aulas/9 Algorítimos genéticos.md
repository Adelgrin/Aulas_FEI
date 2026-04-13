# 9 algorítimos genéticos

Segue a teoria da evolução de darwin, onde um numero de individuos é exposto a um determinado processo de seleção exemplificado pela imagem:

![](imagens/AYkrvovGtN0hiGNJXkSAE_Rynfjhl5VKuU-VyVkmsCs=.png)

## Definição da população inicial:

Podem ser diversos tipos de dados:

* vetores reais
* cadeia de bits
* vetores de inteiros
* ou outras estruturas

Deve ser obrigatoriamente uma escolha aleatória

## Função de aptidão:

São as limitações do algorítimo para definir a melhor forma de se treinar o modelo para um determinado problema

## Evoluções

composta por 3 tipos

* sexuada (gera um novo individuos a partir de 2 pais)
* assexuada (clona o individuos e normalmente se aplica mutação)
* mutação (gera novos valores aleatórios para a quele individuo)

## Mutações:

* generativa
* destrutiva
* swap
* swap sequence

![](imagens/VljXih_Lcjf46W8RxlAVnjQ-0Vx4-Y88kGRpDRjaQrA=.png)

metodo de eliistismo consiste em adicionar o melhor individuo da geração anterior e adiciono ele com a nova população e assim segue, desta forma o individuo com maior aptidão vai tenter o treinamento das novas populações
