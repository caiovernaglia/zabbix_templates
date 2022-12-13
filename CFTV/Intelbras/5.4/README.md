# Template para cameras IP da Intelbras

Inserir as credenciais de login do equipamento nas Macros {$USUARIO} e {$SENHA}

Utilizada a documentação de API da Intelbras (em teoria, é para funcinar em qualquer camera IP)

## Equipamentos Testados:
* VIP 1230 B
* VIP 1230 B G2
* VIP 3230 B SL

## Templates Linkados
* ICMP Checks

## Itens coletados
|Application|Name|Type|Key|
|-----------|----|----|---|
|RAW Itens|Get Encode Config (RAW)|HTTP agent|intelbras_cam.get_encode_config|
|RAW Itens|Get Network Config (RAW)|HTTP agent|intelbras_cam.get_network_config|
|System|Channel Title|HTTP agent|intelbras_cam.get_channel_title|
|System|Current Time|HTTP agent|intelbras_cam.get_current_time|
|System|Device Type|HTTP agent|intelbras_cam.get_device_type|
|System|Hardware Version|HTTP agent|intelbras_cam.get_hardware_version|
|System|HTTP API/CGI Version|HTTP agent|intelbras_cam.get_cgi_version|
|System|ONVIF Version|HTTP agent|intelbras_cam.get_onvif_version|
|System|Serial Number|HTTP agent|intelbras_cam.get_serial_no|
|System|Software Version|HTTP agent|intelbras_cam.get_software_version|
|Network|Network DHCP Enable|Dependent Item|intelbras_cam.net_dhcp|
|Network|Network DNS 1|Dependent Item|intelbras_cam.net_dns1|
|Network|Network DNS 2|Dependent Item|intelbras_cam.net_dns2|
|Network|Network Gateway|Dependent Item|intelbras_cam.net_gateway|
|Network|Network IP|Dependent Item|intelbras_cam.net_ip|
|Network|Network MAC Address|Dependent Item|intelbras_cam.net_mac|
|Network|Network Subnet Mask|Dependent Item|intelbras_cam.net_mask|
|Video|Main Stream - Bit Rate|Dependent Item|intelbras_cam.main_bitrate|
|Video|Main Stream - Bit Rate Control|Dependent Item|intelbras_cam.main_brcontrol|
|Video|Main Stream - Compression|Dependent Item|intelbras_cam.main_compression|
|Video|Main Stream - FPS|Dependent Item|intelbras_cam.main_fps|
|Video|Main Stream - Resolution|Dependent Item|intelbras_cam.main_resolution|
|Video|Main Stream - Stream Quality|Dependent Item|intelbras_cam.main_stream_quality|
|Video|Sub Stream - Bit Rate|Dependent Item|intelbras_cam.sub_bitrate|
|Video|Sub Stream - Bit Rate Control|Dependent Item|intelbras_cam.sub_brcontrol|
|Video|Sub Stream - Compression|Dependent Item|intelbras_cam.sub_compression|
|Video|Sub Stream - FPS|Dependent Item|intelbras_cam.sub_fps|
|Video|Sub Stream - Resolution|Dependent Item|intelbras_cam.sub_resolution|
|Video|Sub Stream - Stream Quality|Dependent Item|intelbras_cam.sub_stream_quality|

## TODO


by: Caio Vernaglia Barros
