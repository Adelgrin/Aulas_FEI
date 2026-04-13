# 3 Lógica de primeira ordem

## Modelos de LPO:

Podem ser relações binárias ou enárias.

As funções funcionam da seguinte forma-> Mãe(Andreia,Carlos)

&#x20;   Mãe é a função

&#x20;   Andreia é o predicado da função

&#x20;   Carlos é a dependencia

## Exercicio:

* alguns alunos tiveram aula de frances em 2010
  * $\exists x, Aluno(x) \wedge Aluno(x,Frances) \wedge AnoAula(Frances,2010)$
* todos os alunos que tiveram aula de frances passaram
  * $\forall x, Aluno(y) \wedge Aluno(y,Frances) \Rarr Aprovado(x) $
* Somente um aluno teve aula de grego em 2010
  * $\exists x, Aluno(x) \wedge Aluno(x,Frances) \wedge AnoAula(Frances,2010)$
  * $Aluno(Fulano) \wedge Aula(Fulano,Grego) \wedge AnoAula(Grego,2010)$
* A melhor nota em grego é sempre mais alta que a melhor nota em frances
  * $\exists x \forall y, Nota(y,Frances) \wedge Nota(x,Nota) \wedge Maior(x,y)$

## Transformação para CNF:

![](imagens/59OxY9b-dVCnVAd_LtVcEi4hF1bX9enOPG59_MhYK8g=.png)

## Solução de uma LPO:

![](imagens/S3IU3Wh06gwk4uI8_pZKZmN68hzuXllQaJum6e_wqBw=.png)
