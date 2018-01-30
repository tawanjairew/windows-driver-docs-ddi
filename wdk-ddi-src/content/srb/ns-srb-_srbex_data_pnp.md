---
UID: NS:srb._SRBEX_DATA_PNP
title: "_SRBEX_DATA_PNP"
author: windows-driver-content
description: The SRBEX_DATA_PNP structure contains the request data for an extended plug and play (PNP) SRB.
old-location: storage\srbex_data_pnp.htm
old-project: storage
ms.assetid: CB64AF68-C40D-44F0-8F52-6BF05E23E5E1
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: StorQueryCapabilities, StorRemoveDevice, StorFilterResourceRequirements, StorStartDevice, StorSupriseRemoval, storport/SRBEX_DATA_PNP, StorStopDevice, _SRBEX_DATA_PNP, SRBEX_DATA_PNP, storport/PSRBEX_DATA_PNP, StorQueryResourceRequirements, storage.srbex_data_pnp, *PSRBEX_DATA_PNP, PSRBEX_DATA_PNP structure pointer [Storage Devices], PSRBEX_DATA_PNP, SRBEX_DATA_PNP structure [Storage Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: srb.h
req.include-header: Storport.h, Srb.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows 8.
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
-	Storport.h
apiname:
-	SRBEX_DATA_PNP
product: Windows
targetos: Windows
req.typenames: "*PSRBEX_DATA_PNP, SRBEX_DATA_PNP"
req.product: Windows 10 or later.
---

# _SRBEX_DATA_PNP structure


## -description


The <b>SRBEX_DATA_PNP</b> structure contains the request data for an extended plug and play (PNP) SRB.
<div class="alert"><b>Note</b>  The SCSI port driver and SCSI miniport driver models may be altered or unavailable in the future. Instead, we recommend using the <a href="https://msdn.microsoft.com/en-us/windows/hardware/drivers/storage/storport-driver">Storport driver</a> and <a href="https://msdn.microsoft.com/en-us/windows/hardware/drivers/storage/storport-miniport-drivers">Storport miniport</a> driver models.</div><div> </div>

## -syntax


````
typedef struct _SRBEX_DATA_PNP {
  SRBEXDATATYPE   Type;
  ULONG           Length;
  UCHAR           PnPSubFunction;
  UCHAR           Reserved[3];
  STOR_PNP_ACTION PnPAction;
  ULONG           SrbPnPFlags;
  ULONG           Reserved1;
} SRBEX_DATA_PNP, *PSRBEX_DATA_PNP;
````


## -struct-fields




### -field Type

Data type indicator for the bidirectional extended SRB data structure. Set to <b>SrbExDataTypePnp</b>.


### -field Length

Length of the data in this structure starting with the <b>PnPSubFunction</b> member. Set to SRBEX_DATA_PNP_LENGTH.


### -field PnPSubFunction

This member is not currently used. Set to 0.


### -field Reserved

This member is reserved. Set to 0.


### -field PnPAction

The plug and play action to perform. This member can have one of the following values:
<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="StorStartDevice"></a><a id="storstartdevice"></a><a id="STORSTARTDEVICE"></a><dl>
<dt><b>StorStartDevice</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
Start the device.

</td>
</tr>
<tr>
<td width="40%"><a id="StorRemoveDevice"></a><a id="storremovedevice"></a><a id="STORREMOVEDEVICE"></a><dl>
<dt><b>StorRemoveDevice</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Remove the device.

</td>
</tr>
<tr>
<td width="40%"><a id="StorStopDevice"></a><a id="storstopdevice"></a><a id="STORSTOPDEVICE"></a><dl>
<dt><b>StorStopDevice</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Stop the device.

</td>
</tr>
<tr>
<td width="40%"><a id="StorQueryCapabilities"></a><a id="storquerycapabilities"></a><a id="STORQUERYCAPABILITIES"></a><dl>
<dt><b>StorQueryCapabilities</b></dt>
<dt>0x09</dt>
</dl>
</td>
<td width="60%">
Query the capabilities of the device.

</td>
</tr>
<tr>
<td width="40%"><a id="StorQueryResourceRequirements"></a><a id="storqueryresourcerequirements"></a><a id="STORQUERYRESOURCEREQUIREMENTS"></a><dl>
<dt><b>StorQueryResourceRequirements</b></dt>
<dt>0x0B</dt>
</dl>
</td>
<td width="60%">
Query the resource requirements for the device.

</td>
</tr>
<tr>
<td width="40%"><a id="StorFilterResourceRequirements"></a><a id="storfilterresourcerequirements"></a><a id="STORFILTERRESOURCEREQUIREMENTS"></a><dl>
<dt><b>StorFilterResourceRequirements</b></dt>
<dt>0x0D</dt>
</dl>
</td>
<td width="60%">
Filter the resource requirements for the device. 

</td>
</tr>
<tr>
<td width="40%"><a id="StorSupriseRemoval"></a><a id="storsupriseremoval"></a><a id="STORSUPRISEREMOVAL"></a><dl>
<dt><b>StorSupriseRemoval</b></dt>
<dt>0x17</dt>
</dl>
</td>
<td width="60%">
Surprise Removal of the device. This value is available starting with Windows 7.

</td>
</tr>
</table> 


### -field SrbPnPFlags

Indicates that the PNP request is for the adapter if SRB_PNP_FLAGS_ADAPTER_REQUEST is set and that storage device address is reserved. Otherwise, <i>SrbPnPFlags</i> will be <b>NULL</b>, indicating that the request is for the storage device specified by an address at <b>AddressOffset</b> in the <a href="..\srb\ns-srb-_storage_request_block.md">STORAGE_REQUEST_BLOCK</a> structure.


### -field Reserved1

This member is reserved. Set to 0.


## -see-also

<a href="..\srb\ns-srb-_storage_request_block.md">STORAGE_REQUEST_BLOCK</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20SRBEX_DATA_PNP structure%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>
