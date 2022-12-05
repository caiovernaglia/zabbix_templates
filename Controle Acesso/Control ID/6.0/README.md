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
|Capacity|Control ID ACS: Get Cards|-|Script|controlid_acs.get_cards|
|Capacity|Control ID ACS: Get Templates|-|Script|controlid_acs.get_templates|
|Capacity|Control ID ACS: Get Users|-|Script|controlid_acs.get_users|
|RAW|Control ID ACS: Get System Info|-|Script|controlid_acs.get_info|

### Control ID - ID Block by HTTP
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
|Capacity|Control ID ACS: Get Cards|-|Script|controlid_acs.get_cards|
|Capacity|Control ID ACS: Get Templates|-|Script|controlid_acs.get_templates|
|Capacity|Control ID ACS: Get Users|-|Script|controlid_acs.get_users|
|Catraca|Control ID ACS: Giros a direita|-|Dependent|controlid_acs.catra_direita|
|Catraca|Control ID ACS: Giros a esquerda|-|Dependent|controlid_acs.catra_esquerda|
|RAW|Control ID ACS: Get System Info|-|Script|controlid_acs.get_info|
|RAW|Control ID ACS: Get Catra Info|-|Script|controlid_acs.get_catrainfo|

### Control ID - ID Box by HTTP
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
|Capacity|Control ID ACS: Get Cards|-|Script|controlid_acs.get_cards|
|Capacity|Control ID ACS: Get Users|-|Script|controlid_acs.get_users|
|RAW|Control ID ACS: Get System Info|-|Script|controlid_acs.get_info|

### Control ID - ID Face by HTTP
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
|Capacity|Control ID ACS: Get Cards|-|Script|controlid_acs.get_cards|
|Capacity|Control ID ACS: Get Faces|-|Script|controlid_acs.get_faces|
|Capacity|Control ID ACS: Get Users|-|Script|controlid_acs.get_users|
|RAW|Control ID ACS: Get System Info|-|Script|controlid_acs.get_info|

### Control ID - ID Flex by HTTP
Pendente de migração do 5.4 para 6.0

### Control ID - ID UHF by HTTP
Ainda não implantado


## TODO
Implantar monitoramento para a ID UHF.
Template para o ID Flex ainda não foi migrado para o Zabbix 6.0 (motivo: sem device em produção). Realizar a migração para disponibilizar para outros usuários.
Melhorar coleta de dados. Atualmente está sendo feito por script consumindo a API dos equipamentos.
Criar triggers de alarme.
Verificar e implantar monitoração do SIP no ID FACE.

## Observações
Developed by: Caio Vernaglia Barros
Feel free to use and change as needed!