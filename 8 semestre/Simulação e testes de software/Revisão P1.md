## FUNDAMENTOS
>[!justificativa para se testar software]
>Softwares com defeito  causam prejuizo e perda de dados
>Corrigir bugs em produção custam 100X mais para corrigir durante o desenvolvimento
>Testes são o principal método de validação e verificação de qualidade

### Características de qualidade
- Qualidades externas
	- Funcionalidade
	- Confiabilidade
	- Usabilidade
- Qualidades Internas
	- Eficiência
	- Manutenibilidade
	- Portabilidade
> [!Definições importantes]
**Erro**: ação humana que produz um resultado incorreto
**Defeito**: imperfeição no código que pode causar
comportamento incorreto
**Falha**: desvio observável do comportamento esperado
durante a execução
![[./imagens/Cenario_definicoes.png]]

### Níveis de testes
**Unidade**: componentes isolados (funções, métodos,
classes)
**Integração**: interação entre módulos
Sistema: a aplicação completa, de ponta a ponta
**Aceitação**: valida se atende aos requisitos do cliente
### Piramide de testes
![[./imagens/piramide_testes.png]]

### Técnicas de testes
**Caixa-preta**: baseado na especificação, sem olhar o
código
**Caixa-branca**: baseado na estrutura interna do código
**Caixa-cinza**: combina especificação com
conhecimento parcial da estrutura
### Tipos de testes
**Regressão**: garante que mudanças não quebraram o
que já funcionava
**Fumaça**: verificação rápida das funcionalidades
principais
**Sanidade**: confirma que uma correção específica
funciona
**Exploratório**: não-roteirizado, guiado pela experiência
do testador

## Ciclo de vida de testes de software STLC (Software Testing Life Cycle)
> [SDLC] é a sequência de fases que um sistema de software passa, sendo elas:
 Análise $\rightarrow$ Design $\rightarrow$ Implementação $\rightarrow$ Verificação/Validação $\rightarrow$ Manutenção
 
> [STLC] é o conjunto de fases de teste alinhados a fase do SDLC sendo eles:
 Análise de Requisitos $\rightarrow$ Planejamento $\rightarrow$ Design $\rightarrow$ Configuração de Ambiente $\rightarrow$ Execução $\rightarrow$ Encerramento

Cada fase da STLC deve estar sincronizada com a fase correspondente do SDLC
#### Exemplo de STLC:
1. Análise de requisitos:
![[./imagens/analise_requisitos.png]]
2. Planejamento:
![[./imagens/planejamento.png]]
3. Design:
![[./imagens/Design.png]]
4. Configuração de ambiente:
![[./imagens/configuracao_ambiente.png]]
5. Execução:
![[./imagens/execucao.png]]
6. Encerramento:
![[./imagens/Encerramento.png]]

> [!Modelo de processo]
Representação abstrata da squência de fases, atividades e artefatos usada para estruturar e controlar o desenvolvimento e o teste de um sistema.

### Modelos de testes
#### V-Model
- Cada fase de desenvolvimento tem um teste associado
- Forte rastreabilidade
:LiCheck: Vantagens
- Clareza de escopo e responsabilidades
- Detecção precoce de defeitos
:LiX: Desvantagens
- Baixa flexibilidade a mudanças de requisitos
- Custo alto de correções tardias
#### Agile Testing
- Testes integrados ao desenvolvimento iterativo
- teste cedo e sempre
:LiCheck: Vantagens
- Colaboração contínua entre dev, QA e stakeholders
:LiX: Desvantagens
- Exige disciplina comunicação e ambiente de integração contínua e saudável
#### DevOps e Continuous Testing
- Pipeline CI/CD
	- CI - Build e testes automatizados a cada mudança
	- CD - Implantação contínua com portões de qualidade
- Observabilidade: logs, métricas e rastreamento para realimentar os testes
:LiX: Desvantagens
- Exige cultura, infraestrutura e testes em múltiplos níveis (Pirâmide de testes)
#### Comparativo entre os modelos:
| Modelo  | Foco Principal                        | Flexibilidade | Ferramentas típicas                            |
| ------- | ------------------------------------- | ------------- | ---------------------------------------------- |
| V-Model | Qualidade em ambientes regulados      | Baixa         | Documentação formal, Revisões, Rastreabilidade |
| Agile   | Feedback rápido, valor por incremento | Alta          | Jira, TestRail, Cypresss, Selenium             |
| DevOps  | Automação, CI/CD, observabilidade     | Muito alta    | Github Actions, Jenkins, Docker, K8s           |
### Métricas de testes:
- **Cobertura**: Linhas, ramos, mutação
- **Taxa de Sucesso**: % de casos aprovados por execução
- **Densidade de defeitos**: tempo médio de correção
- **Eficiência de detecção**: Defeitos achados em teste vs. em produção
- **Lead time de mudança**: Tempo do commit até o deploy com qualidade
## Plano mestre de Testes e análise de riscos
> [!Definição]
Documento estratégico que define a abordagem geral de testes para um projeto ou produto.

Dividido da seguinte forma:
#### Escopo:
Delimita o que está dentro e fora do esforço de teste:
Funcionalidades, Plataformas e intregrações cobertas
#### Estratégias de Teste:
Define quais níveis e tipos de teste serão priorizados, e em qual ordem
#### Critérios de entrada e saídas:
Condições objetivas que determinam quando uma fase de teste pode começar e quando pode terminar (entrada/saída respectivamente)
#### Cronograma e marcos
Datas e entregas intermediárias que sincronizam o esforço de teste com o restante do projeto. (milestones)
#### Recursos necessários:
Inventário do que a execução dos testes vai consumir (hardware, pessoas, software, licenças)
#### Ambiente de teste:
Infraestrutura isolada onde os testes rodam, o mais próxima possível da produção (ambiente de homologação)
#### Métricas e Relatórios:
Indicadores que mostram o progresso e saúde do esforço de teste ao longo do ciclo.
#### Papéis:
Quem faz oque: testador funcional, testador de integração
#### Competências:
Conhecimentos técnicos e de domínio de negócio exigidos de cada papel
#### Alocação:
Quanto tempo, e em qual fase cada pessoa da equipe está dedicada ao esforço de teste
#### Treinamentos:
Capacitação necessária antes da execução, quando a equipe não domina alguma ferramenta ou domínio 
### Análise de Riscos:
#### Evento:
Oque pode ocorrer tem sempre uma causa e um efeito associados
#### Probabilidade:
chance estimada de o evento realmente ocorrer.
#### Impacto:
Tamanho do efeito sobre o projeto, caso o evento ocorra.
#### Exposição ao risco:
Pobabilidade $\times$ impacto: combina os dois num único valor comparável entre riscos diferentes.
![[./imagens/Tabela_riscos.png]]
#### Riscos técnicos:
Risco que vem com complexidade da solução, de dependência externas ou de tecnologia pouco madura.
#### Riscos de Cronograma:
Risco que vem de atrasos acumulados em fases anteriores ou de estimativas otimistas demais.
#### Riscos de Recursos:
Risco que vem de faltar gente qualificada, ou de perder gente da equipe no meio do ciclo de desenvolvimento.
#### Riscos de Qualidade:
Risco que vem de requisitos ambíguos ou de cobertura de teste insuficiente para o que está sendo entregue.
### Análise Qualitativa e quantitativa de riscos
Qualitativa 
- Probabilidade (alta/ média/ baixa)
- Impacto: (alto/ médio / baixo)
- matrix de risco: cruza os dois para priorizar
Quantitativa
- Valores numéricos (%, R$)
- Valor esperado : $\sum$ (Probabilidade $\times$ Impacto)
- Permite comparar riscos entre si
![[./imagens/Matriz_riscos.png]]
## Técnicas de testes:
### Teste caixa-preta
Teste baseado na especificação do sistema, foca no comportamento externo
Aplicado em:
- Requisitos funcionais
- APIs
- Teste de aceitação
### Classe de equivalência
 O domínio é dividido em partições onde todos os elementos devem se comportar de maneira equivalente
 - Classe válida: entrada aceita, comportamento normal
 - Classe inválida: entrada rejeitada, erro tratado
### Análise de valor-limite
os defeitos se concentram nas fronteiras de uma classe de equivalência, por exemplo, para um intervalo válido $[A, B]$ testar os seis valores ao redor das duas fronteiras
![[./imagens/fronteiras_valor-limite.png]]
### Tabela de decisão
Agregam classes de equivalência e valor limite para um mapeamento que combine os dois testes:
> [!Estrutura]
**Condições**: as entradas ou critérios avaliados, cada um verdadeiro ou falso
**Ações**: os resultados ou comportamento esperado
**Regras**: cada combinação de condições, associada à ação correspondente

#### Exemplo:
![[./imagens/tabela_decisao.png]]
### Redução da tabela:
Em alguns casos a condição deixa de importar porque outra da decide o resultado:
![[./imagens/decisao_simplificar.png]]
a regra don't care, simplifica as condições redundantes:
![[./imagens/decisao_simplificada.png]]