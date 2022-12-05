# Control ID Access Control by HTTP

Para Zabbix 6.0

## Equipamentos Testados:
* ID Access PRO
* ID Block
* ID Box
* ID Flex
* ID Face

## Setup
Import template and define Macros according to your environment.

## Zabbix configuration
No configuration is needed.
### Macros used
|Name|Description|Default|
|----|-----------|-------|
|{$USERNAME}|Device username|admin|
|{$PASSWORD}|Device password|admin|

## Templates Linkados
* ICMP Ping (Zabbix Native)

## Items coletados

### Control ID - ID Access Pro by HTTP
|Group|Name|Description|Type|Key and additional info|
|-----|----|-----------|----|-----------------------|
|System|Control ID ACS: Serial Number|-|Dependent|controlid_acs.serialnumber|
|System|Control ID ACS: System Time|-|Dependent|controlid_acs.systemdata|
|System|Control ID ACS: System Uptime|-|Dependent|controlid_acs.uptime|
|System|Control ID ACS: System Version|-|Dependent|controlid_acs.firmwareversion|
|Network|Control ID ACS: MAC Address|-|Dependent|controlid_acs.mac|
|Network|ICMP loss|-|Simple check|icmppingloss|
|Network|ICMP ping|-|Simple check|icmpping|
|Network|ICMP response time|-|Simple check|icmppingsec|

### Control ID - ID Block by HTTP


### Control ID - ID Box by HTTP
Ainda não foi integrado nenhuma chave especifica

### Control ID - ID Face by HTTP


### Control ID - ID Flex by HTTP



## TODO
Atualmente a coleta está sendo feita por script que realiza login e retorna a session toda vez que é feito uma coleta aos itens RAW
Estudando como alterar usando LLD no login e criação de itens prototypes para os RAW (conforme palestra de Jonathan B. Curty na Zabbix Summit Brazil 2022)

by: Caio Vernaglia Barros