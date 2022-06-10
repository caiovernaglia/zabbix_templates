# Template para equipamentos Control ID

Inserir as credenciais de login do equipamento nas Macros {$USUARIO} e {$SENHA}

Os equipamentos utilizam informações básicas dos equipamentos através do Control ID - Base

As checagens especificas para cada equipamento são definidas no template próprio

## Equipamentos Integrados:
* ID Access PRO
* ID Block
* ID Box
* ID Flex
* ID Face

## Templates Linkados
* ICMP Checks

## Items coletados:
### Control ID - Base by HTTP
|Application|Name|Type|Key|
|-----------|----|----|---|
|Status|ICMP Loss|Simple Check|icmppingloss|
|Status|ICMP Ping Status|Simple Check|icmpping|
|Status|ICMP Response Time|Simple Check|icmppingsec|
|RAW|System Info (RAW)|Script|cid.sysinfo_raw|
|RAW|Load Objects - Users (RAW)|Script|cid.loadobjects_user|
|RAW|Load Objects - Cards (RAW)|Script|cid.loadobjects_cards|
|System|System Serial Number|Dependent Item|cid.system_serial|
|System|System Time|Dependent Item|cid.system_data|
|System|System Uptime|Dependent Item|cid.system_uptime|
|System|System Version|Dependent Item|cid.system_version|
|Network|Network IP|Dependent Item|cid.net_ip|
|Network|Network Subnet Mask|Dependent Item|cid.net_mask|
|Network|Network Gateway|Dependent Item|cid.net_gateway|
|Network|Network MAC Address|Dependent Item|cid.net_mac|
|Capacity|Quantidade Users|Dependent Item|cid.qtde_users|
|Capacity|Quantidade Cards|Dependent Item|cid.qte_cards|

### Control ID - ID Access Pro by HTTP
|Application|Name|Type|Key|
|-----------|----|----|---|
|RAW|Load Objects - Templates (RAW)|Script|cid.loadobjects_templates|
|Capacity|Quantidade Templates|Dependent Item|cid.qtde_templates|

### Control ID - ID Block by HTTP
|Application|Name|Type|Key|
|-----------|----|----|---|
|RAW|Load Objects - Templates (RAW)|Script|cid.loadobjects_templates|
|RAW|Load Objects - Catra Info (RAW)|Script|cid.loadobjects_catrainfo|
|Capacity|Quantidade Templates|Dependent Item|cid.qtde_templates|
|Catraca|Giros a Direita|Dependent Item|cid.catrainfo_rightturn|
|Catraca|Giros a Esquerda|Dependent Item|cid.catrainfo_leftturn|

### Control ID - ID Box by HTTP
Ainda não foi integrado nenhuma chave especifica

### Control ID - ID Face by HTTP
|Application|Name|Type|Key|
|-----------|----|----|---|
|RAW|Load Objects - Faces (RAW)|Script|cid.loadobjects_faces|
|Capacity|Quantidade Faces|Dependent Item|cid.qtde_faces|

### Control ID - ID Flex by HTTP
|Application|Name|Type|Key|
|-----------|----|----|---|
|RAW|Load Objects - Templates (RAW)|Script|cid.loadobjects_templates|
|Capacity|Quantidade Templates|Dependent Item|cid.qtde_templates|


## TODO
Atualmente a coleta está sendo feita por script que realiza login e retorna a session toda vez que é feito uma coleta aos itens RAW
Estudando como alterar usando LLD no login e criação de itens prototypes para os RAW (conforme palestra de Jonathan B. Curty na Zabbix Summit Brazil 2022)

by: Caio Vernaglia Barros