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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: cf1febe89c49b29cdfaf8d27760c4fb27b4c4990
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818409"
---
# <a name="msproviderinit"></a><span data-ttu-id="e0b38-103">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="e0b38-103">MSProviderInit</span></span>

  
  
<span data-ttu-id="e0b38-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e0b38-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e0b38-105">Inicializa un proveedor de almacén de mensajes para la operación.</span><span class="sxs-lookup"><span data-stu-id="e0b38-105">Initializes a message store provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e0b38-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e0b38-106">Header file:</span></span>  <br/> |<span data-ttu-id="e0b38-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="e0b38-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="e0b38-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="e0b38-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e0b38-109">Proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="e0b38-109">Message store providers</span></span>  <br/> |
|<span data-ttu-id="e0b38-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e0b38-110">Called by:</span></span>  <br/> |<span data-ttu-id="e0b38-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="e0b38-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="e0b38-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0b38-112">Parameters</span></span>

 <span data-ttu-id="e0b38-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="e0b38-113">_hInstance_</span></span>
  
> <span data-ttu-id="e0b38-114">[entrada] La instancia del mensaje almacén de biblioteca de vínculos dinámicos (DLL) del proveedor que MAPI utiliza cuando vincula.</span><span class="sxs-lookup"><span data-stu-id="e0b38-114">[in] The instance of the message store provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="e0b38-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="e0b38-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="e0b38-116">[entrada] Puntero a un objeto del asignador de memoria exposición de la interfaz de OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="e0b38-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="e0b38-117">El proveedor de almacén de mensajes es posible que necesite utilizar este método de asignación cuando se trabaja con ciertas interfaces como **IStream**.</span><span class="sxs-lookup"><span data-stu-id="e0b38-117">The message store provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="e0b38-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="e0b38-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="e0b38-119">[entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="e0b38-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="e0b38-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="e0b38-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="e0b38-121">[entrada] Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) , que se usará para asignar memoria adicional.</span><span class="sxs-lookup"><span data-stu-id="e0b38-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="e0b38-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="e0b38-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="e0b38-123">[entrada] Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="e0b38-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="e0b38-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e0b38-124">_ulFlags_</span></span>
  
> <span data-ttu-id="e0b38-125">[entrada] Máscara de bits de indicadores.</span><span class="sxs-lookup"><span data-stu-id="e0b38-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="e0b38-126">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="e0b38-126">The following flag can be set:</span></span>
    
<span data-ttu-id="e0b38-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="e0b38-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="e0b38-128">Se está cargando el proveedor en el contexto de un servicio de Windows, un tipo especial de proceso sin acceso a cualquier interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e0b38-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="e0b38-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="e0b38-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="e0b38-130">[entrada] Número de versión de la interfaz de proveedor de servicio (SPI) que usa MAPI.</span><span class="sxs-lookup"><span data-stu-id="e0b38-130">[in] Version number of the service provider interface (SPI) that MAPI uses.</span></span> <span data-ttu-id="e0b38-131">Para el número de versión actual, vea el archivo de encabezado Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="e0b38-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="e0b38-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="e0b38-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="e0b38-133">[out] Puntero al número de versión de la SPI que usa este proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e0b38-133">[out] Pointer to the version number of the SPI that this message store provider uses.</span></span> 
    
 <span data-ttu-id="e0b38-134">_lppMSProvider_</span><span class="sxs-lookup"><span data-stu-id="e0b38-134">_lppMSProvider_</span></span>
  
> <span data-ttu-id="e0b38-135">[out] Puntero a un puntero para el objeto de proveedor de almacén de mensajes inicializada.</span><span class="sxs-lookup"><span data-stu-id="e0b38-135">[out] Pointer to a pointer to the initialized message store provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e0b38-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0b38-136">Return value</span></span>

<span data-ttu-id="e0b38-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="e0b38-137">S_OK</span></span> 
  
> <span data-ttu-id="e0b38-138">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="e0b38-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="e0b38-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="e0b38-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="e0b38-140">La versión SPI usada por MAPI no es compatible con el SPI usado por este proveedor.</span><span class="sxs-lookup"><span data-stu-id="e0b38-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e0b38-141">Notas</span><span class="sxs-lookup"><span data-stu-id="e0b38-141">Remarks</span></span>

<span data-ttu-id="e0b38-142">MAPI llama a la función de punto de entrada **MSProviderInit** para inicializar un proveedor de almacén de mensajes sigue un inicio de sesión de cliente.</span><span class="sxs-lookup"><span data-stu-id="e0b38-142">MAPI calls the entry point function **MSProviderInit** to initialize a message store provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e0b38-143">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="e0b38-143">Notes to implementers</span></span>

<span data-ttu-id="e0b38-144">Un proveedor de almacén de mensajes debe implementar **MSProviderInit** como una función de punto de entrada en el archivo DLL del proveedor.</span><span class="sxs-lookup"><span data-stu-id="e0b38-144">A message store provider must implement **MSProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="e0b38-145">La implementación debe basarse en el prototipo de función **MSPROVIDERINIT** , también especificado en MAPISPI. H.</span><span class="sxs-lookup"><span data-stu-id="e0b38-145">The implementation must be based on the **MSPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="e0b38-146">MAPI define **MSPROVIDERINIT** para usar el tipo de llamada de inicialización estándar MAPI, STDMAPIINITCALLTYPE, que hace que **MSProviderInit** que se deben seguir la convención de llamada CDECL.</span><span class="sxs-lookup"><span data-stu-id="e0b38-146">MAPI defines **MSPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **MSProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="e0b38-147">Una ventaja de CDECL es que se pueden intentar llamadas incluso si el número de parámetros de llamada no coincide con el número de parámetros definidos.</span><span class="sxs-lookup"><span data-stu-id="e0b38-147">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="e0b38-148">Se puede inicializar un proveedor de varias veces, como consecuencia de que aparezca en varios perfiles en uso simultáneo o de aparecer más de una vez en el mismo perfil.</span><span class="sxs-lookup"><span data-stu-id="e0b38-148">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="e0b38-149">Debido a que el objeto de proveedor contiene contexto, **MSProviderInit** debe devolver un objeto de proveedor diferente en _lppMSProvider_ para cada inicialización, incluso para varias inicializaciones en el mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="e0b38-149">Because the provider object contains context, **MSProviderInit** must return a different provider object in  _lppMSProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="e0b38-150">No se debe vincular el archivo DLL del proveedor con Mapix.dll.</span><span class="sxs-lookup"><span data-stu-id="e0b38-150">The provider DLL should not be linked with Mapix.dll.</span></span> <span data-ttu-id="e0b38-151">En su lugar, debe utilizar estos punteros para la asignación de memoria o cancelación.</span><span class="sxs-lookup"><span data-stu-id="e0b38-151">Instead, it should use these pointers for memory allocation or deallocation.</span></span> 
  
<span data-ttu-id="e0b38-152">El proveedor de almacén de mensajes debe usar las funciones que señala _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ para la mayoría de asignación de memoria y cancelación de asignación.</span><span class="sxs-lookup"><span data-stu-id="e0b38-152">The message store provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="e0b38-153">En concreto, el proveedor debe usar estas funciones para asignar la memoria para su uso por las aplicaciones cliente al llamar a las interfaces de objeto como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="e0b38-153">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="e0b38-154">Si el proveedor también espera utilizar el asignador de memoria OLE, debe llamar al método **IUnknown:: AddRef** del objeto asignador indicado por el parámetro _lpMalloc_ .</span><span class="sxs-lookup"><span data-stu-id="e0b38-154">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="e0b38-155">Para obtener más información acerca de cómo escribir **MSProviderInit**, vea [Cargar los proveedores de almacén de mensajes](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="e0b38-155">For more information about writing **MSProviderInit**, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span> <span data-ttu-id="e0b38-156">Para obtener más información acerca de las funciones de punto de entrada, vea [implementar una función de punto de servicio de proveedor de entrada](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="e0b38-156">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e0b38-157">Ver también</span><span class="sxs-lookup"><span data-stu-id="e0b38-157">See also</span></span>



[<span data-ttu-id="e0b38-158">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="e0b38-158">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="e0b38-159">IMSProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0b38-159">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)
  
[<span data-ttu-id="e0b38-160">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="e0b38-160">XPProviderInit</span></span>](xpproviderinit.md)

