

## Cenário 1: Envio de ICMP de PC0 para PC1

### Objetivo
Validar a conectividade IP entre dois hosts na rede.

### Etapas
1. Abrir o Packet Tracer e carregar o cenário de referência.
2. No PC0, abrir o prompt de comando.
3. Executar o comando `ping 192.168.10.11`.
4. Observar a resposta do ping e as estatísticas exibidas.

### Resultados observados
- Comando executado: `ping 192.168.10.11`
- Resposta recebida de `192.168.10.11` com `bytes=32`, `time=4ms` e `TTL=128`
- Total de pacotes: 4 enviados, 4 recebidos, 0 perdidos
- Estatísticas de tempo: mínimo = 4ms, máximo = 11ms, média = 5ms

### Conclusão
A comunicação entre PC0 e PC1 está funcionando corretamente. O ping bem-sucedido indica que a conectividade IP entre os dois dispositivos está estabelecida.

---

## Cenário 2: Acesso ao servidor

### Objetivo
Verificar se PC0 consegue alcançar o servidor remoto na rede.

### Etapas
1. Abrir o cenário no Packet Tracer.
2. No PC0, abrir o prompt de comando.
3. Executar o comando `ping 192.168.20.100`.
4. Analisar as respostas e confirmar se há perda de pacotes.

### Resultados observados
- Resultado do ping: `Request timed out.`
- Total de pacotes: 4 enviados, 0 recebidos, 4 perdidos (100% loss)

### Conclusão
O acesso ao servidor não foi possível. A falha no ping indica que não existe conectividade funcional entre PC0 e o IP `192.168.20.100`, devido à ausência de redes compatíveis.

### Observação
As imagens enviadas devem ser consultadas para acompanhar o teste e verificar o cenário de referência usado na atividade.

---

## Cenário 3: Hosts com mesmo IP configurado

### Objetivo
Identificar o problema de configuração de endereços IP duplicados na rede.

### Etapas
1. Abrir o cenário no Packet Tracer.
2. Checar a configuração de IP dos hosts.
3. Verificar as mensagens de erro exibidas pelo Packet Tracer.

### Resultados observados
- Foi detectado que um host está configurado com um IP já utilizado na rede.
- Mensagem exibida: `This address is already used in the network.`

### Conclusão
Existem hosts com endereço IP duplicado no mesmo segmento de rede. Esse conflito causa falhas de comunicação e instabilidade na entrega de pacotes.

### Impacto
- A conectividade entre dispositivos pode falhar.
- A rede pode se comportar de forma instável.
- O funcionamento geral da rede fica prejudicado.

