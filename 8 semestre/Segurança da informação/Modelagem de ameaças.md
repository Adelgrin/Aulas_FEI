> [!Oque é uma ameaça]
Evento ou circunstância em potencial que pode quebrar um ou mais pilares da triade CIA
## Por que modelar ameaças
> não se pode construir um sistema seguro sem conhecer suas ameaças.

- Feita na concepção do sistema (antes de ser desenvolvido),
- Parde da necessidade de mapear oque pode dar errado.
- Adota o ponto de vista de quem ataca (pentest).
## STRIDE: categorizando ameaças
### $S$ Spoofing
>Fingir ser algo ou alguém que não é.
### $T$ Tapering
>Modificar dados, código ou configuração sem autorização.
### $R$ Repudiation
>Negar ter realizado uma ação, sem que o sistema consiga provar o contrário.
### $I$ Information disclosure
>Expor informação a alguém que não deveria ter acesso a ela.
### $D$ Denial of Service
>Impedir ou degradar o acesso de usuários legítimos a um sistema ou serviço.
### $E$ Elevation of privilege
>Obter permissões além das que foram autorizadas.
## Diagramas de fluxos de dados (DFD)
Diagrama que define como os dados são movimentados entre os componentes de um sistema.
>[!Exemplo]
![[Images/Pasted image 20260828195937.png]]
## DREAD: quantificando o risco
> [!Notas de 0 a 10]
$D$ Damage potential
$R$ Reproducibility
$E$ Exploitability
$A$ Affected users
$D$ Discoverability
## Oque fazer com uma ameaça
- Nada
	- Custo de mitigar supera o dano.
- Informar o usuário
	- O sistema não pode eliminar o risco sozinho.
- Remover o recurso
	- Eliminar a funcionalidade que cria a vulnerabilidade.
- Corrigir o problema
	- Mitigar tecnicamente a causa raiz da ameaça.