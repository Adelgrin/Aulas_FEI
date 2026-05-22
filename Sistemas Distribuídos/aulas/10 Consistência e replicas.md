> [!Problema]
oque fazer quando a única cópia dos dados ou serviço foi perdido?
**Replicas permitem** 
aumentar robustez com a réplica assumida

## operações conflitantes
leitura e escrita acontecem ao mesmo tempo
escrita e escrita acontecem ao mesmo tempo
garantir consistência pela ordem

## Modelo de consistência centralizado em dados
um data store é uma coleção de storages distribuídos
## Tipos de consistência
* Sequencial
		resultado de qualquer execução é o mesmo que todos os processos fossem executados em ordem
* Linearização
		cada operação parece que foi executada de forma instantânea
* Consistência causal
		Escritas que podem ter relações causais entre processos devem ser vistas na mesma ordem entre processos
