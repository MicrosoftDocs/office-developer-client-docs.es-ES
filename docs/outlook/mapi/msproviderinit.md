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
ms.openlocfilehash: 33adef7a8248e137869912afc2026583828b087e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570173"
---
# <a name="msproviderinit"></a><span data-ttu-id="1a9f1-103">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="1a9f1-103">MSProviderInit</span></span>

  
  
<span data-ttu-id="1a9f1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a9f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a9f1-105">Inicializa un proveedor de almacén de mensajes para la operación.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-105">Initializes a message store provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a9f1-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1a9f1-106">Header file:</span></span>  <br/> |<span data-ttu-id="1a9f1-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="1a9f1-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="1a9f1-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="1a9f1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1a9f1-109">Proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="1a9f1-109">Message store providers</span></span>  <br/> |
|<span data-ttu-id="1a9f1-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="1a9f1-110">Called by:</span></span>  <br/> |<span data-ttu-id="1a9f1-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="1a9f1-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="1a9f1-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a9f1-112">Parameters</span></span>

 <span data-ttu-id="1a9f1-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="1a9f1-113">_hInstance_</span></span>
  
> <span data-ttu-id="1a9f1-114">[entrada] La instancia del mensaje almacén de biblioteca de vínculos dinámicos (DLL) del proveedor que MAPI utiliza cuando vincula.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-114">[in] The instance of the message store provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="1a9f1-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="1a9f1-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="1a9f1-116">[entrada] Puntero a un objeto del asignador de memoria exposición de la interfaz de OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="1a9f1-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="1a9f1-117">El proveedor de almacén de mensajes es posible que necesite utilizar este método de asignación cuando se trabaja con ciertas interfaces como **IStream**.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-117">The message store provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="1a9f1-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="1a9f1-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="1a9f1-119">[entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="1a9f1-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="1a9f1-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="1a9f1-121">[entrada] Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) , que se usará para asignar memoria adicional.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="1a9f1-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="1a9f1-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="1a9f1-123">[entrada] Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="1a9f1-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1a9f1-124">_ulFlags_</span></span>
  
> <span data-ttu-id="1a9f1-125">[entrada] Máscara de bits de indicadores.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="1a9f1-126">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="1a9f1-126">The following flag can be set:</span></span>
    
<span data-ttu-id="1a9f1-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="1a9f1-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="1a9f1-128">Se está cargando el proveedor en el contexto de un servicio de Windows, un tipo especial de proceso sin acceso a cualquier interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="1a9f1-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="1a9f1-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="1a9f1-130">[entrada] Número de versión de la interfaz de proveedor de servicio (SPI) que usa MAPI.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-130">[in] Version number of the service provider interface (SPI) that MAPI uses.</span></span> <span data-ttu-id="1a9f1-131">Para el número de versión actual, vea el archivo de encabezado Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="1a9f1-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="1a9f1-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="1a9f1-133">[out] Puntero al número de versión de la SPI que usa este proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-133">[out] Pointer to the version number of the SPI that this message store provider uses.</span></span> 
    
 <span data-ttu-id="1a9f1-134">_lppMSProvider_</span><span class="sxs-lookup"><span data-stu-id="1a9f1-134">_lppMSProvider_</span></span>
  
> <span data-ttu-id="1a9f1-135">[out] Puntero a un puntero para el objeto de proveedor de almacén de mensajes inicializada.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-135">[out] Pointer to a pointer to the initialized message store provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1a9f1-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a9f1-136">Return value</span></span>

<span data-ttu-id="1a9f1-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="1a9f1-137">S_OK</span></span> 
  
> <span data-ttu-id="1a9f1-138">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="1a9f1-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="1a9f1-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="1a9f1-140">La versión SPI usada por MAPI no es compatible con el SPI usado por este proveedor.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1a9f1-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1a9f1-141">Remarks</span></span>

<span data-ttu-id="1a9f1-142">MAPI llama a la función de punto de entrada **MSProviderInit** para inicializar un proveedor de almacén de mensajes sigue un inicio de sesión de cliente.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-142">MAPI calls the entry point function **MSProviderInit** to initialize a message store provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1a9f1-143">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="1a9f1-143">Notes to implementers</span></span>

<span data-ttu-id="1a9f1-144">Un proveedor de almacén de mensajes debe implementar **MSProviderInit** como una función de punto de entrada en el archivo DLL del proveedor.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-144">A message store provider must implement **MSProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="1a9f1-145">La implementación debe basarse en el prototipo de función **MSPROVIDERINIT** , también especificado en MAPISPI. H.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-145">The implementation must be based on the **MSPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="1a9f1-146">MAPI define **MSPROVIDERINIT** para usar el tipo de llamada de inicialización estándar MAPI, STDMAPIINITCALLTYPE, que hace que **MSProviderInit** que se deben seguir la convención de llamada CDECL.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-146">MAPI defines **MSPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **MSProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="1a9f1-147">Una ventaja de CDECL es que se pueden intentar llamadas incluso si el número de parámetros de llamada no coincide con el número de parámetros definidos.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-147">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="1a9f1-148">Se puede inicializar un proveedor de varias veces, como consecuencia de que aparezca en varios perfiles en uso simultáneo o de aparecer más de una vez en el mismo perfil.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-148">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="1a9f1-149">Debido a que el objeto de proveedor contiene contexto, **MSProviderInit** debe devolver un objeto de proveedor diferente en _lppMSProvider_ para cada inicialización, incluso para varias inicializaciones en el mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-149">Because the provider object contains context, **MSProviderInit** must return a different provider object in  _lppMSProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="1a9f1-150">No se debe vincular el archivo DLL del proveedor con Mapix.dll.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-150">The provider DLL should not be linked with Mapix.dll.</span></span> <span data-ttu-id="1a9f1-151">En su lugar, debe utilizar estos punteros para la asignación de memoria o cancelación.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-151">Instead, it should use these pointers for memory allocation or deallocation.</span></span> 
  
<span data-ttu-id="1a9f1-152">El proveedor de almacén de mensajes debe usar las funciones que señala _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ para la mayoría de asignación de memoria y cancelación de asignación.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-152">The message store provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="1a9f1-153">En concreto, el proveedor debe usar estas funciones para asignar la memoria para su uso por las aplicaciones cliente al llamar a las interfaces de objeto como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="1a9f1-153">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="1a9f1-154">Si el proveedor también espera utilizar el asignador de memoria OLE, debe llamar al método **IUnknown:: AddRef** del objeto asignador indicado por el parámetro _lpMalloc_ .</span><span class="sxs-lookup"><span data-stu-id="1a9f1-154">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="1a9f1-155">Para obtener más información acerca de cómo escribir **MSProviderInit**, vea [Cargar los proveedores de almacén de mensajes](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="1a9f1-155">For more information about writing **MSProviderInit**, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span> <span data-ttu-id="1a9f1-156">Para obtener más información acerca de las funciones de punto de entrada, vea [implementar una función de punto de servicio de proveedor de entrada](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="1a9f1-156">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1a9f1-157">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="1a9f1-157">See also</span></span>



[<span data-ttu-id="1a9f1-158">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="1a9f1-158">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="1a9f1-159">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1a9f1-159">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)
  
[<span data-ttu-id="1a9f1-160">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="1a9f1-160">XPProviderInit</span></span>](xpproviderinit.md)

