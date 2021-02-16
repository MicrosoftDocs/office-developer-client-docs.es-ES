---
title: ABProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ABProviderInit
api_type:
- HeaderDef
ms.assetid: c3dcd0d4-018a-47b0-b040-227034ed59d8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: acec07df0b72685cf9ec6b21499c730b72f58c59
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428287"
---
# <a name="abproviderinit"></a><span data-ttu-id="4c079-103">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="4c079-103">ABProviderInit</span></span>
 
<span data-ttu-id="4c079-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c079-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c079-105">Inicializa un proveedor de libreta de direcciones para su funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="4c079-105">Initializes an address book provider for operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c079-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4c079-106">Header file:</span></span>  <br/> |<span data-ttu-id="4c079-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="4c079-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="4c079-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="4c079-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4c079-109">Proveedores de libretas de direcciones</span><span class="sxs-lookup"><span data-stu-id="4c079-109">Address book providers</span></span>  <br/> |
|<span data-ttu-id="4c079-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="4c079-110">Called by:</span></span>  <br/> |<span data-ttu-id="4c079-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="4c079-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT ABProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPABPROVIDER FAR * lppABProvider
);
```

## <a name="parameters"></a><span data-ttu-id="4c079-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c079-112">Parameters</span></span>

 <span data-ttu-id="4c079-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="4c079-113">_hInstance_</span></span>
  
> <span data-ttu-id="4c079-114">[entrada] Instancia de la biblioteca de vínculos dinámicos (DLL) del proveedor de libreta de direcciones que MAPI usó cuando se vinculó.</span><span class="sxs-lookup"><span data-stu-id="4c079-114">[in] The instance of the address book provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="4c079-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="4c079-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="4c079-116">[entrada] Puntero a un objeto de asignador de memoria que expone la interfaz OLE **IMalloc.**</span><span class="sxs-lookup"><span data-stu-id="4c079-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="4c079-117">Es posible que el proveedor de libreta de direcciones necesite usar este método de asignación al trabajar con determinadas interfaces, como **IStream**.</span><span class="sxs-lookup"><span data-stu-id="4c079-117">The address book provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="4c079-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="4c079-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="4c079-119">[entrada] Puntero a la [función MAPIAllocateBuffer,](mapiallocatebuffer.md) que se usará cuando lo requiera MAPI para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="4c079-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used where required by MAPI to allocate memory.</span></span> 
    
 <span data-ttu-id="4c079-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="4c079-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="4c079-121">[entrada] Puntero a la [función MAPIAllocateMore,](mapiallocatemore.md) que se usará cuando mapi lo requiera para asignar memoria adicional.</span><span class="sxs-lookup"><span data-stu-id="4c079-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used where required by MAPI to allocate additional memory.</span></span> 
    
 <span data-ttu-id="4c079-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="4c079-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="4c079-123">[entrada] Puntero a la [función MAPIFreeBuffer,](mapifreebuffer.md) que se usará cuando MAPI lo requiera para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="4c079-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used where required by MAPI to free memory.</span></span> 
    
 <span data-ttu-id="4c079-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4c079-124">_ulFlags_</span></span>
  
> <span data-ttu-id="4c079-125">[entrada] Máscara de bits de marcas.</span><span class="sxs-lookup"><span data-stu-id="4c079-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="4c079-126">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="4c079-126">The following flag can be set:</span></span>
    
<span data-ttu-id="4c079-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="4c079-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="4c079-128">El proveedor se carga en el contexto de un servicio de Windows, un tipo especial de proceso sin acceso a ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4c079-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="4c079-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="4c079-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="4c079-130">[entrada] Número de versión de la interfaz del proveedor de servicios (SPI) que MAPI.DLL uso.</span><span class="sxs-lookup"><span data-stu-id="4c079-130">[in] Version number of the service provider interface (SPI) that MAPI.DLL uses.</span></span> <span data-ttu-id="4c079-131">Para el número de versión actual, vea MAPISPI. Archivo de encabezado H.</span><span class="sxs-lookup"><span data-stu-id="4c079-131">For the current version number, see the MAPISPI.H header file.</span></span> 
    
 <span data-ttu-id="4c079-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="4c079-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="4c079-133">[salida] Puntero al número de versión del SPI que usa este proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4c079-133">[out] Pointer to the version number of the SPI that this address book provider uses.</span></span> 
    
 <span data-ttu-id="4c079-134">_lppABProvider_</span><span class="sxs-lookup"><span data-stu-id="4c079-134">_lppABProvider_</span></span>
  
> <span data-ttu-id="4c079-135">[salida] Puntero a un puntero al objeto de proveedor de libreta de direcciones inicializado.</span><span class="sxs-lookup"><span data-stu-id="4c079-135">[out] Pointer to a pointer to the initialized address book provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4c079-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c079-136">Return value</span></span>

<span data-ttu-id="4c079-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="4c079-137">S_OK</span></span> 
  
> <span data-ttu-id="4c079-138">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="4c079-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="4c079-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="4c079-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="4c079-140">La versión spi que usa MAPI no es compatible con el SPI que usa este proveedor.</span><span class="sxs-lookup"><span data-stu-id="4c079-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4c079-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4c079-141">Remarks</span></span>

<span data-ttu-id="4c079-142">MAPI llama a la función de punto de **entrada ABProviderInit para** inicializar un proveedor de libreta de direcciones después de un inicio de sesión de cliente.</span><span class="sxs-lookup"><span data-stu-id="4c079-142">MAPI calls the entry point function **ABProviderInit** to initialize an address book provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4c079-143">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="4c079-143">Notes to implementers</span></span>

<span data-ttu-id="4c079-144">Un proveedor de libreta de direcciones debe implementar **ABProviderInit** como una función de punto de entrada en la DLL del proveedor.</span><span class="sxs-lookup"><span data-stu-id="4c079-144">An address book provider must implement **ABProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="4c079-145">La implementación debe basarse en el prototipo de función **ABPROVIDERINIT,** también especificado en MAPISPI.H.</span><span class="sxs-lookup"><span data-stu-id="4c079-145">The implementation must be based on the **ABPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="4c079-146">MAPI define **ABPROVIDERINIT para** usar el tipo de llamada de inicialización ESTÁNDAR DE MAPI, STDMAPIINITCALLTYPE, que hace que **ABProviderInit** siga la convención de llamada CDECL.</span><span class="sxs-lookup"><span data-stu-id="4c079-146">MAPI defines **ABPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **ABProviderInit** to follow the CDECL calling convention.</span></span> 
  
<span data-ttu-id="4c079-147">Un proveedor se puede inicializar varias veces, como resultado de aparecer en varios perfiles en uso simultáneo o de aparecer más de una vez en el mismo perfil.</span><span class="sxs-lookup"><span data-stu-id="4c079-147">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="4c079-148">Dado que el objeto de proveedor contiene contexto, **ABProviderInit** debe devolver un objeto de proveedor diferente en  _lppABProvider_ para cada inicialización, incluso para varias inicializaciones en el mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="4c079-148">Because the provider object contains context, **ABProviderInit** must return a different provider object in  _lppABProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="4c079-149">El proveedor de libreta de direcciones debe usar las funciones a las que  _apuntan lpAllocateBuffer_,  _lpAllocateMore_ y  _lpFreeBuffer_ para la mayor parte de la asignación y desasignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="4c079-149">The address book provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="4c079-150">En particular, el proveedor debe usar estas funciones para asignar memoria para su uso por parte de las aplicaciones cliente al llamar a interfaces de objetos como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="4c079-150">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="4c079-151">Si el proveedor también espera usar el asignador de memoria OLE, debe llamar al método **IUnknown::AddRef** del objeto de asignador al que apunta el parámetro _lpMalloc._</span><span class="sxs-lookup"><span data-stu-id="4c079-151">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="4c079-152">Para obtener más información sobre cómo escribir **ABProviderInit**, vea Implementar una función de punto de entrada [del proveedor de libreta de direcciones.](implementing-an-address-book-provider-entry-point-function.md)</span><span class="sxs-lookup"><span data-stu-id="4c079-152">For more information on writing **ABProviderInit**, see [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md).</span></span> <span data-ttu-id="4c079-153">Para obtener más información acerca de las funciones de punto de entrada, vea Implementar una función de punto de [entrada del proveedor de servicios.](implementing-a-service-provider-entry-point-function.md)</span><span class="sxs-lookup"><span data-stu-id="4c079-153">For more information on entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4c079-154">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4c079-154">See also</span></span>

- [<span data-ttu-id="4c079-155">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4c079-155">IABProvider : IUnknown</span></span>](iabprovideriunknown.md) 
- [<span data-ttu-id="4c079-156">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="4c079-156">MSProviderInit</span></span>](msproviderinit.md)
- [<span data-ttu-id="4c079-157">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="4c079-157">XPProviderInit</span></span>](xpproviderinit.md)

