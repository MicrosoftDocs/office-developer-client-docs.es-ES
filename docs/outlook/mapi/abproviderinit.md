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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 03375a11be3f6f128db5f6147c5fbe901d0a0fa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816367"
---
# <a name="abproviderinit"></a><span data-ttu-id="64128-103">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="64128-103">ABProviderInit</span></span>
 
<span data-ttu-id="64128-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="64128-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="64128-105">Inicializa un proveedor de la libreta de direcciones para la operación.</span><span class="sxs-lookup"><span data-stu-id="64128-105">Initializes an address book provider for operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="64128-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="64128-106">Header file:</span></span>  <br/> |<span data-ttu-id="64128-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="64128-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="64128-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="64128-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="64128-109">Proveedores de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="64128-109">Address book providers</span></span>  <br/> |
|<span data-ttu-id="64128-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="64128-110">Called by:</span></span>  <br/> |<span data-ttu-id="64128-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="64128-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="64128-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64128-112">Parameters</span></span>

 <span data-ttu-id="64128-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="64128-113">_hInstance_</span></span>
  
> <span data-ttu-id="64128-114">[entrada] La instancia de la biblioteca de vínculos dinámicos (DLL) del proveedor de libreta de direcciones que MAPI utiliza cuando vincula.</span><span class="sxs-lookup"><span data-stu-id="64128-114">[in] The instance of the address book provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="64128-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="64128-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="64128-116">[entrada] Puntero a un objeto del asignador de memoria exposición de la interfaz de OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="64128-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="64128-117">El proveedor de la libreta de direcciones que necesite utilizar este método de asignación cuando se trabaja con ciertas interfaces como **IStream**.</span><span class="sxs-lookup"><span data-stu-id="64128-117">The address book provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="64128-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="64128-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="64128-119">[entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se utilizará cuando sea necesario por MAPI para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="64128-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used where required by MAPI to allocate memory.</span></span> 
    
 <span data-ttu-id="64128-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="64128-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="64128-121">[entrada] Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) , que se utilizará cuando sea necesario por MAPI para asignar memoria adicional.</span><span class="sxs-lookup"><span data-stu-id="64128-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used where required by MAPI to allocate additional memory.</span></span> 
    
 <span data-ttu-id="64128-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="64128-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="64128-123">[entrada] Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará cuando sea necesario por MAPI para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="64128-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used where required by MAPI to free memory.</span></span> 
    
 <span data-ttu-id="64128-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="64128-124">_ulFlags_</span></span>
  
> <span data-ttu-id="64128-125">[entrada] Máscara de bits de indicadores.</span><span class="sxs-lookup"><span data-stu-id="64128-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="64128-126">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="64128-126">The following flag can be set:</span></span>
    
<span data-ttu-id="64128-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="64128-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="64128-128">Se está cargando el proveedor en el contexto de un servicio de Windows, un tipo especial de proceso sin acceso a cualquier interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="64128-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="64128-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="64128-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="64128-130">[entrada] Número de versión de la interfaz de proveedor de servicios (SPI) que MAPI. Se utiliza el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="64128-130">[in] Version number of the service provider interface (SPI) that MAPI.DLL uses.</span></span> <span data-ttu-id="64128-131">Para el número de versión actual, vea la MAPISPI. Archivo de encabezado H.</span><span class="sxs-lookup"><span data-stu-id="64128-131">For the current version number, see the MAPISPI.H header file.</span></span> 
    
 <span data-ttu-id="64128-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="64128-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="64128-133">[out] Puntero al número de versión de la SPI que usa este proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="64128-133">[out] Pointer to the version number of the SPI that this address book provider uses.</span></span> 
    
 <span data-ttu-id="64128-134">_lppABProvider_</span><span class="sxs-lookup"><span data-stu-id="64128-134">_lppABProvider_</span></span>
  
> <span data-ttu-id="64128-135">[out] Puntero a un puntero para el objeto de proveedor de la libreta de direcciones inicializado.</span><span class="sxs-lookup"><span data-stu-id="64128-135">[out] Pointer to a pointer to the initialized address book provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="64128-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64128-136">Return value</span></span>

<span data-ttu-id="64128-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="64128-137">S_OK</span></span> 
  
> <span data-ttu-id="64128-138">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="64128-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="64128-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="64128-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="64128-140">La versión SPI usada por MAPI no es compatible con el SPI usado por este proveedor.</span><span class="sxs-lookup"><span data-stu-id="64128-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="64128-141">Notas</span><span class="sxs-lookup"><span data-stu-id="64128-141">Remarks</span></span>

<span data-ttu-id="64128-142">MAPI llama a la función de punto de entrada **ABProviderInit** para inicializar un proveedor de la libreta de direcciones siguiendo un inicio de sesión de cliente.</span><span class="sxs-lookup"><span data-stu-id="64128-142">MAPI calls the entry point function **ABProviderInit** to initialize an address book provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="64128-143">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="64128-143">Notes to implementers</span></span>

<span data-ttu-id="64128-144">Un proveedor de la libreta de direcciones debe implementar **ABProviderInit** como una función de punto de entrada en el archivo DLL del proveedor.</span><span class="sxs-lookup"><span data-stu-id="64128-144">An address book provider must implement **ABProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="64128-145">La implementación debe basarse en el prototipo de función **ABPROVIDERINIT** , también especificado en MAPISPI. H.</span><span class="sxs-lookup"><span data-stu-id="64128-145">The implementation must be based on the **ABPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="64128-146">MAPI define **ABPROVIDERINIT** para usar el tipo de llamada de inicialización estándar MAPI, STDMAPIINITCALLTYPE, que hace que **ABProviderInit** que se deben seguir la convención de llamada CDECL.</span><span class="sxs-lookup"><span data-stu-id="64128-146">MAPI defines **ABPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **ABProviderInit** to follow the CDECL calling convention.</span></span> 
  
<span data-ttu-id="64128-147">Se puede inicializar un proveedor de varias veces, como consecuencia de que aparezca en varios perfiles en uso simultáneo o de aparecer más de una vez en el mismo perfil.</span><span class="sxs-lookup"><span data-stu-id="64128-147">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="64128-148">Debido a que el objeto de proveedor contiene contexto, **ABProviderInit** debe devolver un objeto de proveedor diferente en _lppABProvider_ para cada inicialización, incluso para varias inicializaciones en el mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="64128-148">Because the provider object contains context, **ABProviderInit** must return a different provider object in  _lppABProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="64128-149">El proveedor de la libreta de direcciones debe usar las funciones que señala _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ para la mayoría de asignación de memoria y cancelación de asignación.</span><span class="sxs-lookup"><span data-stu-id="64128-149">The address book provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="64128-150">En concreto, el proveedor debe usar estas funciones para asignar la memoria para su uso por las aplicaciones cliente al llamar a las interfaces de objeto como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="64128-150">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="64128-151">Si el proveedor también espera utilizar el asignador de memoria OLE, debe llamar al método **IUnknown:: AddRef** del objeto asignador indicado por el parámetro _lpMalloc_ .</span><span class="sxs-lookup"><span data-stu-id="64128-151">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="64128-152">Para obtener más información sobre cómo escribir **ABProviderInit**, vea [implementar una función de punto de entrada de dirección de la libreta de proveedor](implementing-an-address-book-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="64128-152">For more information on writing **ABProviderInit**, see [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md).</span></span> <span data-ttu-id="64128-153">Para obtener más información sobre las funciones de punto de entrada, vea [implementar una función de punto de servicio de proveedor de entrada](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="64128-153">For more information on entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="64128-154">Ver también</span><span class="sxs-lookup"><span data-stu-id="64128-154">See also</span></span>

- [<span data-ttu-id="64128-155">IABProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="64128-155">IABProvider : IUnknown</span></span>](iabprovideriunknown.md) 
- [<span data-ttu-id="64128-156">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="64128-156">MSProviderInit</span></span>](msproviderinit.md)
- [<span data-ttu-id="64128-157">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="64128-157">XPProviderInit</span></span>](xpproviderinit.md)

