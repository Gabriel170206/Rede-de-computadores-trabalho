# Acesso ao Servidor

## Contexto

Neste documento descrevo o problema observado na tentativa de acesso de PC0 a um servidor em outro segmento de rede.

## Comportamento observado

O PC0 tentou executar o comando `ping 192.168.20.100` e recebeu as seguintes respostas:

- `Request timed out.`
- 4 pacotes enviados, 0 recebidos, 4 perdidos (100% loss)

## Causa provável

Com base nas evidências disponíveis, o servidor e o PC0 estão em IPs diferentes e não foi possível estabelecer comunicação direta. A falta de resposta ao ping indica que não há conectividade entre o host que originou a requisição e o endereço de destino `192.168.20.100`.

## Evidências usadas

- Captura de tela do prompt de comando mostrando a tentativa de `ping` para `192.168.20.100` com 100% de perda.
- Arquivo enviado `Cenario Referencia-Redes-iguais.pkt`, que representa o cenário referência de rede usado na atividade.

## Conclusão

O acesso ao servidor não foi possível porque PC0 não conseguiu alcançar o IP do servidor. A falha de ping confirma que, no cenário atual, não existe rota funcional ou os dispositivos estão em redes incompatíveis.
