# PACKET TRACER: ENXERGANDO AS CAMADAS

## Introdução
Este documento registra a atividade "PACKET TRACER: ENXERGANDO AS CAMADAS". A tarefa foi concluída utilizando o arquivo de cenário `Arquivo-SLIDE6.pkt`, observando a travessia das camadas de rede no Packet Tracer e validando o comportamento dos pacotes durante o teste de conectividade.

## Objetivo da atividade
- Entender como um pacote ICMP é construído e processado nas diferentes camadas do modelo OSI.
- Usar o modo de Simulação do Packet Tracer para visualizar os PDUs em cada etapa.
- Confirmar a conectividade entre hosts e documentar os resultados.

## Requisitos do Slide-6
- Carregar e validar o cenário de rede.
- Executar o teste de ping entre os hosts. 
- Observar e registrar o encapsulamento/desencapsulamento das camadas.
- Documentar os resultados com capturas de tela e evidências.

## Etapa 1: Teste de ping inicial
### Procedimento
1. Abrir o Packet Tracer e carregar o arquivo `Arquivo-SLIDE6.pkt`.
2. Verificar as configurações de IP, máscara e gateway nos hosts envolvidos.
3. No host de origem, executar o comando de ping para o host de destino.
4. Confirmar que o host consegue iniciar a transmissão do pacote ICMP.

### Resultados
- O pacote ICMP foi gerado corretamente na camada de aplicação e transportado para as camadas inferiores.
- A mensagem de ping foi enviada e o teste inicial foi realizado com sucesso.
- Evidência registrada em: `ETAPA1-teste-de-ping.png`.

## Etapa 2: Observação do PDU inbound e outbound
### Procedimento
1. Alternar para o modo de Simulação do Packet Tracer.
2. Aplicar filtro para observar pacotes ICMP ou todo o tráfego relevante.
3. Iniciar a simulação e inspecionar os PDUs nos dispositivos intermediários.
4. Comparar o estado do PDU no momento em que ele entra (Inbound) e sai (Outbound) de um roteador/switch.

### Observações
- Foi possível visualizar o encapsulamento nos campos de cabeçalho das camadas de Enlace, Rede e Transporte.
- O endereço MAC muda entre as interfaces de origem e destino, enquanto o endereço IP permanece constante.
- O TTL do pacote foi decrementado pelo roteador durante o encaminhamento.
- O passo de inspeção inbound/outbound confirmou a lógica de encaminhamento entre segmentos de rede.

### Evidência
- Captura de tela com a inspeção PDU: `ETAPA2-PDU-InBound_and_outBound.png`.

## Etapa 3: Análise do disparo final de ping
### Procedimento
1. Realizar o disparo final do ping após a configuração e a análise das camadas.
2. Observar a resposta do host de destino e o retorno do pacote ao host de origem.
3. Verificar o fluxo de ida e volta das mensagens ICMP.

### Resultados
- O ping final foi concluído com sucesso, confirmando a conectividade entre os hosts.
- A análise do comportamento das camadas mostrou que o pacote foi corretamente desencapsulado no destino e reencapsulado na resposta.
- Evidências registradas em: `ETAPA3-disparoInicial-Ping-.png` e `ETAPA3-disparoFinalping.png`.

## Conclusões
- Todas as etapas do Slide-6 foram concluídas de acordo com os requisitos da atividade.
- A topologia do cenário funcionou corretamente e permitiu observar o caminho do pacote através das camadas do modelo OSI.
- As capturas de tela fornecem evidências do teste de ping e da visualização dos PDUs inbound/outbound.
- A atividade comprovou que o Packet Tracer permite enxergar as camadas de rede e validar o processo de encapsulamento/desencapsulamento.
