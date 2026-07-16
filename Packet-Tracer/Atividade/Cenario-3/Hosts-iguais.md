# Hosts com mesmo IP configurado

## Observações dos arquivos enviados

- O arquivo de cenário `Cenario Referencia-Redes-iguais.pkt` foi enviado como referência do ambiente.
- A captura de tela mostra que um host está configurado com IP estático e que o endereço já está sendo usado na rede: `This address is already used in the network.`

## Impacto de dois hosts com o mesmo IP

Com base nas evidências disponíveis, o problema observado no cenário envolve hosts com o mesmo endereço IP. Esse tipo de configuração causa conflitos na rede e afeta o comportamento dos demais dispositivos.

- Quando dois equipamentos compartilham o mesmo IP, os pacotes podem ser entregues ao host incorreto.
- A rede pode apresentar resposta incorreta a ARP, fazendo com que outros hosts jamais encontrem o destino certo ou recebam respostas inesperadas.
- O aviso mostrado na interface (`This address is already used in the network.`) indica que o próprio sistema detecta o conflito e impede a configuração correta.

## Consequências no cenário estudado

- Mesmo que PC0 consiga alcançar `192.168.10.11` em `Envio-de-IP.md`, a presença de um IP duplicado torna a comunicação instável e imprevisível.
- Em um ambiente com IP duplicado, outros hosts podem ter sua conectividade afetada, pois as mensagens ARP e as tabelas de encaminhamento ficam contaminadas.

## Conclusão

Os dados fornecidos mostram um conflito de endereço IP em hosts configurados no mesmo segmento de rede. Esse conflito prejudica a entrega de pacotes e causa problemas de conectividade para os demais dispositivos da rede.
