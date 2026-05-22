Sistemas dependem de concorrência e colaboração, 
Necessário garantir tratamento de:
* concorrência

## Tipos existentes
* baseado em permissão
	* 
* baseado em token
> [!Token Ring]
Recebe o token ultiliza se necessario e repassa
### Vantagens
* fácil
* garantia de segurança
* não ocorre deadlock
### Desvantagens
* o processo que possui token fica dedicado a isso

> [!Baseado em permissão Coordenado]
quando o processo requer usar o recurso ele pede ao cordenador

### Vantagens
* exlusão mutua
* justo : recebeo acesso ao recurso na ordem que fez a requisição
* não sofre startvation
* Fácil de implementar
### Desvantagens
* Coordenador pode parar de funcionar
> [!Baseado em permissão distribuido]
recebe uma mensagem pedindo recurso e:

