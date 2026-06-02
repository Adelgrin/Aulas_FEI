## LPS 
> [!Linhas de produto de software]
Consiste em criar um software modular que pode ser vendido ou desenvolvido com modulos diferentes

Estes módulos (features) São obrigatórios, opcionais, alternativos ou alternativos
Exemplo usado no projeto:
![[../Pasted image 20260602144436.png]]
![[../Pasted image 20260602144541.png]]
**Este modelo permite que o usuário/comprador do software utilize apenas as features necessárias**

## DDD
Domain driven design
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