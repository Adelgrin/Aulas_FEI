A ideia consistem em escolher um serviço para sincronizar tempo
este eleição pode ocorrer de diferentes forma
sendo elas:
## Eleição por bullying
* usa o ID (rank) para determinar quem é o coordenador
* o coordenador sempre carrega o maior rank disponível
* quando o coordenador para de funcionar uma nova eleição ocorre
## Eleição em anel
* sempre incrementa o valor anterior na sequecia de ranks
* se alguem não funciona ele é pulado da fila
# Relógio lógico
Consiste em sicronizar o relogio baseado no tempo de delay do envio da mensagem
> [!Este relogio não utiliza tempo real e sim tempo passado]
Exemplo:
![[../imagens/Pasted image 20260522172659.png]]
Neste exemplo ele acrescente +1 no final do tempo anterior 
