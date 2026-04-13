# 4 Request-reply

## zeromq

**socket em nivel mais baixo, (melhor performance)**

* Pipeline: cliente envia mensagem, workers trabalham em

paralelo na mensagem, um cliente recebe o resultado (dividir

e conquistar)

comunicação mais baixo nivel possivel (comunicação em bytes)

## funcionalidade:

A grande vantagem do request reply é o cliente sempre aguarda um reply para enviar a proxima mensagem, dessa forma a mensagem mantem contexto (na maioria das vezes) e enfilera oq não recebeu reply

## Broker

![](imagens/mdNCA62K550mCsWbiVmIUIh9TbobPL5pPYCgjcoZ4Bs=.png)

funciona como um router para orquestrar clientes vs servidores para evitar concorrência de pacote

