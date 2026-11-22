## Testes de caixa preta
- Requisitos funcionais:
		Verifica se o sistema faz o que a especificação promete, sem depender de como foi implementado por dentro.
- APIs:
		Testa o contrato de entrada e saída exposto publicamente: é justamente essa fronteira externa que a caixa-preta enxerga.
- Teste de aceitação:
		Valida da perspectiva de quem vai usar o sistema, que também não vê nem precisa ver o código.
## Classes de equivalência
> A ideia é dividir o domínio de entrada em partições, chamadas classes de equivalência, onde todos os elementos de uma mesma classe levam o sistema a se comportar de forma equivalente.

Se um elemento de uma classe revela um defeito, os demais elementos da mesma classe tendem a revelar o mesmo defeito. Basta testar um representante de cada classe.
- Classes válidas: Entrada aceita, comportamento normal esperado.
- Classes inválidas: Entrada rejeitada, erro tratado.
### Identificando classes:
- Conjuntos e enumarações:
		Uma classe válida para cada valor aceito, mais uma inválida agrupando os valores não previstos.
- Condições booleanas:
		Uma classe para o caso verdadeiro, outra para o caso falso.
- Strings:
		Por tamanho: vazia, normal ou acima do limite.
		Por conteúdo: caracteres permitidos ou não.
	
![[./imagens/Pasted image 20261122150015.png]]

| Classes | Intervalo               | Tipo         |
| ------- | ----------------------- | ------------ |
| CE1     | idade < 0               | Inválida     |
| CE2     | 0 $\le$ idade $\le$ 17  | Válida (0%)  |
| CE3     | 18 $\le$ idade $\le$ 64 | Válida (10%) |
| CE4     | idade $\ge$ 65          | Válida (20%) |
| CE5     | não numérico            | Inválida     |
> [!Um representante por classe já cobre a especificação inteira:]
por exemplo, -5 ,10 ,30 ,70  e "abc", cinco casos no lugar de milhares.

### Valores-limite
> Para um intervalo válido [A,B] testar os seis valores ao redor das duas fronteiras:
> A-1, A, A+1, B-1, B, B+1

### Tabela de decisão:
> [!Estrutura:]

- Condições:
		as entradas ou critérios avaliados, cada um verdadeiro ou falso.
- Ações: 
		os resultados ou comportamentos esperados.
- Regras:
		cada combinação de condições, associada à ação correspondente.
![[./imagens/Pasted image 20261122151736.png]]
![[./imagens/Pasted image 20261122151806.png]]
**8 Regras** = $2^3$ combinações, todas relevantes.
```python
@pytest . mark . parametrize ( " idade , renda , score , aprovado " , [
(25 , 4000 , 700 , True ) , (25 , 4000 , 500 , False ) ,
(25 , 2500 , 700 , False ) , (25 , 2500 , 500 , False ) ,
(17 , 4000 , 700 , False ) , (17 , 4000 , 500 , False ) ,
(17 , 2500 , 700 , False ) , (17 , 2500 , 500 , False ) ,
]) # R1 a R8 , na ordem da tabela
def test_aprovar_emprestimo(idade ,renda ,score ,aprovado):
resultado = aprovar_emprestimo(idade ,renda ,score)
assert resultado == aprovado
```

Em algumas regras, uma confição deixa de importar porque outra condição já decide o resultado sozinha. Relembrando a tabela do empréstimo:
![[./imagens/Pasted image 20261122152302.png]]
**Don't care (X)**: o valor dessa condição, verdadeiro ou falso, não muda a ação da regra.
![[./imagens/Pasted image 20261122152401.png]]
**R4**: se idade $\lt$ 18, renda e score não importam. 
**R3**: se renda $\lt$ 3000, score não importa.
**Redução**: 8 regras viram 4.
## Teste combinatorial
- **Teste combinatorial**:
		família de técnicas que escolhe casos de teste para cobrir todas as combinações de valores de $t$ parâmetros, com $t$ menor que o total de parâmetros.
- **Cobertura $t$-a-$t$**:  
		garantia de que toda combinação de valores de quaisquer $t$ parâmetros aparece em algum caso.
- Pairwise:
		o caso $t = 2$
### Pairwise:
> Técnica que seleciona um conjunto de casos que cobre todas as combinações de valores de cada par de parâmetros.

Dez chaves liga/desliga
- Combinações completas: 1024
- Casos *pairwise* da ferramenta: 8
- Mínimo possível: 6 casos
Pares de valores
$\binom{10}{2}$ = 45 pares de chaves, cada um com $2 \times 2 = 4$ combinações: $45 \times 4 = 180$. Cada caso cobre 45, um por par de chaves.

| Caso | C1  | C2  | C3  | C4  | C5  | C6  | C7  | C8  | C9  | C10 |     |
| ---- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1    | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |     |
| 2    | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 0   |     |
| 3    | 1   | 0   | 1   | 0   | 1   | 0   | 1   | 0   | 1   | 1   |     |
| 4    | 0   | 1   | 0   | 1   | 0   | 1   | 0   | 1   | 0   | 1   |     |
| 5    | 0   | 1   | 1   | 0   | 0   | 1   | 1   | 0   | 0   | 1   |     |
| 6    | 1   | 0   | 0   | 1   | 1   | 0   | 0   | 1   | 0   | 1   |     |
| 7    | 0   | 0   | 0   | 1   | 1   | 1   | 1   | 0   | 1   | 1   |     |
| 8    | 1   | 1   | 1   | 0   | 0   | 0   | 0   | 1   | 1   | 1   |     |
> Exemplo simplificado

Suponha 3 parâmetros com 2 valores cada ($2 \times 2 \times 2 = 8$ combinações exaustivas):

- **Auth:** Token, Sessão
    
- **Cache:** Ativo, Inativo
    
- **Compressão:** Gzip, Brotli
    

Existem $\binom{3}{2} \times 4 = 12$ pares ao todo. Com **4 casos de teste** pairwise, todos os 12 pares são cobertos:

| **Caso**  | **Auth** | **Cache** | **Compressão** | **Pares novos cobertos**                             |
| --------- | -------- | --------- | -------------- | ---------------------------------------------------- |
| **CT-01** | Token    | Ativo     | Gzip           | (Token, Ativo), (Token, Gzip), (Ativo, Gzip)         |
| **CT-02** | Token    | Inativo   | Brotli         | (Token, Inativo), (Token, Brotli), (Inativo, Brotli) |
| **CT-03** | Sessão   | Ativo     | Brotli         | (Sessão, Ativo), (Sessão, Brotli), (Ativo, Brotli)   |
| **CT-04** | Sessão   | Inativo   | Gzip           | (Sessão, Inativo), (Sessão, Gzip), (Inativo, Gzip)   |
### Testes baseados em propriedades:
- **Propriedade**: 
		afirmação que vale para todas as entradas válidas de uma função
- **Teste** **baseado** **em** **propriedades**: 
		você declara as propriedades e uma ferramenta gera centenas de entradas para tentar refutá-las
- **Contraexemplo**: 
		entrada que faz uma propriedade falhar
Exemplo:
```python
somar(2,3) == 5
somar(0,5) == 5
somar(-2,2) == 0
```
Propriedades:
Comutativa:
somar(a,b) == somar(b,a)
Identidade:
somar(a,0) == a
Associativa:
somar(somar(a,b),c) == somar(a, somar(b,c))

## Grafos de código
![[./imagens/Pasted image 20261122171822.png]]
![[./imagens/Pasted image 20261122171902.png]]
### Complexidade ciclomática
$$V(G) = E - N + 2 ;\\ V(G) = P +1$$
$E$: arestas
$N$: nós
$P$: nós de decisão com dois ramos.
### Critérios que olham a decisão:
- **Cobertura** **de** **condições (CC)**: 
		Toda condição assume V e F ao menos uma vez. Não garante que decisão assuma V e F.
- **Condição/decisão (CDC)**: 
		CC e C1 juntas.
- **Condições** **multiplas (MCC)**:
		Toda combinação de valores das condições; com $n$ condições, $2^n$ testes.
### Condições/decisão modificadas (MC/DC):
> Critério que exige CDC e o efeito independente de cada condição. Para cada condição, dois testes que diferem só nela e mudam o valor da decisão.