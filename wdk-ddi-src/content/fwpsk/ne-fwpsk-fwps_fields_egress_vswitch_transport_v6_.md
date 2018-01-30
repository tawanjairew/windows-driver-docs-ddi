---
UID: NE:fwpsk.FWPS_FIELDS_EGRESS_VSWITCH_TRANSPORT_V6_
title: FWPS_FIELDS_EGRESS_VSWITCH_TRANSPORT_V6_
author: windows-driver-content
description: The WPS_FIELDS_EGRESS_VSWITCH_TRANSPORT_V6 enumeration type specifies the data field identifiers for the FWPS_LAYER_EGRESS_VSWITCH_TRANSPORT_V6 run-time filtering layer.
old-location: netvista\fwps_fields_egress_vswitch_transport_v6.htm
old-project: netvista
ms.assetid: 4c78a684-85e4-4062-8d52-eaf3b04733bc
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_ID, fwpsk/FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_NETWORK_TYPE, FWPS_FIELDS_EGRESS_VSWITCH_TRANSPORT_V6_, fwpsk/FWPS_FIELDS_EGRESS_VSWITCH_TRANSPORT_V6, FWPS_FIELDS_EGRESS_VSWITCH_TRANSPORT_V6, fwpsk/FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_SOURCE_INTERFACE_ID, FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_SOURCE_INTERFACE_TYPE, FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_IP_SOURCE_ADDRESS, FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_DESTINATION_INTERFACE_ID, fwpsk/FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_DESTINATION_INTERFACE_TYPE, fwpsk/FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_SOURCE_VM_ID, FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_IP_DESTINATION_PORT, fwpsk/FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_ID, FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_TENANT_NETWORK_ID, fwpsk/FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_IP_SOURCE_PORT, FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_MAX, fwpsk/FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_IP_PROTOCOL, FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_IP_PROTOCOL, FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_NETWORK_TYPE, FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_IP_DESTINATION_ADDRESS, FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_IP_SOURCE_PORT, FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_DESTINATION_INTERFACE_TYPE, fwpsk/FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_SOURCE_INTERFACE_TYPE, FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_SOURCE_VM_ID, fwpsk/FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_IP_DESTINATION_ADDRESS, fwpsk/FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_MAX, FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VLAN_ID, netvista.fwps_fields_egress_vswitch_transport_v6, fwpsk/FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_IP_DESTINATION_PORT, fwpsk/FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VLAN_ID, fwpsk/FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_TENANT_NETWORK_ID, fwpsk/FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_FLAGS, FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_DESTINATION_VM_ID, FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_FLAGS, fwpsk/FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_DESTINATION_INTERFACE_ID, FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_SOURCE_INTERFACE_ID, fwpsk/FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_DESTINATION_VM_ID, FWPS_FIELDS_EGRESS_VSWITCH_TRANSPORT_V6 enumeration [Network Drivers Starting with Windows Vista], fwpsk/FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_IP_SOURCE_ADDRESS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: fwpsk.h
req.include-header: Fwpsk.h
req.target-type: Windows
req.target-min-winverclnt: Supported starting with Windows 8.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: "<= DISPATCH_LEVEL"
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	fwpsk.h
apiname:
-	FWPS_FIELDS_EGRESS_VSWITCH_TRANSPORT_V6
product: Windows
targetos: Windows
req.typenames: FWPS_FIELDS_EGRESS_VSWITCH_TRANSPORT_V6
---

# FWPS_FIELDS_EGRESS_VSWITCH_TRANSPORT_V6_ enumeration


## -description


The WPS_FIELDS_EGRESS_VSWITCH_TRANSPORT_V6 enumeration type specifies the data field identifiers for the
  FWPS_LAYER_EGRESS_VSWITCH_TRANSPORT_V6 
  <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa366492">run-time filtering layer</a>.


## -syntax


````
typedef enum FWPS_FIELDS_EGRESS_VSWITCH_TRANSPORT_V4_ { 
  FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_IP_SOURCE_ADDRESS,
  FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_IP_DESTINATION_ADDRESS,
  FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_IP_PROTOCOL,
  FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_IP_SOURCE_PORT,
  FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_IP_DESTINATION_PORT,
  FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VLAN_ID,
  FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_TENANT_NETWORK_ID,
  FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_ID,
  FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_NETWORK_TYPE,
  FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_SOURCE_INTERFACE_ID,
  FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_SOURCE_INTERFACE_TYPE,
  FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_SOURCE_VM_ID,
  FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_DESTINATION_INTERFACE_ID,
  FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_DESTINATION_INTERFACE_TYPE,
  FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_DESTINATION_VM_ID,
  FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_FLAGS,
  FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_MAX
} FWPS_FIELDS_EGRESS_VSWITCH_TRANSPORT_V6;
````


## -enum-fields




### -field FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_IP_SOURCE_ADDRESS

The virtual switch egress IP source address field.


### -field FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_IP_DESTINATION_ADDRESS

The virtual switch egress IP destination address field.


### -field FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_IP_PROTOCOL

The virtual switch egress IP protocol  field.


### -field FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_IP_SOURCE_PORT

The virtual switch egress IP source port field.


### -field FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_IP_DESTINATION_PORT

The virtual switch egress IP destination port  field.


### -field FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VLAN_ID

The virtual switch egress virtual LAN (VLAN) identifier field.


### -field FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_TENANT_NETWORK_ID

The virtual switch egress virtual switch tenant network identifier field.


### -field FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_ID

The virtual switch egress identifier field.


### -field FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_NETWORK_TYPE

The virtual switch egress network type field.


### -field FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_SOURCE_INTERFACE_ID

The virtual switch egress source interface identifier field.


### -field FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_SOURCE_INTERFACE_TYPE

The virtual switch egress source interface type  field.


### -field FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_SOURCE_VM_ID

The virtual switch egress source virtual machine (VM) identifier  field.


### -field FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_DESTINATION_INTERFACE_ID

The virtual switch egress destination interface identifier field.


### -field FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_DESTINATION_INTERFACE_TYPE

The virtual switch egress destination interface type  field.


### -field FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_VSWITCH_DESTINATION_VM_ID

The virtual switch egress destination virtual machine (VM) identifier  field.


### -field FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_L2_FLAGS



### -field FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_COMPARTMENT_ID



### -field FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS header files and binaries.


#### - FWPS_FIELD_EGRESS_VSWITCH_TRANSPORT_V6_FLAGS

The virtual switch egress flags field.
