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
		resultado de qualquer execução
* Linearização
		cada operação parece que foi execudada de forma intantânea
* Consistência causal
