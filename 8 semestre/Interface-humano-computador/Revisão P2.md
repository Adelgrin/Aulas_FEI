## Temas da prova:
- tópico 5 (hta/goms/ctt)
- tópico 10 (molic)
- ⁠tópico 13 (avaliação heurística)
- ⁠tópico 14 (usabilidade por observação de usuário)
### Tópico 5
#### HTA
Hta apresenta as operações e funções do sistema proposto
sendo os operadored 
1>2: que apresenta a sequência que as tarefas devem ser propostas
1/2: as opções de tarefas propostas (or)
1+2: todas as tarefas que devem ser concluídas para compor a principal (and)
#### GOMS
goms se apresenta como método, consiste de **objetivos** e **subobjetivos**.
**Primitivas internas de percepção**: cognitiva, tomada de decisão
**Primitivas externas** : operadores (ações concretas que permitem que o usuário execute)
Exeplo de GOMS:
```
GOAL 0: descobrir direção de tráfego de uma rua
- GOAL 1: ecnontrar a rua
  - METHOD 1.A: zoom até o nível de ruas
  - SEL. RULE: a região em que se situa a rua está visível no mapa e o usuário conhece o local
  - METHOD 1.B: fazer busca pelo nome da rua
  - SEL.RULE: o usuário não conhece o local ou o mapa visível está longe de lá
- GOAL 2: identificar a direção do tráfego na rua
```
as goals listam os meus objetivos com o sistema
os methods são as formas de se atingir os objetivos
e as selection rules são as regras de seleção para que a quele metodo se prove o certo para a situação

Detalhamento de método
```
GOAL 0: descobrir direção de tráfego de uma rua
- GOAL 1: ecnontrar a rua
  - METHOD 1.A: zoom até o nível de ruas
  - SEL. RULE: a região em que se situa a rua está visível no mapa e o usuário conhece o local
    - METHOD 1.A.A: zoom utilizando roda do mouse
    - SEL.RULE.: rua não centralizada no mapa, cursosr distante da escala e preferência do usuário
		- OP.1.A.A.1: deslocar o cursor do mouse para a rua desejada
		- OP.1.A.A.2: girar a roda do mouse para a frente
		- OP.1.A.A.3: verificar enquadramento da rua no mapa
    - METHOD 1.A.B: zoom utilizando o menu pop-up
    - SEL.RULE.: rua centralizada no mapa, cursor distante da escala e preferencia do usuário
    - METHOD 1.A.C: zoom utilizando botão de zoom in
    - SEL.RULE.: cursor próximo da escala e preferência do usuário
```
conta com submétodos com suas proprias regras de seleção
no caso de **operadores** a notação volta a utilizar os números, e o operador segue a sequência para executar o método
no exemplo a cima os operadores 1, 2 e 3 seguem esta sequência para executar o metodo
#### goms klm
keying = 0.2s
pointing = 1.1s
homing = 0.4s
press mouse = 0.1s
mentally preparing = 1.2s
#### CTT
permite diferenciar as tarefas do usuário fora do sistema e tarefas interativas, além de tarefas do próprio sistema
é um diagrama horizontal onde verticalmente existe uma derivação de tarefas
Ativação = T1 >> T2
ativação com passagem de informações = T1[]>>T2
escolha = T1 [] T2
tarefas concorrentes = T1 ||| T2
tarefas concorrentes e comunicantes = T1 | [] | T2
tarefas independentes = T1 |=| T2
desativação = T1 [> T2
suspensão/retomada = T1 |> T2
## Molic
consiste em diagramas de processos de conversação (que podem ser considerados telas) no caso estes processos são as interações do usuário com o sistema
### Processos ubíquos
consiste em um tópico de interação que está sempre disponível para o usuário
exemplo é o cabeçalho de aplicativos que em qualquer tela está sempre disponível para a interação do usuário

o processo funciona como uma função da modelagem
exemplo de login:
o diagrama apresenta o efetuar login, e posterior a isso é uma modelagem baseada no ubíquo, dessa forma o usuário não necessita de fazer o login constantemente
## Heuristicas
### Investigação

### Inspeção
alguns métodos são:
- avaliação heuristica
- percurso cognitivo
- método de inspeção semiótica
### Observação


Huristica de nielsen
- visibilidade do estado do sistema
- correspondencia entre o sistema e o mundo real
- controle e liberdade do usuário
- consistência e padronização
- reconhecimento em vez de memória
- flexibilidade e eficiência de uso
- projeto estético e minimalista
- prevenção de erros
- ajude os usuários a reconhecerem, diagnosticarem e se recuperarem de erros
- ajuda e documentação
![[./imagens/Pasted image 20261125175303.png]]
![[./imagens/Pasted image 20261125175620.png]]