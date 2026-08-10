## Componentes vs Serviços

| Aspecto     | Componentes                       | Serviços                         |
| ----------- | --------------------------------- | -------------------------------- |
| Escopo      | Interno ao sistema                | (Externo entre sistemas)         |
| Comunicação | Chamada de metodo                 | HTTP, REST, mensagens            |
| Acoplamento | Médio (Dependencia direta)        | Baixo (contratos bem definidos)  |
| Interface   | Interfaces fornecidas/requeridas  | Contratos de serviço (API, JSON) |
| Exemplo     | ClienteComponente.buscarCliente() | GET /clientes{id}                |

## Orquestração
```mermaid
sequenceDiagram 
    autonumber
    actor P as Pedido
    participant O as Orquestrador
    participant MB as Message Broker
    participant PA as Pagamento
    participant PR as Produto

    Note over P, O: Início da Saga do Pedido
    P->>O: 1. CRIAR_PEDIDO_SAGA
    activate O
    
    O->>MB: 2. CRIAR_PAGAMENTO
    activate MB
    MB->>PA: 2.1 - CRIAR_PAGAMENTO
    activate PA
    Note right of PA: Processa Pagamento...
    PA->>MB: 3 - PAGAMENTO_RECEBIDO
    deactivate PA
    MB-->>O: 3.1 - PAGAMENTO_RECEBIDO
    deactivate MB
    
    O->>MB: 4. ATUALIZAR_ESTOQUE
    activate MB
    MB->>PR: 4.1 - ATUALIZAR_ESTOQUE
    activate PR
    Note right of PR: Atualiza Estoque...
    PR->>MB: 5 - PRODUTO_VENDIDO
    deactivate PR
    MB-->>O: 5.1 - PRODUTO_VENDIDO
    deactivate MB
    
    deactivate O
    Note over P, O: Saga Concluída
```

## Coreografia
```mermaid
sequenceDiagram
    participant Broker as Message Broker
    participant Pedido
    participant Pagamento
    participant Produto

    Pedido->>Broker: 1 - PEDIDO_CRIADO
    Broker->>Pagamento: 1.1 - PEDIDO_CRIADO

    Pagamento->>Broker: 2 - PAGAMENTO_RECEBIDO
    Broker->>Produto: 2.1 - PAGAMENTO_RECEBIDO

    Produto->>Broker: 3 - PRODUTO_VENDIDO
    Broker->>Pedido: 3.1 - PRODUTO_VENDIDO
```

## Testing
