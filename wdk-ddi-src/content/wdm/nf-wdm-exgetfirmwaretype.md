---
UID: NF:wdm.ExGetFirmwareType
title: ExGetFirmwareType function
author: windows-driver-content
description: Returns the system firmware type.
old-location: kernel\exgetfirmwaretype.htm
old-project: kernel
ms.assetid: b8a420d5-7741-4676-9956-dcf996125c6d
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: wdm/ExGetFirmwareType, ExGetFirmwareType function [Kernel-Mode Driver Architecture], ExGetFirmwareType, kernel.exgetfirmwaretype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe (kernel mode)
req.irql: "<=APC_LEVEL"
topictype:
-	APIRef
-	kbSyntax
apitype:
-	DllExport
apilocation:
-	NtosKrnl.exe
apiname:
-	ExGetFirmwareType
product: Windows
targetos: Windows
req.typenames: WORK_QUEUE_TYPE
req.product: Windows 10 or later.
---

# ExGetFirmwareType function


## -description


Returns the system firmware type.


## -syntax


````
FIRMWARE_TYPE ExGetFirmwareType(
   VOID 
);
````


## -parameters





## -returns


Returns a <a href="https://msdn.microsoft.com/c058e20e-11f9-4652-b658-9fd0a43d4224">FIRMWARE_TYPE</a>-type value that indicates the type of firmware.

