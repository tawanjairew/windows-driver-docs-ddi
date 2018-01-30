---
UID: NS:hbapiwmi._SM_GetBindingSupport_IN
title: "_SM_GetBindingSupport_IN"
author: windows-driver-content
description: The SM_GetBindingSupport_IN structure is used to provide input parameters to the SM_GetBindingSupport method.
old-location: storage\sm_getbindingsupport_in.htm
old-project: storage
ms.assetid: c89d86fe-fe8c-48d2-a5c2-7971ea96b7ad
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: SM_GetBindingSupport_IN structure [Storage Devices], hbapiwmi/SM_GetBindingSupport_IN, _SM_GetBindingSupport_IN, structs-Fibre_f13c3a99-7626-4dda-b0f2-8505b7aff3b5.xml, storage.sm_getbindingsupport_in, SM_GetBindingSupport_IN, *PSM_GetBindingSupport_IN, PSM_GetBindingSupport_IN, PSM_GetBindingSupport_IN structure pointer [Storage Devices], hbapiwmi/PSM_GetBindingSupport_IN
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: hbapiwmi.h
req.include-header: Hbapiwmi.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	hbapiwmi.h
apiname:
-	SM_GetBindingSupport_IN
product: Windows
targetos: Windows
req.typenames: "*PSM_GetBindingSupport_IN, SM_GetBindingSupport_IN"
---

# _SM_GetBindingSupport_IN structure


## -description


The SM_GetBindingSupport_IN structure is used to provide input parameters to the SM_GetBindingSupport method.


## -syntax


````
typedef struct _SM_GetBindingSupport_IN {
  UCHAR HbaPortWWN[8];
  UCHAR DomainPortWWN[8];
} SM_GetBindingSupport_IN, *PSM_GetBindingSupport_IN;
````


## -struct-fields




### -field HbaPortWWN

The worldwide name (WWN) of the local port whose events the WMI client will receive.


### -field DomainPortWWN

A worldwide name (WWN) that specifies the SAS domain worldwide name of the local port.


## -remarks


The WMI tool suite generates a declaration of the SM_GetBindingSupport_IN structure in <i>Hbapiwmi.h</i> when it compiles the MS_SMHBA_BindingEntry WMI class.

