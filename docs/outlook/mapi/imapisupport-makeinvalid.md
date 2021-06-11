---
title: IMAPISupportMakeInvalid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.MakeInvalid
api_type:
- COM
ms.assetid: c630ecaf-b19c-4991-9779-e13cc492c755
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 84e87f8a8d3c419afc4b86e200aeaba57e6a85f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427496"
---
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="a2e39-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="a2e39-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="a2e39-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2e39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2e39-105">Marca un objeto como inutilizable.</span><span class="sxs-lookup"><span data-stu-id="a2e39-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="a2e39-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a2e39-106">Parameters</span></span>

 <span data-ttu-id="a2e39-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a2e39-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a2e39-108">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a2e39-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a2e39-109">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="a2e39-109">_lpObject_</span></span>
  
> <span data-ttu-id="a2e39-110">[in] Puntero al objeto que se va a invalidar.</span><span class="sxs-lookup"><span data-stu-id="a2e39-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="a2e39-111">La interfaz del objeto debe derivarse de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="a2e39-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="a2e39-112">_ulRefCount_</span><span class="sxs-lookup"><span data-stu-id="a2e39-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="a2e39-113">[in] Recuento de referencias actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a2e39-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="a2e39-114">_cMethods_</span><span class="sxs-lookup"><span data-stu-id="a2e39-114">_cMethods_</span></span>
  
> <span data-ttu-id="a2e39-115">[in] Recuento de métodos en la tabla vtable del objeto.</span><span class="sxs-lookup"><span data-stu-id="a2e39-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a2e39-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2e39-116">Return value</span></span>

<span data-ttu-id="a2e39-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="a2e39-117">S_OK</span></span> 
  
> <span data-ttu-id="a2e39-118">El objeto se marcó correctamente como inutilizable.</span><span class="sxs-lookup"><span data-stu-id="a2e39-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a2e39-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a2e39-119">Remarks</span></span>

<span data-ttu-id="a2e39-120">El **método IMAPISupport::MakeInvalid** se implementa para todos los objetos de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="a2e39-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="a2e39-121">El objeto que se va a invalidar debe derivar de la **interfaz IUnknown** o de una interfaz derivada de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="a2e39-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="a2e39-122">**MakeInvalid** marca un objeto como inutilizable reemplazando la tabla vtable del objeto por una tabla vtable auxiliar de tamaño similar en la que los métodos **IUnknown::AddRef** e **IUnknown::Release** realizan el rendimiento esperado.</span><span class="sxs-lookup"><span data-stu-id="a2e39-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="a2e39-123">Sin embargo, cualquier otro método falla, devolviendo el valor MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="a2e39-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a2e39-124">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="a2e39-124">Notes to callers</span></span>

<span data-ttu-id="a2e39-125">Los proveedores de servicios y los servicios de mensajes normalmente llaman **a MakeInvalid en** el momento del apagado.</span><span class="sxs-lookup"><span data-stu-id="a2e39-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="a2e39-126">Sin embargo, se puede llamar a **MakeInvalid** en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="a2e39-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="a2e39-127">Por ejemplo, si un cliente libera un objeto sin liberar algunos de sus subobjetos, puede llamar a **MakeInvalid** inmediatamente para liberar esos subobjetos.</span><span class="sxs-lookup"><span data-stu-id="a2e39-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="a2e39-128">Debe ser el propietario del objeto que intente invalidar.</span><span class="sxs-lookup"><span data-stu-id="a2e39-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="a2e39-129">Debe tener al menos 16 bytes de longitud y tener al menos tres métodos en su tabla virtual.</span><span class="sxs-lookup"><span data-stu-id="a2e39-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="a2e39-130">Puede llamar a **MakeInvalid** y, a continuación, realizar cualquier trabajo de apagado, como descartar estructuras de datos asociadas, que normalmente se realiza durante la liberación de un objeto.</span><span class="sxs-lookup"><span data-stu-id="a2e39-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="a2e39-131">El código para admitir el objeto no debe mantenerse en la memoria, ya que MAPI libera la memoria llamando a [MAPIFreeBuffer](mapifreebuffer.md) y, a continuación, libera el objeto.</span><span class="sxs-lookup"><span data-stu-id="a2e39-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="a2e39-132">Puede liberar recursos, llamar **a MakeInvalid** y, a continuación, omitir el objeto invalidado.</span><span class="sxs-lookup"><span data-stu-id="a2e39-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a2e39-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2e39-133">See also</span></span>



[<span data-ttu-id="a2e39-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="a2e39-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="a2e39-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a2e39-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

