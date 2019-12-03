# BIG-IP F5 Zabbix template
Zabbix 4.2 template for BIG IP F5 loadbalancer

Forked from https://github.com/blka/zabbix-3.0-BIG-IP-F5 and optimized for Zabbix v4.2. Tested on F5 LTM version 14.1.2

Summary
This template can be used to query values and receive traps via SNMP from a F5 BIG-IP Load balancer. Entities like fans, temperature sensors, power supplies and various Node/Pool/Virtual sever information are discovered by Low-Level discovery.

Value mappings:

	SNMP (Type: sysCmFailoverStatusId):
		0 ⇒ unknown
		1 ⇒ offline
		2 ⇒ forcedOffline
		3 ⇒ standby
		4 ⇒ active

	SNMP (Type: sysCmSyncStatusId):
		0 ⇒ unknown
		1 ⇒ syncing
		2 ⇒ needManualSync
		3 ⇒ inSync
		4 ⇒ syncFailed
		5 ⇒ syncDisconnected
		6 ⇒ standalone
		7 ⇒ awaitingInitialSync
		8 ⇒ incompatibleVersion
		9 ⇒ partialSync

	SNMP (Type: sysChassisFanStatus):
		0 ⇒ bad
		1 ⇒ good
		2 ⇒ notpresent

	SNMP (Type: ltmNodeAddrStatusAvailState):
		0 ⇒ none
		1 ⇒ green
		2 ⇒ yellow
		3 ⇒ red
		4 ⇒ blue
		5 ⇒ gray

	SNMP (Type: ltmNodeAddrStatusEnabledState):
		0 ⇒ none
		1 ⇒ enabled
		2 ⇒ disabled
		3 ⇒ disabledbyparent

	SNMP (Type: ltmPoolStatusAvailState):
		0 ⇒ none
		1 ⇒ green
		2 ⇒ yellow
		3 ⇒ red
		4 ⇒ blue
		5 ⇒ grey

	SNMP (Type: ltmPoolStatusEnabledState):
		0 ⇒ none
		1 ⇒ enabled
		2 ⇒ disabled
		3 ⇒ disabledbyparent

	SNMP (Type: sysChassisPowerSupplyStatus):
		0 ⇒ bad
		1 ⇒ good
		2 ⇒ notpresent

	SNMP (Type: ltmVsStatusAvailState):
		0 ⇒ none
		1 ⇒ green
		2 ⇒ yellow
		3 ⇒ red
		4 ⇒ blue
		5 ⇒ gray

	SNMP (Type: ltmVsStatusEnabledState):
		0 ⇒ none
		1 ⇒ enabled
		2 ⇒ disabled
		3 ⇒ disabledbyparent

enjoy