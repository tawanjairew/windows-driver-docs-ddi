---
UID: NS:poscx._POS_CX_ATTRIBUTES
title: _POS_CX_ATTRIBUTES (poscx.h)
description: The POS_CX_ATTRIBUTES structure contains pointers to event callback functions implemented by the client driver.
old-location: pos\pos_cx_attributes.htm
tech.root: pos
ms.assetid: A91B8EAA-2FCB-4468-8CF3-A3C4D9D7E355
ms.date: 02/23/2018
ms.keywords: POS_CX_ATTRIBUTES, POS_CX_ATTRIBUTES structure, PPOS_CX_ATTRIBUTES, PPOS_CX_ATTRIBUTES structure pointer, _POS_CX_ATTRIBUTES, pos.pos_cx_attributes, poscx/POS_CX_ATTRIBUTES, poscx/PPOS_CX_ATTRIBUTES
ms.topic: struct
req.header: poscx.h
req.include-header: Poscx.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- poscx.h
api_name:
- POS_CX_ATTRIBUTES
product:
- Windows
targetos: Windows
req.typenames: POS_CX_ATTRIBUTES
req.product: Windows 10 or later.
---

# _POS_CX_ATTRIBUTES structure


## -description


The POS_CX_ATTRIBUTES structure contains pointers to event callback functions implemented by the client driver.

Use <a href="https://msdn.microsoft.com/library/windows/hardware/mt593141">POS_CX_ATTRIBUTES_INIT</a> to initialize this structure.


## -struct-fields




### -field EvtDeviceOwnershipChange

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/mt593115">EVT_POS_CX_DEVICE_OWNERSHIP_CHANGE</a> callback function.


### -field EvtDeviceRemoteClaim

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/mt593116">EVT_POS_CX_DEVICE_REMOTE_CLAIM</a> callback function.


### -field EvtDeviceRemoteRelease

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/mt593117">EVT_POS_CX_DEVICE_REMOTE_RELEASE</a> callback function.


### -field EvtDeviceRemoteRetain

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/mt593118">EVT_POS_CX_DEVICE_REMOTE_RETAIN</a> callback function.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt593141">POS_CX_ATTRIBUTES_INIT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt593125">PosCxInit</a>
 

 

