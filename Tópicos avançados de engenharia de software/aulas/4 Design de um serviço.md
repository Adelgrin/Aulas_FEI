## Princípios da orientação a serviços
1.  Contrato Padronizado
2.  Reusabilidade
3.  Granularidade
4.  Autonomia
5.  Abstração
6.  Baixo Acoplamento
7.  Visibilidade
8.  Capacidade de Composição
9.  Independência de Estado
10.  Interoperabilidade
---
### Contrato padronizado
### Reusabilidade
Deve ser genérico
* Agnóstico
* Utilitario
* Entidade
* Tarefas (Especícos)
### Granularidade
Escopo funcional (oque o serviço deve fazer)
deve haver coordenação com outros serviços (quanto mais interligação entre serviços maior a **granularidade**)
> [!Nota]
Serviços baseados em crud por exemplo são granularidade média
### Autonomia
um serviço independente que busque funcionar de maineira independente de outros
### Abstração
separar cada ator para suas respectivas permissões
**Exemplo:**
consumidor que deve ter acesso apenas ao contrato, desta forma separado da ACL de implementação (Lógica)
### Baixo acoplamento
poucas interfaces de ligação entre "componentes"
### Visibilidade
Limitação de quem pode e deve ler determinados serviços
### Capacidade de Composição
Baseado nos contratos o serviço deve acompanhar a composição, isto é a definição de com o serviço deve se comportar
### Independência de estado
stateless - não armazena estado, não guarda informação de sessões anteriores
### Interoperabilidade
Capacidade de integração entre sistemas

 ![[../imagens/Pasted image 20260414214710.png]]