---
UID: NS:ndischimney._NDIS_OFFLOAD_HANDLE
title: "_NDIS_OFFLOAD_HANDLE"
author: windows-driver-content
description: The NDIS_OFFLOAD_HANDLE structure represents a driver's context for an offloaded state object.
old-location: netvista\ndis_offload_handle.htm
old-project: netvista
ms.assetid: cc1d7ca2-273a-42ca-896c-aebee862a4cd
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: "*PNDIS_OFFLOAD_HANDLE, NDIS_OFFLOAD_HANDLE structure [Network Drivers Starting with Windows Vista], PNDIS_OFFLOAD_HANDLE, tcp_chim_struct_32ac0fbc-873b-4cd9-9121-d7e77667f05d.xml, ndischimney/NDIS_OFFLOAD_HANDLE, ndischimney/PNDIS_OFFLOAD_HANDLE, NDIS_OFFLOAD_HANDLE, netvista.ndis_offload_handle, PNDIS_OFFLOAD_HANDLE structure pointer [Network Drivers Starting with Windows Vista], _NDIS_OFFLOAD_HANDLE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ndischimney.h
req.include-header: Ndischimney.h
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
-	ndischimney.h
apiname:
-	NDIS_OFFLOAD_HANDLE
product: Windows
targetos: Windows
req.typenames: "*PNDIS_OFFLOAD_HANDLE, NDIS_OFFLOAD_HANDLE"
---

# _NDIS_OFFLOAD_HANDLE structure


## -description


<p class="CCE_Message">[The TCP chimney offload feature is deprecated and should not be used.]

The NDIS_OFFLOAD_HANDLE structure represents a driver's context for an offloaded state object.


## -syntax


````
typedef struct _NDIS_OFFLOAD_HANDLE {
  PVOID NdisReserved[1];
  PVOID MiniportOffloadContext;
} NDIS_OFFLOAD_HANDLE, *PNDIS_OFFLOAD_HANDLE;
````


## -struct-fields




### -field NdisReserved

Reserved for use by NDIS.


### -field MiniportOffloadContext

A pointer that references a host memory location into which the underlying driver writes a PVOID
     value when completing the initiate offload operation. This PVOID value references the underlying
     driver's offload context for the offloaded state object.


## -remarks


When propagating the offload of a TCP chimney state object, an intermediate driver supplies a pointer
    to an NDIS_OFFLOAD_HANDLE structure. This pointer, in effect, references the intermediate driver's
    context for the offloaded state object.

The NDIS_OFFLOAD_HANDLE structure contains a 
    <b>MiniportOffloadContext</b> pointer that references a memory location into which the underlying driver
    or offload target writes a PVOID value before completing the initiate offload operation. This PVOID value
    references the underlying driver's or offload target's context for the offloaded state object.

For more information about the use of the NDIS_OFFLOAD_HANDLE structure, see 
    <mshelp:link keywords="netvista.referencing_offloaded_state_through_an_intermediate_driver" tabindex="0">
    Referencing Offloaded State Through an Intermediate Driver</mshelp:link>.



## -see-also

<a href="..\ndischimney\nf-ndischimney-ndisminitiateoffloadcomplete.md">NdisMInitiateOffloadComplete</a>

<a href="..\ndischimney\nc-ndischimney-w_initiate_offload_handler.md">MiniportInitiateOffload</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NDIS_OFFLOAD_HANDLE structure%20 RELEASE:%20(1/18/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>
