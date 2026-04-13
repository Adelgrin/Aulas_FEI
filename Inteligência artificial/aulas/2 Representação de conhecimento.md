# 2 Representação de conhecimento

## Lógica proposicional (LP):

Trabalha com operadores unários e binários, sendo:

operadores unários como(NOT) $\neg$

e operadores binários (AND, OR, Implicação) $\wedge,\vee,\rarr$

trabalha apenas com verdadeiro ou falso

Implicância trabalha como or onde se um é verdadeiro a implicância é verdadeira:

$p = (q \vee r)$

$p \rarr s$

onde **q** ou **r** pode ser verdadeiro implicando em **p**

• Eliminar $\lrarr$ substituindo$\alpha \lrarr \beta$ por$(\alpha \rarr \beta) \wedge (\beta \rarr \alpha)$

• Eliminar $\rarr$ substituindo$\alpha \rarr \beta$por $\neg \alpha \vee \beta$

• Eliminar dupla negação:$\neg \neg \alpha \equiv \alpha$

### Exemplo:

![](imagens/bo-tjP2Z0CDMKgewPScF5nrAIo3_zoQkr1TAKY2bgLI=.png)

## Clausula de Horn:

busca adicionar toda a equação como uma implicância:


![](imagens/L8lZiwrjbVNTewV1cq9X2z8Rv1OXKZ_rfSugFi781UU=.png)

