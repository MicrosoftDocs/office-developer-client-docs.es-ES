---
title: XPProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.XPProviderInit
api_type:
- COM
ms.assetid: df6eacf4-1cf9-4c25-806f-f87c38dad597
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0415e782a98102314ce732f744c0d29590f646c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820999"
---
# <a name="xpproviderinit"></a><span data-ttu-id="65503-103">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="65503-103">XPProviderInit</span></span>

  
  
<span data-ttu-id="65503-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="65503-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="65503-105">Inicializa un proveedor de transporte para la operación.</span><span class="sxs-lookup"><span data-stu-id="65503-105">Initializes a transport provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="65503-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="65503-106">Header file:</span></span>  <br/> |<span data-ttu-id="65503-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="65503-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="65503-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="65503-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="65503-109">Proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="65503-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="65503-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="65503-110">Called by:</span></span>  <br/> |<span data-ttu-id="65503-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="65503-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT XPProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPXPPROVIDER FAR * lppXPProvider
);
```

## <a name="parameters"></a><span data-ttu-id="65503-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65503-112">Parameters</span></span>

 <span data-ttu-id="65503-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="65503-113">_hInstance_</span></span>
  
> <span data-ttu-id="65503-114">[entrada] La instancia de la biblioteca de vínculos dinámicos del proveedor de transporte (DLL) que MAPI utilizada cuando carga el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="65503-114">[in] The instance of the transport provider's dynamic-link library (DLL) that MAPI used when it loaded the DLL.</span></span>
    
 <span data-ttu-id="65503-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="65503-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="65503-116">[entrada] Puntero a un objeto del asignador de memoria exposición de la interfaz de OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="65503-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="65503-117">El proveedor de transporte que necesite utilizar este método de asignación cuando se trabaja con ciertas interfaces como **IStream**.</span><span class="sxs-lookup"><span data-stu-id="65503-117">The transport provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="65503-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="65503-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="65503-119">[entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="65503-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="65503-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="65503-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="65503-121">[entrada] Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) , que se usará para asignar memoria adicional.</span><span class="sxs-lookup"><span data-stu-id="65503-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="65503-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="65503-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="65503-123">[entrada] Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="65503-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="65503-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="65503-124">_ulFlags_</span></span>
  
> <span data-ttu-id="65503-125">[entrada] Máscara de bits de indicadores.</span><span class="sxs-lookup"><span data-stu-id="65503-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="65503-126">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="65503-126">The following flag can be set:</span></span>
    
<span data-ttu-id="65503-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="65503-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="65503-128">Se está cargando el proveedor en el contexto de un servicio de Windows, un tipo especial de proceso sin acceso a cualquier interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="65503-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="65503-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="65503-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="65503-130">[entrada] Número de versión de la interfaz de proveedor de servicio (SPI) que usa MAPI..</span><span class="sxs-lookup"><span data-stu-id="65503-130">[in] Version number of the service provider interface (SPI) that Mapi.dll uses.</span></span> <span data-ttu-id="65503-131">Para el número de versión actual, vea el archivo de encabezado Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="65503-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="65503-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="65503-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="65503-133">[out] Puntero al número de versión de la SPI que usa este proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="65503-133">[out] Pointer to the version number of the SPI that this transport provider uses.</span></span> 
    
 <span data-ttu-id="65503-134">_lppXPProvider_</span><span class="sxs-lookup"><span data-stu-id="65503-134">_lppXPProvider_</span></span>
  
> <span data-ttu-id="65503-135">[out] Puntero a un puntero al objeto de proveedor de transporte inicializado.</span><span class="sxs-lookup"><span data-stu-id="65503-135">[out] Pointer to a pointer to the initialized transport provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="65503-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65503-136">Return value</span></span>

<span data-ttu-id="65503-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="65503-137">S_OK</span></span> 
  
> <span data-ttu-id="65503-138">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="65503-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="65503-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="65503-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="65503-140">La versión SPI usada por MAPI no es compatible con el SPI usado por este proveedor.</span><span class="sxs-lookup"><span data-stu-id="65503-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="65503-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="65503-141">Remarks</span></span>

<span data-ttu-id="65503-142">MAPI llama a la función de punto de entrada **XPProviderInit** para inicializar un proveedor de transporte después de un inicio de sesión de cliente.</span><span class="sxs-lookup"><span data-stu-id="65503-142">MAPI calls the entry point function **XPProviderInit** to initialize a transport provider following a client logon.</span></span> <span data-ttu-id="65503-143">**XPProviderInit** se llama una vez para cada proveedor de transporte especificado en el perfil del cliente.</span><span class="sxs-lookup"><span data-stu-id="65503-143">**XPProviderInit** is called once for each transport provider specified in the client's profile.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="65503-144">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="65503-144">Notes to implementers</span></span>

<span data-ttu-id="65503-145">Un proveedor de transporte debe implementar **XPProviderInit** como una función de punto de entrada en el archivo DLL del proveedor.</span><span class="sxs-lookup"><span data-stu-id="65503-145">A transport provider must implement **XPProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="65503-146">La implementación debe basarse en el prototipo de función **XPPROVIDERINIT** , también especificado en Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="65503-146">The implementation must be based on the **XPPROVIDERINIT** function prototype, also specified in Mapispi.h.</span></span> <span data-ttu-id="65503-147">MAPI define **XPPROVIDERINIT** para usar el tipo de llamada de inicialización estándar MAPI, STDMAPIINITCALLTYPE, que hace que **XPProviderInit** que se deben seguir la convención de llamada CDECL.</span><span class="sxs-lookup"><span data-stu-id="65503-147">MAPI defines **XPPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **XPProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="65503-148">Una ventaja de CDECL es que se pueden intentar llamadas incluso si el número de parámetros de llamada no coincide con el número de parámetros definidos.</span><span class="sxs-lookup"><span data-stu-id="65503-148">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="65503-149">Un proveedor se puede inicializar varias veces como consecuencia de que aparezca en varios perfiles en uso simultáneo o de aparecer más de una vez en el mismo perfil.</span><span class="sxs-lookup"><span data-stu-id="65503-149">A provider can be initialized multiple times as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="65503-150">Debido a que el objeto de proveedor contiene contexto, **XPProviderInit** debe devolver un objeto de proveedor diferente en _lppXPProvider_ para cada inicialización, incluso para varias inicializaciones en el mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="65503-150">Because the provider object contains context, **XPProviderInit** must return a different provider object in  _lppXPProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="65503-151">El proveedor de transporte debe usar las funciones que señala _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ para la mayoría de asignación de memoria y cancelación de asignación.</span><span class="sxs-lookup"><span data-stu-id="65503-151">The transport provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="65503-152">En concreto, el proveedor debe usar estas funciones para asignar la memoria para su uso por las aplicaciones cliente al llamar a las interfaces de objeto como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="65503-152">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="65503-153">Si el proveedor también espera utilizar el asignador de memoria OLE, debe llamar al método **IUnknown:: AddRef** del objeto asignador indicado por el parámetro _lpMalloc_ .</span><span class="sxs-lookup"><span data-stu-id="65503-153">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="65503-154">Para obtener más información acerca de cómo escribir **XPProviderInit**, vea [inicializar el proveedor de transporte](initializing-the-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="65503-154">For more information about writing **XPProviderInit**, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span> <span data-ttu-id="65503-155">Para obtener más información acerca de las funciones de punto de entrada, vea [implementar una función de punto de servicio de proveedor de entrada](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="65503-155">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="65503-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="65503-156">See also</span></span>



[<span data-ttu-id="65503-157">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="65503-157">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="65503-158">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="65503-158">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)
  
[<span data-ttu-id="65503-159">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="65503-159">MSProviderInit</span></span>](msproviderinit.md)

