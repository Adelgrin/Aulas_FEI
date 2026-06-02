## LPS 
> [!Linhas de produto de software]
Consiste em criar um software modular que pode ser vendido ou desenvolvido com modulos diferentes

Estes módulos (features) São obrigatórios, opcionais, alternativos ou alternativos
Exemplo usado no projeto:
![[../Pasted image 20260602144436.png]]
![[../Pasted image 20260602144541.png]]
**Este modelo permite que o usuário/comprador do software utilize apenas as features necessárias**

## DDD
>[!Domain driven design]
Busca modelar um software com uma modelagem clara

**Modelagem Estratégica**
* Dominios e subdominios
* Bounded context
* Linguagem ubiqua
* Context Map
### Dominios:
Dominios definem a área de negócio para que o software foi desenvolvido
Separado em:
1. Subdominio Core
2. Subdominio Suporte
3. Subdominio Genérico
### Bounded context
Fronteira lógica para simplificar a nomenclatura
Consiste em dividir os contextos para que as nomenclaturas sejam limitadas a quele subdominio, para evitar conflitos e para isso é utilizada a **Linguagem Ubiqua** (linguagem comum entre todas as partes relacionadas ao software)

### Context map
Mapeia as relações entre os bounded context
Define cada um dos contextos definidos, quais são os bounded context, e interliga eles em um fluxograma que demonstra a funcionalidade da quela feature ou microserviço

## Testes
1. Testes unitários
	Verifica o funcionamento de unidades isoladas
2. Teste de integração
	Teste de serviços e sistemas externos(como APIs)
3. Teste de componentes
	Testar funcionalidades completas de um único serviço
4. Testes de controle de serviço
	Verifica a comunicação entre cliente e servidor e as estruturas das request/response
5. Teste end-to-end
	Teste o fluxo completo de um sistema de serviços

**as fases do ciclo de vida de software orientado a serviço funcionam da seguinte forma:**
![[../Pasted image 20260602173847.png]]