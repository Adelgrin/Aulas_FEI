Sistemas dependem de concorrência e colaboração, 
Necessário garantir tratamento de:
* concorrência

## Tipos existentes
* baseado em permissão
	* Centralizados
	* Distribuídos
* baseado em token
> [!Token Ring]
Recebe o token ultiliza se necessario e repassa
### Vantagens
* fácil
* garantia de segurança
* não ocorre deadlock
### Desvantagens
* o processo que possui token fica dedicado a isso

> [!Baseado em permissão Centralizado]
quando o processo requer usar o recurso ele pede ao cordenador
utiliza o relógio lógico de Lamport para ordenar as trocas de mensagens

### Vantagens
* exlusão mutua
* justo : recebe acesso ao recurso na ordem que fez a requisição
* não sofre starvation
* Fácil de implementar
### Desvantagens
* Coordenador pode parar de funcionar

> [!Baseado em permissão distribuido]
Processos trabalham juntos para gerenciar recursos

Processo requere a utilização do recurso a todos os outros processos
para garantir acesso ao recurso ele verifica:
* se não estiver usando o recurso ou não pretende usar,
responde OK para P
* se estiver usando o recurso, ele não responde P, mas
adiciona em uma fila de respostas
* se também quiser acessar o recurso, ele compara o valor
do relógio lógico da mensagem de com o dele. Se o valor
for menor, faz no caso 1, senão faz o caso 2
### Vantagens
* Garantia de evitar deadlock e starvation
### Desvantagens
* com N processos temos N pontos de falha
* Se o processo para de funcionar o requerente nunca sabe se pode usar o recurso