---
title: MSProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MSProviderInit
api_type:
- HeaderDef
ms.assetid: 230c66c4-ab04-4fa6-946f-9f4b704f2842
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9a5f8b44f9d795282ccfd61fd32a306c5478ed21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416240"
---
# <a name="msproviderinit"></a><span data-ttu-id="3730d-103">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="3730d-103">MSProviderInit</span></span>

  
  
<span data-ttu-id="3730d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3730d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3730d-105">Inicializa un proveedor de almacén de mensajes para su operación.</span><span class="sxs-lookup"><span data-stu-id="3730d-105">Initializes a message store provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3730d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="3730d-106">Header file:</span></span>  <br/> |<span data-ttu-id="3730d-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="3730d-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="3730d-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="3730d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3730d-109">Proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="3730d-109">Message store providers</span></span>  <br/> |
|<span data-ttu-id="3730d-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="3730d-110">Called by:</span></span>  <br/> |<span data-ttu-id="3730d-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="3730d-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT MSProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPMSPROVIDER FAR * lppMSProvider
);
```

## <a name="parameters"></a><span data-ttu-id="3730d-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="3730d-112">Parameters</span></span>

 <span data-ttu-id="3730d-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="3730d-113">_hInstance_</span></span>
  
> <span data-ttu-id="3730d-114">[in] Instancia de la biblioteca de vínculos dinámicos (DLL) del proveedor de almacenamiento de mensajes que MAPI usó cuando se vinculó.</span><span class="sxs-lookup"><span data-stu-id="3730d-114">[in] The instance of the message store provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="3730d-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="3730d-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="3730d-116">[in] Puntero a un objeto de asignador de memoria que expone la **interfaz OLE IMalloc.**</span><span class="sxs-lookup"><span data-stu-id="3730d-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="3730d-117">Es posible que el proveedor del almacén de mensajes necesite usar este método de asignación al trabajar con determinadas interfaces, como **IStream**.</span><span class="sxs-lookup"><span data-stu-id="3730d-117">The message store provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="3730d-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="3730d-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="3730d-119">[in] Puntero a la [función MAPIAllocateBuffer,](mapiallocatebuffer.md) que se usará para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="3730d-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="3730d-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="3730d-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="3730d-121">[in] Puntero a la [función MAPIAllocateMore,](mapiallocatemore.md) que se usará para asignar memoria adicional.</span><span class="sxs-lookup"><span data-stu-id="3730d-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="3730d-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="3730d-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="3730d-123">[in] Puntero a la [función MAPIFreeBuffer,](mapifreebuffer.md) que se usará para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="3730d-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="3730d-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3730d-124">_ulFlags_</span></span>
  
> <span data-ttu-id="3730d-125">[in] Máscara de bits de marcas.</span><span class="sxs-lookup"><span data-stu-id="3730d-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="3730d-126">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="3730d-126">The following flag can be set:</span></span>
    
<span data-ttu-id="3730d-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="3730d-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="3730d-128">El proveedor se está cargando en el contexto de un servicio Windows, un tipo especial de proceso sin acceso a ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="3730d-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="3730d-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="3730d-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="3730d-130">[in] Número de versión de la interfaz del proveedor de servicios (SPI) que utiliza MAPI.</span><span class="sxs-lookup"><span data-stu-id="3730d-130">[in] Version number of the service provider interface (SPI) that MAPI uses.</span></span> <span data-ttu-id="3730d-131">Para el número de versión actual, vea el archivo de encabezado Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="3730d-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="3730d-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="3730d-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="3730d-133">[salida] Puntero al número de versión del SPI que usa este proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="3730d-133">[out] Pointer to the version number of the SPI that this message store provider uses.</span></span> 
    
 <span data-ttu-id="3730d-134">_lppMSProvider_</span><span class="sxs-lookup"><span data-stu-id="3730d-134">_lppMSProvider_</span></span>
  
> <span data-ttu-id="3730d-135">[salida] Puntero a un puntero al objeto de proveedor del almacén de mensajes inicializado.</span><span class="sxs-lookup"><span data-stu-id="3730d-135">[out] Pointer to a pointer to the initialized message store provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3730d-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3730d-136">Return value</span></span>

<span data-ttu-id="3730d-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="3730d-137">S_OK</span></span> 
  
> <span data-ttu-id="3730d-138">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="3730d-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="3730d-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="3730d-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="3730d-140">La versión SPI que usa MAPI no es compatible con el SPI que usa este proveedor.</span><span class="sxs-lookup"><span data-stu-id="3730d-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3730d-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3730d-141">Remarks</span></span>

<span data-ttu-id="3730d-142">MAPI llama a la función de punto de entrada **MSProviderInit para** inicializar un proveedor de almacén de mensajes después de un inicio de sesión de cliente.</span><span class="sxs-lookup"><span data-stu-id="3730d-142">MAPI calls the entry point function **MSProviderInit** to initialize a message store provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3730d-143">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="3730d-143">Notes to implementers</span></span>

<span data-ttu-id="3730d-144">Un proveedor de almacén de mensajes debe implementar **MSProviderInit** como una función de punto de entrada en la DLL del proveedor.</span><span class="sxs-lookup"><span data-stu-id="3730d-144">A message store provider must implement **MSProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="3730d-145">La implementación debe basarse en el prototipo de función **MSPROVIDERINIT,** también especificado en MAPISPI.H.</span><span class="sxs-lookup"><span data-stu-id="3730d-145">The implementation must be based on the **MSPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="3730d-146">MAPI define **MSPROVIDERINIT para** usar el tipo de llamada de inicialización MAPI estándar, STDMAPIINITCALLTYPE, lo que hace que **MSProviderInit** siga la convención de llamada CDECL.</span><span class="sxs-lookup"><span data-stu-id="3730d-146">MAPI defines **MSPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **MSProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="3730d-147">Una ventaja de CDECL es que las llamadas se pueden intentar incluso si el número de parámetros de llamada no coincide con el número de parámetros definidos.</span><span class="sxs-lookup"><span data-stu-id="3730d-147">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="3730d-148">Un proveedor se puede inicializar varias veces, como resultado de aparecer en varios perfiles en uso simultáneo o de aparecer más de una vez en el mismo perfil.</span><span class="sxs-lookup"><span data-stu-id="3730d-148">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="3730d-149">Dado que el objeto provider contiene contexto, **MSProviderInit** debe devolver un objeto de proveedor diferente en  _lppMSProvider_ para cada inicialización, incluso para varias inicializaciones en el mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="3730d-149">Because the provider object contains context, **MSProviderInit** must return a different provider object in  _lppMSProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="3730d-150">El DLL del proveedor no debe vincularse con Mapix.dll.</span><span class="sxs-lookup"><span data-stu-id="3730d-150">The provider DLL should not be linked with Mapix.dll.</span></span> <span data-ttu-id="3730d-151">En su lugar, debe usar estos punteros para la asignación de memoria o la desasignación.</span><span class="sxs-lookup"><span data-stu-id="3730d-151">Instead, it should use these pointers for memory allocation or deallocation.</span></span> 
  
<span data-ttu-id="3730d-152">El proveedor del almacén de mensajes debe usar las funciones apuntadas por  _lpAllocateBuffer_,  _lpAllocateMore_ y  _lpFreeBuffer_ para la asignación y desasignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="3730d-152">The message store provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="3730d-153">En particular, el proveedor debe usar estas funciones para asignar memoria para su uso por las aplicaciones cliente al llamar a interfaces de objetos como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="3730d-153">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="3730d-154">Si el proveedor también espera usar el asignador de memoria OLE, debe llamar al método **IUnknown::AddRef** del objeto de asignador al que apunta el parámetro _lpMalloc._</span><span class="sxs-lookup"><span data-stu-id="3730d-154">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="3730d-155">Para obtener más información acerca de cómo **escribir MSProviderInit,** vea [Loading Message Store Providers](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="3730d-155">For more information about writing **MSProviderInit**, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span> <span data-ttu-id="3730d-156">Para obtener más información acerca de las funciones de punto de entrada, vea [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="3730d-156">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3730d-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="3730d-157">See also</span></span>



[<span data-ttu-id="3730d-158">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="3730d-158">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="3730d-159">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3730d-159">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)
  
[<span data-ttu-id="3730d-160">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="3730d-160">XPProviderInit</span></span>](xpproviderinit.md)

