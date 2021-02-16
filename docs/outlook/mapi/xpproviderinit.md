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
ms.openlocfilehash: ee0ff8d32436f71020be2cdc91d6677bd4ec8e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428539"
---
# <a name="xpproviderinit"></a><span data-ttu-id="1da65-103">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="1da65-103">XPProviderInit</span></span>

  
  
<span data-ttu-id="1da65-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1da65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1da65-105">Inicializa un proveedor de transporte para su funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="1da65-105">Initializes a transport provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1da65-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1da65-106">Header file:</span></span>  <br/> |<span data-ttu-id="1da65-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="1da65-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="1da65-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="1da65-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1da65-109">Proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="1da65-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="1da65-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="1da65-110">Called by:</span></span>  <br/> |<span data-ttu-id="1da65-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="1da65-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="1da65-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1da65-112">Parameters</span></span>

 <span data-ttu-id="1da65-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="1da65-113">_hInstance_</span></span>
  
> <span data-ttu-id="1da65-114">[entrada] Instancia de la biblioteca de vínculos dinámicos (DLL) del proveedor de transporte que MAPI usó cuando cargó la DLL.</span><span class="sxs-lookup"><span data-stu-id="1da65-114">[in] The instance of the transport provider's dynamic-link library (DLL) that MAPI used when it loaded the DLL.</span></span>
    
 <span data-ttu-id="1da65-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="1da65-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="1da65-116">[entrada] Puntero a un objeto de asignador de memoria que expone la interfaz OLE **IMalloc.**</span><span class="sxs-lookup"><span data-stu-id="1da65-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="1da65-117">Es posible que el proveedor de transporte necesite usar este método de asignación al trabajar con determinadas interfaces, como **IStream**.</span><span class="sxs-lookup"><span data-stu-id="1da65-117">The transport provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="1da65-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="1da65-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="1da65-119">[entrada] Puntero a la [función MAPIAllocateBuffer,](mapiallocatebuffer.md) que se usará para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="1da65-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="1da65-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="1da65-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="1da65-121">[entrada] Puntero a la [función MAPIAllocateMore,](mapiallocatemore.md) que se usará para asignar memoria adicional.</span><span class="sxs-lookup"><span data-stu-id="1da65-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="1da65-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="1da65-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="1da65-123">[entrada] Puntero a la [función MAPIFreeBuffer,](mapifreebuffer.md) que se usará para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="1da65-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="1da65-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1da65-124">_ulFlags_</span></span>
  
> <span data-ttu-id="1da65-125">[entrada] Máscara de bits de marcas.</span><span class="sxs-lookup"><span data-stu-id="1da65-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="1da65-126">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="1da65-126">The following flag can be set:</span></span>
    
<span data-ttu-id="1da65-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="1da65-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="1da65-128">El proveedor se está cargando en el contexto de un servicio de Windows, un tipo especial de proceso sin acceso a ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1da65-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="1da65-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="1da65-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="1da65-130">[entrada] Número de versión de la interfaz del proveedor de servicios (SPI) que Mapi.dll uso.</span><span class="sxs-lookup"><span data-stu-id="1da65-130">[in] Version number of the service provider interface (SPI) that Mapi.dll uses.</span></span> <span data-ttu-id="1da65-131">Para el número de versión actual, vea el archivo de encabezado Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="1da65-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="1da65-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="1da65-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="1da65-133">[salida] Puntero al número de versión del SPI que usa este proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="1da65-133">[out] Pointer to the version number of the SPI that this transport provider uses.</span></span> 
    
 <span data-ttu-id="1da65-134">_lppXPProvider_</span><span class="sxs-lookup"><span data-stu-id="1da65-134">_lppXPProvider_</span></span>
  
> <span data-ttu-id="1da65-135">[salida] Puntero a un puntero al objeto de proveedor de transporte inicializado.</span><span class="sxs-lookup"><span data-stu-id="1da65-135">[out] Pointer to a pointer to the initialized transport provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1da65-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1da65-136">Return value</span></span>

<span data-ttu-id="1da65-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="1da65-137">S_OK</span></span> 
  
> <span data-ttu-id="1da65-138">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="1da65-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="1da65-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="1da65-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="1da65-140">La versión spi que usa MAPI no es compatible con el SPI que usa este proveedor.</span><span class="sxs-lookup"><span data-stu-id="1da65-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1da65-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1da65-141">Remarks</span></span>

<span data-ttu-id="1da65-142">MAPI llama a la función **XPProviderInit de** punto de entrada para inicializar un proveedor de transporte después de un inicio de sesión de cliente.</span><span class="sxs-lookup"><span data-stu-id="1da65-142">MAPI calls the entry point function **XPProviderInit** to initialize a transport provider following a client logon.</span></span> <span data-ttu-id="1da65-143">**Se llama a XPProviderInit** una vez para cada proveedor de transporte especificado en el perfil del cliente.</span><span class="sxs-lookup"><span data-stu-id="1da65-143">**XPProviderInit** is called once for each transport provider specified in the client's profile.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1da65-144">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="1da65-144">Notes to implementers</span></span>

<span data-ttu-id="1da65-145">Un proveedor de transporte debe **implementar XPProviderInit** como una función de punto de entrada en la DLL del proveedor.</span><span class="sxs-lookup"><span data-stu-id="1da65-145">A transport provider must implement **XPProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="1da65-146">La implementación debe basarse en el prototipo de función **XPPROVIDERINIT,** también especificado en Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="1da65-146">The implementation must be based on the **XPPROVIDERINIT** function prototype, also specified in Mapispi.h.</span></span> <span data-ttu-id="1da65-147">MAPI define **XPPROVIDERINIT para** usar el tipo de llamada de inicialización MAPI estándar, STDMAPIINITCALLTYPE, que hace que **XPProviderInit** siga la convención de llamada CDECL.</span><span class="sxs-lookup"><span data-stu-id="1da65-147">MAPI defines **XPPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **XPProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="1da65-148">Una ventaja de CDECL es que las llamadas se pueden intentar incluso si el número de parámetros de llamada no coincide con el número de parámetros definidos.</span><span class="sxs-lookup"><span data-stu-id="1da65-148">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="1da65-149">Un proveedor se puede inicializar varias veces como resultado de aparecer en varios perfiles en uso simultáneo o de aparecer más de una vez en el mismo perfil.</span><span class="sxs-lookup"><span data-stu-id="1da65-149">A provider can be initialized multiple times as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="1da65-150">Dado que el objeto de proveedor contiene contexto, **XPProviderInit** debe devolver un objeto de proveedor diferente en  _lppXPProvider para_ cada inicialización, incluso para varias inicializaciones en el mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="1da65-150">Because the provider object contains context, **XPProviderInit** must return a different provider object in  _lppXPProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="1da65-151">El proveedor de transporte debe usar las funciones a las que  _apuntan lpAllocateBuffer_,  _lpAllocateMore_ y  _lpFreeBuffer_ para la mayor parte de la asignación y desasignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="1da65-151">The transport provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="1da65-152">En particular, el proveedor debe usar estas funciones para asignar memoria para que las usen las aplicaciones cliente al llamar a interfaces de objetos como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="1da65-152">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="1da65-153">Si el proveedor también espera usar el asignador de memoria OLE, debe llamar al método **IUnknown::AddRef** del objeto de asignador al que apunta el parámetro _lpMalloc._</span><span class="sxs-lookup"><span data-stu-id="1da65-153">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="1da65-154">Para obtener más información acerca de cómo escribir **XPProviderInit**, vea [Inicializar el proveedor de transporte.](initializing-the-transport-provider.md)</span><span class="sxs-lookup"><span data-stu-id="1da65-154">For more information about writing **XPProviderInit**, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span> <span data-ttu-id="1da65-155">Para obtener más información acerca de las funciones de punto de entrada, vea Implementar una función de punto de entrada [del proveedor de servicios.](implementing-a-service-provider-entry-point-function.md)</span><span class="sxs-lookup"><span data-stu-id="1da65-155">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1da65-156">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1da65-156">See also</span></span>



[<span data-ttu-id="1da65-157">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="1da65-157">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="1da65-158">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1da65-158">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)
  
[<span data-ttu-id="1da65-159">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="1da65-159">MSProviderInit</span></span>](msproviderinit.md)

