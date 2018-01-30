---
UID: NI:usbioctl.IOCTL_USB_HCD_GET_STATS_1
title: IOCTL_USB_HCD_GET_STATS_1
author: windows-driver-content
description: The IOCTL_USB_HCD_GET_STATS_1 IOCTL has been deprecated. Do not use.
old-location: buses\ioctl_usb_hcd_get_stats_1.htm
old-project: usbref
ms.assetid: 8be34d4d-b2f1-4d34-911a-95ac2e19df87
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: buses.ioctl_usb_hcd_get_stats_1, IOCTL_USB_HCD_GET_STATS_1 control code [Buses], IOCTL_USB_HCD_GET_STATS_1, usbioctl/IOCTL_USB_HCD_GET_STATS_1, usbirp_2817a2bf-23af-43f8-8c50-c945cf2544f0.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: usbioctl.h
req.include-header: Usbioctl.h
req.target-type: Windows
req.target-min-winverclnt: Available on Microsoft Windows Server 2003, Windows XP, and Windows 2000, but it is not available on Windows Vista.
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
-	Usbioctl.h
apiname:
-	IOCTL_USB_HCD_GET_STATS_1
product: Windows
targetos: Windows
req.typenames: USB_HUB_TYPE
req.product: Windows 10 or later.
---

# IOCTL_USB_HCD_GET_STATS_1 IOCTL


##  Major Code: 


[[XREF-LINK:IRP_MJ_DEVICE_CONTROL]

## -description


The <b>IOCTL_USB_HCD_GET_STATS_1</b> IOCTL has been deprecated. Do not use.


## -ioctlparameters




### -input-buffer


<text></text>



### -input-buffer-length


<text></text>



### -output-buffer


<text></text>



### -output-buffer-length


<text></text>



### -in-out-buffer


<text></text>



### -inout-buffer-length


<text></text>



### -status-block


Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.
Otherwise, Status to the appropriate error condition as a NTSTATUS code. 
For more information, see [XREF-LINK:NTSTATUS Values].

