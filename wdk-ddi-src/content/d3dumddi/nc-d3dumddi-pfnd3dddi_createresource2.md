---
UID: NC:d3dumddi.PFND3DDDI_CREATERESOURCE2
title: PFND3DDDI_CREATERESOURCE2
author: windows-driver-content
description: Creates a resource. Implemented by Windows Display Driver Model (WDDM) 1.2 and later user-mode display drivers.
old-location: display\createresource2.htm
old-project: display
ms.assetid: a8326707-cffc-4a20-ad3d-c7862661f513
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: display.createresource2, CreateResource2 callback function [Display Devices], CreateResource2, PFND3DDDI_CREATERESOURCE2, PFND3DDDI_CREATERESOURCE2, d3dumddi/CreateResource2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3dumddi.h
req.include-header: D3dumddi.h
req.target-type: Desktop
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
-	UserDefined
apilocation:
-	D3dumddi.h
apiname:
-	CreateResource2
product: Windows
targetos: Windows
req.typenames: DXGK_PTE
---

# PFND3DDDI_CREATERESOURCE2 callback


## -description


Creates a resource. Implemented by Windows Display Driver Model (WDDM) 1.2 and later user-mode display drivers.


## -prototype


````
PFND3DDDI_CREATERESOURCE2 CreateResource2;

_Check_return_ HRESULT APIENTRY* CreateResource2(
  _In_    HANDLE                    hDevice,
  _Inout_ D3DDDIARG_CREATERESOURCE2 *pResource2
)
{ ... }
````


## -parameters




### -param hDevice [in]

 A handle to the display device (graphics context) that is used to create the resource.


### -param *






#### - pResource2 [in, out]

 A pointer to a <a href="..\d3dukmdt\ns-d3dukmdt-_d3dddiarg_createresource2.md">D3DDDIARG_CREATERESOURCE2</a> structure that describes the resource that is created.


## -returns


Returns <b>S_OK</b> or an appropriate error result. WDDM 1.3 and later Direct3D Level 9 drivers must return this error code:
<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="..\d3dukmdt\ns-d3dukmdt-_d3dddiarg_createresource2.md">D3DDDIARG_CREATERESOURCE2</a>.<b>Flags</b> member has the <b>CaptureBuffer</b> flag value set and the resource exceeds what the driver can support.

</td>
</tr>
</table> 



## -remarks


The call to <i>CreateResource2</i> can contain a list of surfaces. The <b>SurfCount</b> member of the <a href="..\d3dukmdt\ns-d3dukmdt-_d3dddiarg_createresource2.md">D3DDDIARG_CREATERESOURCE2</a> structure that is specified by the <i>pResource2</i> parameter specifies the number of surfaces—including MIP-map levels—to create. For example, a 256x256x9 texture MIP-map resource contains a list of nine surfaces where the <b>SurfCount</b> member and number of MIP-map levels are both set to 9. A cube map that contains nine MIP-map levels should have the number of MIP-map levels set to 9 and <b>SurfCount</b> set to 54. A three-surface swap chain should have <b>SurfCount</b> set to 3 and the number of MIP-map levels set to 0. Note that the number of MIP-map levels is always less than or equal to the value in <b>SurfCount</b>.

In response to the <i>CreateResource2</i> call, the user-mode display driver can call the <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_allocatecb.md">pfnAllocateCb</a> function to create one or more memory allocations. The user-mode display driver must determine whether it must create multiple allocations per surface, one allocation for all surfaces, or one allocation per surface. For more information about allocations, see <a href="https://msdn.microsoft.com/33fc9f0a-57ed-479f-9cb0-3f3f540047ab">Video Memory Management and GPU Scheduling</a>.
<div class="alert"><b>Note</b>    The driver's <i>CreateResource2</i> function is not required to call <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_allocatecb.md">pfnAllocateCb</a> before returning; instead, the driver can defer allocation creation. </div><div> </div><div class="alert"><b>Note</b>    A resource can be shared only if all of the allocations for the resource are made atomically in a single call to <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_allocatecb.md">pfnAllocateCb</a>.</div><div> </div>The <b>hResource</b> member in the <a href="..\d3dukmdt\ns-d3dukmdt-_d3dddiarg_createresource2.md">D3DDDIARG_CREATERESOURCE2</a> structure is a handle that's used to identify the resource. The user-mode display driver should store the value of <b>hResource</b> that was passed in the <i>CreateResource2</i> call and overwrite the value with another value that the Microsoft Direct3D runtime can use when the <i>CreateResource2</i> call returns. In other words, in calls to the runtime, the user-mode display driver uses the <b>hResource</b> value that was passed to <i>CreateResource2</i>; in calls to the user-mode display driver (for example, in calls to the <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_settexture.md">SetTexture</a> or <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_setstreamsource.md">SetStreamSource</a> functions), the runtime uses the <b>hResource</b> value that was returned from <i>CreateResource2</i>. Note that each surface does not have an explicit handle; if the surface must be referred to individually (for example in a call to the <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_blt.md">Blt</a> function), it is referred to by a handle and an index. The index identifies the surface within the resource. The index is the same as the index of the surface in the array that is contained in the <b>pSurfList</b> member of <b>D3DDDIARG_CREATERESOURCE2</b>.

Resources can be shared by multiple devices (<b>hDevice</b>) and processes. The runtime specifies that a resource is shared by setting the <b>SharedResource</b> bit-field flag in the <b>Flags</b> member of <a href="..\d3dukmdt\ns-d3dukmdt-_d3dddiarg_createresource2.md">D3DDDIARG_CREATERESOURCE2</a>. If this bit-field flag is set, the user-mode display driver must adhere to the following restrictions on shared resources: 
<ul>
<li>
The user-mode display driver can call the <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_allocatecb.md">pfnAllocateCb</a> and <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_deallocatecb.md">pfnDeallocateCb</a> functions exactly once each.

</li>
<li>
The user-mode display driver cannot create additional allocations for the resource after the resource is initially created and likewise can destroy the resource allocations only at the time that the resource itself is destroyed.

</li>
<li>
When the user-mode display driver's <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_destroyresource.md">DestroyResource</a> function is called for a shared resource that was created or opened through a call to the driver's <i>CreateResource2</i> or <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_openresource.md">OpenResource</a> function, the driver must set the <b>hResource</b> member of the <a href="..\d3dumddi\ns-d3dumddi-_d3dddicb_deallocate.md">D3DDDICB_DEALLOCATE</a> structure to non-NULL and the <b>NumAllocations</b> member of <b>D3DDDICB_DEALLOCATE</b> to zero in a call to the <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_deallocatecb.md">pfnDeallocateCb</a> function to destroy or close the resource. That is, allocations that are associated with a shared resource cannot be destroyed or closed individually; the resource must be destroyed or closed atomically in one call to <i>pfnDeallocateCb</i>.

</li>
<li>
The number of allocations must be consistent for the resource type (that is, another process that is creating the same resource type should generate the same number and type of allocations). Furthermore, renaming is not allowed for these resources.

</li>
</ul>The bit-field flags that are specified in the <a href="..\d3dukmdt\ns-d3dukmdt-_d3dddi_resourceflags2.md">D3DDDI_RESOURCEFLAGS2</a> structure are passed in the <b>Flags</b> member of <a href="..\d3dukmdt\ns-d3dukmdt-_d3dddiarg_createresource2.md">D3DDDIARG_CREATERESOURCE2</a>.
<div class="alert"><b>Note</b>    A resource can be created without specifying any flags. Surfaces that are associated with such a resource can potentially be locked and can be a source or destination in a bit-block transfer (bitblt) operation. However, such surfaces cannot be used for anything else. </div><div> </div><div class="alert"><b>Note</b>    Plain surfaces are differentiated from textures or stand-alone render targets by the absence of the <b>Texture</b> or <b>Primary</b> bit-field flag. For example, the presence of the <b>Primary</b> bit-field flag indicates a stand-alone render target and the absence of this flag indicates a render target that is a back buffer.</div><div> </div><div class="alert"><b>Note</b>    To ensure that changes to the runtime do not break existing drivers, the drivers must not use the following reserved members of the <a href="..\d3dukmdt\ns-d3dukmdt-_d3dddiarg_createresource2.md">D3DDDIARG_CREATERESOURCE2</a> structure in calls to their <i>CreateResource2</i> function to affect the behavior of the drivers:<ul>
<li>
The undefined bits of the <b>Flags</b> member are reserved.

</li>
<li>
If the <b>Primary</b> bit-field flag is not set in <b>Flags</b>, the <b>RefreshRate</b> and <b>Output</b> members are reserved.

</li>
<li>
If the <b>RenderTarget</b>, <b>DecodeRenderTarget</b>, or <b>VideoProcessRenderTarget</b> bit-field flag is not set in <b>Flags</b>, the <b>MultisampleType</b> and <b>MultisampleQuality</b> members are reserved.

</li>
<li>
If the <b>VertexBuffer</b> bit-field flag is not set in <b>Flags</b>, the <b>Fvf</b> member is reserved.

</li>
<li>
If the <b>Texture</b>, <b>CubeMap</b>, and <b>Volume</b> bit-field flags are not set in <b>Flags</b>, the <b>MipLevels</b> member is reserved.

</li>
</ul>
</div><div> </div>For more information about creating and destroying resources, see <a href="https://msdn.microsoft.com/d443bdc3-1c5a-4372-9e6a-b8a4d21499b9">Handling Resource Creation and Destruction</a>.

For a system memory resource, the display miniport driver can chose to wrap an allocation around the system memory if the system memory is properly aligned for direct access by the graphics processing unit (GPU). The display miniport driver wraps an allocation around the system memory by setting the <b>ExistingSysMem</b>  flag in the <b>Flags</b> member of the <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_allocationinfo.md">DXGK_ALLOCATIONINFO</a> structure when creating the allocation by using its <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_createallocation.md">DxgkDdiCreateAllocation</a> function. If the display miniport driver cannot wrap an allocation around the system memory or the wrapping fails, the driver should still succeed the creation of the resource and use the CPU to access the resource.

If the runtime requests to create a vertex or index buffer and if the user-mode display driver cannot create the buffer for reasons other than out of memory (for example, a lack of hardware support), the driver must fail with <b>D3DERR_NOTAVAILABLE</b>.



## -see-also

<a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_allocatecb.md">pfnAllocateCb</a>

<a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_allocationinfo.md">DXGK_ALLOCATIONINFO</a>

<a href="..\d3dukmdt\ns-d3dukmdt-_d3dddiarg_createresource2.md">D3DDDIARG_CREATERESOURCE2</a>

<a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_createallocation.md">DxgkDdiCreateAllocation</a>

<a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_settexture.md">SetTexture</a>

<a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_setstreamsource.md">SetStreamSource</a>

<a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_deallocatecb.md">pfnDeallocateCb</a>

<a href="..\d3dukmdt\ns-d3dukmdt-_d3dddi_resourceflags2.md">D3DDDI_RESOURCEFLAGS2</a>

<a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_blt.md">Blt</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20PFND3DDDI_CREATERESOURCE2 callback function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>
