---
UID: NE:wudfddi_types._WDF_DEVICE_HWACCESS_TARGET_TYPE
title: "_WDF_DEVICE_HWACCESS_TARGET_TYPE"
author: windows-driver-content
description: The WDF_DEVICE_HWACCESS_TARGET_TYPE enumeration is used internally by the framework. Do not use.
old-location: wdf\wdf_device_hwaccess_target_type.htm
old-project: wdf
ms.assetid: AF462D58-1854-4A56-8DC6-63F373439842
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: wudfddi_types/WdfDeviceHwAccessTargetTypeRegisterBuffer, WdfDeviceHwAccessTargetTypeMaximum, wudfddi_types/WdfDeviceHwAccessTargetTypeInvalid, wdfdevice/WdfDeviceHwAccessTargetTypePortBuffer, wudfddi_types/WdfDeviceHwAccessTargetTypePortBuffer, WDF_DEVICE_HWACCESS_TARGET_TYPE enumeration, wdfdevice/WDF_DEVICE_HWACCESS_TARGET_TYPE, wudfddi_types/WdfDeviceHwAccessTargetTypeMaximum, WdfDeviceHwAccessTargetTypeRegister, wdfdevice/WdfDeviceHwAccessTargetTypeRegister, wdfdevice/WdfDeviceHwAccessTargetTypeRegisterBuffer, wdfdevice/WdfDeviceHwAccessTargetTypeInvalid, WdfDeviceHwAccessTargetTypeRegisterBuffer, WdfDeviceHwAccessTargetTypePortBuffer, wdfdevice/WdfDeviceHwAccessTargetTypePort, _WDF_DEVICE_HWACCESS_TARGET_TYPE, wudfddi_types/WdfDeviceHwAccessTargetTypeRegister, WdfDeviceHwAccessTargetTypeInvalid, wdfdevice/PWDF_DEVICE_HWACCESS_TARGET_TYPE, PWDF_DEVICE_HWACCESS_TARGET_TYPE enumeration pointer, *PWDF_DEVICE_HWACCESS_TARGET_TYPE, wudfddi_types/WdfDeviceHwAccessTargetTypePort, WDF_DEVICE_HWACCESS_TARGET_TYPE, wudfddi_types/PWDF_DEVICE_HWACCESS_TARGET_TYPE, PWDF_DEVICE_HWACCESS_TARGET_TYPE, WdfDeviceHwAccessTargetTypePort, umdf.wdf_device_hwaccess_target_type, wdf.wdf_device_hwaccess_target_type, wdfdevice/WdfDeviceHwAccessTargetTypeMaximum, wudfddi_types/WDF_DEVICE_HWACCESS_TARGET_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wudfddi_types.h
req.include-header: Wdf.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.11
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.exe
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	HeaderDef
apilocation:
-	wdfdevice.h
-	wudfddi_types.h
apiname:
-	WDF_DEVICE_HWACCESS_TARGET_TYPE
product: Windows
targetos: Windows
req.typenames: WDF_DEVICE_HWACCESS_TARGET_TYPE, *PWDF_DEVICE_HWACCESS_TARGET_TYPE
req.product: Windows 10 or later.
---

# _WDF_DEVICE_HWACCESS_TARGET_TYPE enumeration


## -description


<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>WDF_DEVICE_HWACCESS_TARGET_TYPE</b> enumeration is used internally by the framework. Do not use.


## -syntax


````
typedef enum __WDF_IO_TARGET_STATE { 
  WdfDeviceHwAccessTargetTypeInvalid         = 0,
  WdfDeviceHwAccessTargetTypeRegister        = 1,
  WdfDeviceHwAccessTargetTypeRegisterBuffer  = 2,
  WdfDeviceHwAccessTargetTypePort            = 3,
  WdfDeviceHwAccessTargetTypePortBuffer      = 4,
  WdfDeviceHwAccessTargetTypeMaximum         = 5
} WDF_DEVICE_HWACCESS_TARGET_TYPE, *PWDF_DEVICE_HWACCESS_TARGET_TYPE;
````


## -enum-fields




### -field WdfDeviceHwAccessTargetTypeInvalid



### -field WdfDeviceHwAccessTargetTypeRegister



### -field WdfDeviceHwAccessTargetTypeRegisterBuffer



### -field WdfDeviceHwAccessTargetTypePort



### -field WdfDeviceHwAccessTargetTypePortBuffer



### -field WdfDeviceHwAccessTargetTypeMaximum



## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff561319">UMDF Structures and Enumeration Types</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20WDF_DEVICE_HWACCESS_TARGET_TYPE enumeration%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>
