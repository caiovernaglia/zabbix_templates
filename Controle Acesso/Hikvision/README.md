# Hikvision by http

Para Zabbix 6.0

## Equipamentos Testados:
* DS-K1T671
* DS-K1T341
* DS-K1T343

## Setup
Import template and define Macros according to you environment.

## Zabbix Configuratio
No configuration is needed.
### Macros used
|Name|Description|Default|
|----|-----------|-------|
|{$USER}|Device username|admin|
|{$PASSWORD}|Device password|admin|
|{$HIKVISION_ISAPI_PORT}|ISAPI Port|80|
|{$FACECOUNT_INFO}|Faces count threshold for info trigger|2000|
|{$FACECOUNT_WARN}|Faces count threshold for warning trigger|2500|

## Linked Templates
* ICMP Ping (Zabbix Native)

## Itens coletados
|Group|Name|Description|Type|Key and additional info|
|-----|----|-----------|----|-----------------------|
|System|Hikvision ACS: Device Model|-|Dependent|hikvision_acs.deviceModel|
|System|Hikvision ACS: Device Name|-|Dependent|hikvision_acs.deviceName|
|System|Hikvision ACS: Firmware Version|-|Dependent|hikvision_acs.firmwareversion|
|System|Hikvision ACS: Firmware Build|-|Dependent|hikvision_acs.firmwarebuild|
|System|Hikvision ACS: Serial Number|-|Dependent|hikvision_acs.serialnumber|
|Network|Hikvision ACS: MAC Address|-|Dependent|hikvision_acs.mac|
|Network|ICMP loss|-|Simple check|icmppingloss|
|Network|ICMP ping|-|Simple check|icmpping|
|Network|ICMP response time|-|Simple check|icmppingsec|
|Capacity|Hikvision ACS: Get User Count|-|http_agent|hikvision_acs.get_usercount|
|Capacity|Hikvision ACS: Get Faces Count|-|http_agent|hikvision_acs.get_facecount|
|RAW|Hikvision ACS: Get device info|-|http_agent|hikvision_acs.get_info|

## Triggers
|Name|Description|Expression|
|----|-----------|----------|
|High ICMP ping loss|-|min(/Hikvision access controll by HTTP/icmppingloss,5m)>{$ICMP_LOSS_WARN} and min(/Hikvision access controll by HTTP/icmppingloss,5m)<100|
|High ICMP ping response time|-|avg(/Hikvision access controll by HTTP/icmppingsec,5m)>{$ICMP_RESPONSE_TIME_WARN}|
|Unavailable by ICMP Ping|-|max(/Hikvision access controll by HTTP/icmpping,#3)=0|
|Hikvision ACS: Equipament has been replaced|-|last(/Hikvision access controll by HTTP/hikvision_acs.serialnumber,#1)<>last(/Hikvision access controll by HTTP/hikvision_acs.serialnumber,#2) and length(last(/Hikvision access controll by HTTP/hikvision_acs.serialnumber))>0|
|Hikvision ACS: Firmware version has changed|-|last(/Hikvision access controll by HTTP/hikvision_acs.firmwareversion,#1)<>last(/Hikvision access controll by HTTP/hikvision_acs.firmwareversion,#2) and length(last(/Hikvision access controll by HTTP/hikvision_acs.firmwareversion))>0|
|Hikvision ACS: Firmware build has changed|-|last(/Hikvision access controll by HTTP/hikvision_acs.firmwarebuild,#1)<>last(/Hikvision access controll by HTTP/hikvision_acs.firmwarebuild,#2) and length(last(/Hikvision access controll by HTTP/hikvision_acs.firmwarebuild))>0|
|Hikvision ACS: Faces count greater than {$FACECOUNT_INFO}|-|last(/Hikvision access controll by HTTP/hikvision_acs.get_facecount,#1)>={$FACECOUNT_INFO}|
|Hikvision ACS: Faces count greater than {$FACECOUNT_WARN}|-|last(/Hikvision access controll by HTTP/hikvision_acs.get_facecount,#1)>={$FACECOUNT_WARN}|


## TODO
Implantar coleta de uptime. Não foi encontrado um endpoint na ISAPI para coleta do uptime (testado no DS-K1T343, pode ser que nos demais exista).

Implantar Web scenarios para monitorar interface web. Já houve situação de coleta via ISAPI com sucesso mas o equipamento estava com a interface web travada.

## Observações
Developed by: Caio Vernaglia Barros

Feel free to use and change as needed!