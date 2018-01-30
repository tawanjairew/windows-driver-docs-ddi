---
UID: NS:ntddrilapitypes.RILDIALPARAMS_V2
title: RILDIALPARAMS_V2
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rildialparams_v2.htm
old-project: netvista
ms.assetid: 0a60001b-5fa9-4f25-a92f-3634e2a50e36
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: netvista.rildialparams_v2, RILDIALPARAMS, RILDIALPARAMS_V2 structure [Network Drivers Starting with Windows Vista], *LPRILDIALPARAMS_V2, RILDIALPARAMS_V2, ntddrilapitypes/RILDIALPARAMS_V2, *LPRILDIALPARAMS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntddrilapitypes.h
req.include-header: 
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
-	ntddrilapitypes.h
apiname:
-	RILDIALPARAMS_V2
product: Windows
targetos: Windows
req.typenames: RILDIALPARAMS, *LPRILDIALPARAMS_V2, *LPRILDIALPARAMS, RILDIALPARAMS_V2
---

# RILDIALPARAMS_V2 structure


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.


## -syntax


````
typedef struct _RILDIALPARAMS_V2 {
  DWORD                       dwExecutor;
  RILADDRESS                  raAddress;
  DWORD                       dwOptions;
  RILCALLTYPE                 dwType;
  BOOL                        fHasMediaOffer;
  RILCALLMEDIAOFFERANSWERSET  rcmMediaOffer;
} RILDIALPARAMS_V2, RILDIALPARAMS_V2;
````


## -struct-fields




### -field dwExecutor



### -field raAddress



### -field dwOptions



### -field dwType



### -field fHasMediaOffer



### -field rcmMediaOffer

