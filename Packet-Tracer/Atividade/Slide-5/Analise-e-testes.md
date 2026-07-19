

## Etapa 1: Topologia básica

### Objetivo
Validar a estrutura inicial da rede e garantir que os dispositivos estão conectados conforme o cenário planejado.

### Procedimento realizado
- O ambiente foi carregado no Packet Tracer a partir do arquivo de cenário.
- A topologia básica foi verificada com switches, roteadores e hosts corretamente posicionados.
- As conexões físicas e lógicas foram conferidas para confirmar que a rede possui os segmentos necessários.

### Resultado
A topologia básica está correta e pronta para a auditoria. A imagem `ETAPA1-Topologia-Basica.png` documenta a estrutura da rede antes de aplicar filtros e testes.

---

## Etapa 2: Filtro de protocolo

### Objetivo
Identificar o tráfego relevante para auditoria, filtrando protocolos e analisando pacotes de interesse.

### Procedimento realizado
- Foi configurado o filtro de protocolo no Packet Tracer ou em uma ferramenta de captura para isolar o tráfego desejado.
- Foram monitorados os protocolos usados pela rede para detectar possíveis anomalias ou falhas de configuração.

### Resultado
O filtro permitiu localizar somente os pacotes de auditoria, reduzindo o ruído e facilitando a análise. A imagem `ETAPA2-filtro-protocolo.png` mostra o filtro aplicado e os protocolos identificados.

---

## Etapa 3: Disparo de ping

### Objetivo
Testar a conectividade entre hosts e verificar se os caminhos de rede estão funcionando corretamente.

### Procedimento realizado
- Executou-se o ping entre os hosts principais do cenário.
- O tempo de resposta e a taxa de sucesso foram avaliados.
- Quaisquer pacotes perdidos ou tempos de espera foram documentados.

### Resultado
O disparo de ping confirmou a conectividade entre os dispositivos-chave da rede. Os testes indicaram comunicação estável e ajudaram a validar o encaminhamento dos pacotes. O conteúdo dessa etapa está documentado na pasta `ETAPA3-Disparo-de-Ping`.

---

## Etapa 4: Identificação de endereços MAC

### Objetivo
Auditar os endereços físicos dos dispositivos e associá-los às portas de rede para garantir rastreabilidade.

### Procedimento realizado
- Foram consultadas as tabelas de endereços MAC nos switches e nos hosts.
- As correspondências entre MACs e portas foram verificadas.
- Buscou-se certificar que não havia duplicidade ou inconsistência nas entradas.

### Resultado
A auditoria dos endereços MAC mostrou que os dispositivos estavam identificados corretamente. A imagem `ETAPA4-enderecosMacs.png` registra as tabelas de endereços e as associações de porta.

