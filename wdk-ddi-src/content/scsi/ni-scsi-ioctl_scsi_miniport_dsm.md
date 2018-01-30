---
UID: NI:scsi.IOCTL_SCSI_MINIPORT_DSM
title: IOCTL_SCSI_MINIPORT_DSM
author: windows-driver-content
description: A Data Set Management (DSM) notification is transferred to a miniport driver in a IOCTL_SCSI_MINIPORT_DSM control code request.
old-location: storage\ioctl_scsi_miniport_dsm.htm
old-project: storage
ms.assetid: CA91B623-F926-453D-A348-92655875D801
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: storage.ioctl_scsi_miniport_dsm, IOCTL_SCSI_MINIPORT_DSM control code [Storage Devices], IOCTL_SCSI_MINIPORT_DSM, scsi/IOCTL_SCSI_MINIPORT_DSM
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: scsi.h
req.include-header: Ntddscsi.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows 8.1.
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
-	scsi.h
apiname:
-	IOCTL_SCSI_MINIPORT_DSM
product: Windows
targetos: Windows
req.typenames: SES_DOWNLOAD_MICROCODE_STATE, *PSES_DOWNLOAD_MICROCODE_STATE
req.product: Windows 10 or later.
---

# IOCTL_SCSI_MINIPORT_DSM IOCTL


##  Major Code: 


[[XREF-LINK:IRP_MJ_DEVICE_CONTROL]

## -description


A Data Set Management (DSM) notification is transferred to a miniport driver in a 
     <b>IOCTL_SCSI_MINIPORT_DSM</b> control code request. The <b>IOCTL_SCSI_MINIPORT_DSM</b> request is a sub-IOCTL of <a href="..\ntddscsi\ni-ntddscsi-ioctl_scsi_miniport.md">IOCTL_SCSI_MINIPORT</a>. This IOCTL generated by StorPort in response to a DSM action, then sent  to the miniport as a <a href="..\srb\ns-srb-_storage_request_block.md">STORAGE_REQUEST_BLOCK</a> (SRB) with a function type of SRB_FUNCTION_IO_CONTROL. The input and output data is contained in the SRB data block. 
<div class="alert"><b>Note</b>  The SCSI port driver and SCSI miniport driver models may be altered or unavailable in the future. Instead, we recommend using the <a href="https://msdn.microsoft.com/en-us/windows/hardware/drivers/storage/storport-driver">Storport driver</a> and <a href="https://msdn.microsoft.com/en-us/windows/hardware/drivers/storage/storport-miniport-drivers">Storport miniport</a> driver models.</div><div> </div>

## -ioctlparameters




### -input-buffer

The buffer specified in the <b>DataBuffer</b> member of the SRB must contain an <a href="..\ntddscsi\ns-ntddscsi-_srb_io_control.md">SRB_IO_CONTROL</a> structure and a <b>DSM_NOTIFICATION_REQUEST_BLOCK</b> structure.  


### -input-buffer-length

<b>DataTransferLength</b> indicates the size, in bytes, of the buffer, which must be at least <b>sizeof</b> (SRB_IO_CONTROL) + <b>sizeof</b>(DSM_NOTIFICATION_REQUEST_BLOCK), with additional storage for the <b>MP_DEVICE_DATA_SET_RANGE</b> structures included.


### -output-buffer

An updated <a href="..\ntddscsi\ns-ntddscsi-_srb_io_control.md">SRB_IO_CONTROL</a> structure is returned to the data buffer in the SRB. The <b>SrbStatus</b> contains the result of the miniport's processing of the request.


### -output-buffer-length

The length of an <a href="..\ntddscsi\ns-ntddscsi-_srb_io_control.md">SRB_IO_CONTROL</a> structure.


### -in-out-buffer


<text></text>



### -inout-buffer-length


<text></text>



### -status-block

The resulting status of the function request is set in the <b>SrbStatus</b> member of <a href="..\ntddscsi\ns-ntddscsi-_srb_io_control.md">SRB_IO_CONTROL</a>. The following are the  DSM disk IOCTL status codes.
<table>
<tr>
<th>SRB Status</th>
<th>Description</th>
</tr>
<tr>
<td>SRB_STATUS_SUCCESS</td>
<td>The request completed successfully.</td>
</tr>
<tr>
<td>SRB_STATUS_INVALID_REQUEST</td>
<td>The request contains an invalid buffer size</td>
</tr>
</table> 


## -remarks


<b>DSM_NOTIFICATION_REQUEST_BLOCK</b>

A <b>DSM_NOTIFICATION_REQUEST_BLOCK</b> structure immediately follows the <a href="..\ntddscsi\ns-ntddscsi-_srb_io_control.md">SRB_IO_CONTROL</a> structure in the data buffer of the SRB.  <b>DSM_NOTIFICATION_REQUEST_BLOCK</b> is defined in ntddscsi.h as the following.
<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef struct _DSM_NOTIFICATION_REQUEST_BLOCK {
    ULONG   Version;
    ULONG   Size;
    ULONG   NotifyFLags;
    ULONG   DataSetProfile;
    ULONG   Reserved[3];
    ULONG   DataSetRangesCount;
    MP_DEVICE_DATA_SET_RANGE DataSetRanges[ANYSIZE_ARRAY];
} DSM_NOTIFICATION_REQUEST_BLOCK, *PDSM_NOTIFICATION_REQUEST_BLOCK;</pre>
</td>
</tr>
</table></span></div>

<b>MP_DEVICE_DATA_SET_RANGE</b>

The LBA ranges are included in the  in <b>DataSetRanges</b> member of <b>DSM_NOTIFICATION_REQUEST_BLOCK</b> as an array of <b>MP_DEVICE_DATA_SET_RANGE</b> structures. <b>MP_DEVICE_DATA_SET_RANGE</b> is defined in ntddscsi.h as the following.
<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>rypedef struct _MP_DEVICE_DATA_SET_RANGE {
    LONGLONG    StartingOffset;
    ULONGLONG   LengthInBytes;
} MP_DEVICE_DATA_SET_RANGE, *PMP_DEVICE_DATA_SET_RANGE;</pre>
</td>
</tr>
</table></span></div>

The <b>DSM_NOTIFICATION_REQUEST_BLOCK</b> structure is located after the <a href="..\ntddscsi\ns-ntddscsi-_srb_io_control.md">SRB_IO_CONTROL</a> structure in the <b>DataBuffer</b> of the SRB.

The <a href="..\ntddscsi\ns-ntddscsi-_srb_io_control.md">SRB_IO_CONTROL</a> structure for this IOCTL contains IOCTL_MINIPORT_SIGNATURE_DSM_NOTIFICATION in its <b>Signature</b> member and <b>IOCTL_SCSI_MINIPORT_DSM</b> in the <b>ControlCode</b> member.



## -see-also

<a href="..\ntddscsi\ni-ntddscsi-ioctl_scsi_miniport.md">IOCTL_SCSI_MINIPORT</a>

<a href="..\srb\ns-srb-_storage_request_block.md">STORAGE_REQUEST_BLOCK</a>

<a href="..\ntddscsi\ns-ntddscsi-_srb_io_control.md">SRB_IO_CONTROL</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20IOCTL_SCSI_MINIPORT_DSM control code%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>
