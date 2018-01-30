---
UID: NE:fwpsk.FWPS_FIELDS_RPC_UM_
title: FWPS_FIELDS_RPC_UM_
author: windows-driver-content
description: The FWPS_FIELDS_RPC_UM enumeration type specifies the data field identifiers for the FWPS_LAYER_RPC_UM run-time filtering layer.
old-location: netvista\fwps_fields_rpc_um.htm
old-project: netvista
ms.assetid: 7f493a14-174f-4101-8c08-069dbe9ec3e7
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: fwpsk/FWPS_FIELD_RPC_UM_REMOTE_USER_TOKEN, fwpsk/FWPS_FIELD_RPC_UM_DCOM_APP_ID, fwpsk/FWPS_FIELD_RPC_UM_AUTH_TYPE, FWPS_FIELD_RPC_UM_IMAGE_NAME, fwpsk/FWPS_FIELD_RPC_UM_IMAGE_NAME, fwpsk/FWPS_FIELD_RPC_UM_LOCAL_ADDR_V4, FWPS_FIELD_RPC_UM_SEC_KEY_SIZE, fwpsk/FWPS_FIELD_RPC_UM_REMOTE_ADDR_V6, FWPS_FIELDS_RPC_UM_, fwpsk/FWPS_FIELD_RPC_UM_MAX, FWPS_FIELD_RPC_UM_IF_VERSION, FWPS_FIELDS_RPC_UM enumeration [Network Drivers Starting with Windows Vista], fwpsk/FWPS_FIELD_RPC_UM_PROTOCOL, wfp_ref_5_const_3_data_fields_8dbe4a13-7ea4-4e12-a880-ffbaf3a533ed.xml, fwpsk/FWPS_FIELD_RPC_UM_IF_UUID, FWPS_FIELD_RPC_UM_REMOTE_USER_TOKEN, FWPS_FIELD_RPC_UM_AUTH_LEVEL, fwpsk/FWPS_FIELD_RPC_UM_IF_VERSION, FWPS_FIELD_RPC_UM_REMOTE_ADDR_V4, FWPS_FIELDS_RPC_UM, fwpsk/FWPS_FIELD_RPC_UM_AUTH_LEVEL, FWPS_FIELD_RPC_UM_IF_UUID, FWPS_FIELD_RPC_UM_AUTH_TYPE, FWPS_FIELD_RPC_UM_PROTOCOL, FWPS_FIELD_RPC_UM_IF_FLAG, fwpsk/FWPS_FIELD_RPC_UM_SEC_ENCRYPT_ALGORITHM, FWPS_FIELD_RPC_UM_REMOTE_ADDR_V6, fwpsk/FWPS_FIELD_RPC_UM_PIPE, FWPS_FIELD_RPC_UM_DCOM_APP_ID, FWPS_FIELD_RPC_UM_LOCAL_ADDR_V4, fwpsk/FWPS_FIELD_RPC_UM_LOCAL_PORT, FWPS_FIELD_RPC_UM_PIPE, FWPS_FIELD_RPC_UM_SEC_ENCRYPT_ALGORITHM, FWPS_FIELD_RPC_UM_LOCAL_PORT, netvista.fwps_fields_rpc_um, fwpsk/FWPS_FIELDS_RPC_UM, FWPS_FIELD_RPC_UM_MAX, FWPS_FIELD_RPC_UM_LOCAL_ADDR_V6, fwpsk/FWPS_FIELD_RPC_UM_REMOTE_ADDR_V4, fwpsk/FWPS_FIELD_RPC_UM_LOCAL_ADDR_V6, fwpsk/FWPS_FIELD_RPC_UM_IF_FLAG, fwpsk/FWPS_FIELD_RPC_UM_SEC_KEY_SIZE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: fwpsk.h
req.include-header: Fwpsk.h
req.target-type: Windows
req.target-min-winverclnt: Supported starting with Windows Vista.
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
-	FWPS_FIELDS_RPC_UM
product: Windows
targetos: Windows
req.typenames: FWPS_FIELDS_RPC_UM
---

# FWPS_FIELDS_RPC_UM_ enumeration


## -description


The FWPS_FIELDS_RPC_UM enumeration type specifies the data field identifiers for the
  FWPS_LAYER_RPC_UM 
  <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa366492">run-time filtering layer</a>.


## -syntax


````
typedef enum FWPS_FIELDS_RPC_UM_ { 
  FWPS_FIELD_RPC_UM_REMOTE_USER_TOKEN,
  FWPS_FIELD_RPC_UM_IF_UUID,
  FWPS_FIELD_RPC_UM_IF_VERSION,
  FWPS_FIELD_RPC_UM_IF_FLAG,
  FWPS_FIELD_RPC_UM_DCOM_APP_ID,
  FWPS_FIELD_RPC_UM_IMAGE_NAME,
  FWPS_FIELD_RPC_UM_PROTOCOL,
  FWPS_FIELD_RPC_UM_AUTH_TYPE,
  FWPS_FIELD_RPC_UM_AUTH_LEVEL,
  FWPS_FIELD_RPC_UM_SEC_ENCRYPT_ALGORITHM,
  FWPS_FIELD_RPC_UM_SEC_KEY_SIZE,
  FWPS_FIELD_RPC_UM_LOCAL_ADDR_V4,
  FWPS_FIELD_RPC_UM_LOCAL_ADDR_V6,
  FWPS_FIELD_RPC_UM_LOCAL_PORT,
  FWPS_FIELD_RPC_UM_PIPE,
  FWPS_FIELD_RPC_UM_REMOTE_ADDR_V4,
  FWPS_FIELD_RPC_UM_REMOTE_ADDR_V6,
  FWPS_FIELD_RPC_UM_MAX
} FWPS_FIELDS_RPC_UM;
````


## -enum-fields




### -field FWPS_FIELD_RPC_UM_REMOTE_USER_TOKEN

The identification of the remote user.


### -field FWPS_FIELD_RPC_UM_IF_UUID

The UUID of the RPC interface.


### -field FWPS_FIELD_RPC_UM_IF_VERSION

The version of the RPC interface.


### -field FWPS_FIELD_RPC_UM_IF_FLAG

Reserved for internal use.


### -field FWPS_FIELD_RPC_UM_DCOM_APP_ID

The identification of the COM application.


### -field FWPS_FIELD_RPC_UM_IMAGE_NAME

The name of the application.


### -field FWPS_FIELD_RPC_UM_PROTOCOL



####  The possible condition values are:



#### RPC_PROTSEQ_TCP



#### RPC_PROTSEQ_HTTP



#### RPC_PROTSEQ_NMP



### -field FWPS_FIELD_RPC_UM_AUTH_TYPE

The authentication service type. For more information about authentication service types, see
     Authentication-Service Constants in the RPC section of the Microsoft Windows SDK documentation.


### -field FWPS_FIELD_RPC_UM_AUTH_LEVEL

The authentication service level. For more information about authentication service levels, see
     Authentication-Service Constants in the RPC section of the Windows SDK documentation.


### -field FWPS_FIELD_RPC_UM_SEC_ENCRYPT_ALGORITHM

The certificate-based security service provider interface (SSPI) encryption algorithm.


### -field FWPS_FIELD_RPC_UM_SEC_KEY_SIZE

The certificate-based SSPI encryption key size.


### -field FWPS_FIELD_RPC_UM_LOCAL_ADDR_V4

The local IPv4 address.


### -field FWPS_FIELD_RPC_UM_LOCAL_ADDR_V6

The local IPv6 address.


### -field FWPS_FIELD_RPC_UM_LOCAL_PORT

The local transport protocol port number.


### -field FWPS_FIELD_RPC_UM_PIPE

The name of the remote named pipe.


### -field FWPS_FIELD_RPC_UM_REMOTE_ADDR_V4

The remote IPv4 address.


### -field FWPS_FIELD_RPC_UM_REMOTE_ADDR_V6

The remote IPv6 address. The IPv6 address of the RPC client.


### -field FWPS_FIELD_RPC_UM_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS
     header files and binaries.
