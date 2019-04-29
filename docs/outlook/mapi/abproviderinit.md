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
# <a name="abproviderinit"></a><span data-ttu-id="33a92-103">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="33a92-103">ABProviderInit</span></span>
 
<span data-ttu-id="33a92-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33a92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33a92-105">Inicializa un proveedor de libreta de direcciones para la operación.</span><span class="sxs-lookup"><span data-stu-id="33a92-105">Initializes an address book provider for operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="33a92-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="33a92-106">Header file:</span></span>  <br/> |<span data-ttu-id="33a92-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="33a92-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="33a92-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="33a92-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="33a92-109">Proveedores de libretas de direcciones</span><span class="sxs-lookup"><span data-stu-id="33a92-109">Address book providers</span></span>  <br/> |
|<span data-ttu-id="33a92-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="33a92-110">Called by:</span></span>  <br/> |<span data-ttu-id="33a92-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="33a92-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="33a92-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="33a92-112">Parameters</span></span>

 <span data-ttu-id="33a92-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="33a92-113">_hInstance_</span></span>
  
> <span data-ttu-id="33a92-114">a La instancia de la biblioteca de vínculos dinámicos (DLL) del proveedor de la libreta de direcciones que MAPI usó cuando se vinculó.</span><span class="sxs-lookup"><span data-stu-id="33a92-114">[in] The instance of the address book provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="33a92-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="33a92-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="33a92-116">a Puntero a un objeto de asignador de memoria que expone la interfaz OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="33a92-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="33a92-117">Es posible que el proveedor de la libreta de direcciones necesite usar este método de asignación al trabajar con determinadas interfaces, como **IStream**.</span><span class="sxs-lookup"><span data-stu-id="33a92-117">The address book provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="33a92-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="33a92-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="33a92-119">a Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará en el caso de que MAPI solicite para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="33a92-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used where required by MAPI to allocate memory.</span></span> 
    
 <span data-ttu-id="33a92-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="33a92-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="33a92-121">a Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) , que se usará cuando sea necesario para la asignación de memoria adicional por parte de MAPI.</span><span class="sxs-lookup"><span data-stu-id="33a92-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used where required by MAPI to allocate additional memory.</span></span> 
    
 <span data-ttu-id="33a92-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="33a92-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="33a92-123">a Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará en el caso de que MAPI necesite para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="33a92-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used where required by MAPI to free memory.</span></span> 
    
 <span data-ttu-id="33a92-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="33a92-124">_ulFlags_</span></span>
  
> <span data-ttu-id="33a92-125">a Máscara de máscara de marcas.</span><span class="sxs-lookup"><span data-stu-id="33a92-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="33a92-126">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="33a92-126">The following flag can be set:</span></span>
    
<span data-ttu-id="33a92-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="33a92-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="33a92-128">El proveedor se está cargando en el contexto de un servicio de Windows, un tipo especial de proceso sin acceso a ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="33a92-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="33a92-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="33a92-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="33a92-130">a Número de versión de la interfaz del proveedor de servicios (SPI) que MAPI. DLL usa.</span><span class="sxs-lookup"><span data-stu-id="33a92-130">[in] Version number of the service provider interface (SPI) that MAPI.DLL uses.</span></span> <span data-ttu-id="33a92-131">Para el número de versión actual, vea el MAPISPI. H archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="33a92-131">For the current version number, see the MAPISPI.H header file.</span></span> 
    
 <span data-ttu-id="33a92-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="33a92-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="33a92-133">contempla Puntero al número de versión del SPI que usa este proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="33a92-133">[out] Pointer to the version number of the SPI that this address book provider uses.</span></span> 
    
 <span data-ttu-id="33a92-134">_lppABProvider_</span><span class="sxs-lookup"><span data-stu-id="33a92-134">_lppABProvider_</span></span>
  
> <span data-ttu-id="33a92-135">contempla Puntero a un puntero al objeto proveedor de la libreta de direcciones inicializado.</span><span class="sxs-lookup"><span data-stu-id="33a92-135">[out] Pointer to a pointer to the initialized address book provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="33a92-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33a92-136">Return value</span></span>

<span data-ttu-id="33a92-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="33a92-137">S_OK</span></span> 
  
> <span data-ttu-id="33a92-138">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="33a92-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="33a92-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="33a92-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="33a92-140">La versión de SPI que usa MAPI no es compatible con el SPI que usa este proveedor.</span><span class="sxs-lookup"><span data-stu-id="33a92-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="33a92-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="33a92-141">Remarks</span></span>

<span data-ttu-id="33a92-142">MAPI llama a la función de punto de entrada **ABProviderInit** para inicializar un proveedor de libreta de direcciones siguiendo un inicio de sesión de cliente.</span><span class="sxs-lookup"><span data-stu-id="33a92-142">MAPI calls the entry point function **ABProviderInit** to initialize an address book provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="33a92-143">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="33a92-143">Notes to implementers</span></span>

<span data-ttu-id="33a92-144">Un proveedor de libreta de direcciones debe implementar **ABProviderInit** como una función de punto de entrada en el archivo DLL del proveedor.</span><span class="sxs-lookup"><span data-stu-id="33a92-144">An address book provider must implement **ABProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="33a92-145">La implementación debe basarse en el prototipo de función **ABPROVIDERINIT** , también especificado en MAPISPI. H.</span><span class="sxs-lookup"><span data-stu-id="33a92-145">The implementation must be based on the **ABPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="33a92-146">MAPI define **ABPROVIDERINIT** para usar el tipo de llamada de inicialización MAPI estándar, STDMAPIINITCALLTYPE, que hace que **ABPROVIDERINIT** siga la Convención de llamada Cdecl.</span><span class="sxs-lookup"><span data-stu-id="33a92-146">MAPI defines **ABPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **ABProviderInit** to follow the CDECL calling convention.</span></span> 
  
<span data-ttu-id="33a92-147">Un proveedor se puede inicializar varias veces, como resultado de aparecer en varios perfiles en uso simultáneo o de aparecer más de una vez en el mismo perfil.</span><span class="sxs-lookup"><span data-stu-id="33a92-147">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="33a92-148">Debido a que el objeto de proveedor contiene contexto, **ABProviderInit** debe devolver un objeto de proveedor diferente en _lppABProvider_ para cada inicialización, incluso para varias inicializaciones en el mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="33a92-148">Because the provider object contains context, **ABProviderInit** must return a different provider object in  _lppABProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="33a92-149">El proveedor de la libreta de direcciones debe usar las funciones a las que apunta _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ para la mayor parte de la asignación y desasignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="33a92-149">The address book provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="33a92-150">En concreto, el proveedor debe usar estas funciones para asignar memoria para que la usen las aplicaciones cliente al llamar a interfaces de objeto como [IMAPIProp:: GetProps](imapiprop-getprops.md) y [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="33a92-150">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="33a92-151">Si el proveedor también espera utilizar el asignador de memoria OLE, debe llamar al método **IUnknown:: AddRef** del objeto de asignador al que señala el parámetro _lpMalloc_ .</span><span class="sxs-lookup"><span data-stu-id="33a92-151">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="33a92-152">Para obtener más información sobre cómo escribir **ABProviderInit**, consulte [implementar una función de punto de entrada de proveedor de libreta de direcciones](implementing-an-address-book-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="33a92-152">For more information on writing **ABProviderInit**, see [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md).</span></span> <span data-ttu-id="33a92-153">Para obtener más información acerca de las funciones de punto de entrada, vea [implementar una función de punto de entrada de proveedor de servicios](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="33a92-153">For more information on entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="33a92-154">Ver también</span><span class="sxs-lookup"><span data-stu-id="33a92-154">See also</span></span>

- [<span data-ttu-id="33a92-155">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="33a92-155">IABProvider : IUnknown</span></span>](iabprovideriunknown.md) 
- [<span data-ttu-id="33a92-156">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="33a92-156">MSProviderInit</span></span>](msproviderinit.md)
- [<span data-ttu-id="33a92-157">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="33a92-157">XPProviderInit</span></span>](xpproviderinit.md)

