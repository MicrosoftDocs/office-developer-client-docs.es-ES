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
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="467e4-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="467e4-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="467e4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="467e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="467e4-105">Marca un objeto como inutilizable.</span><span class="sxs-lookup"><span data-stu-id="467e4-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="467e4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="467e4-106">Parameters</span></span>

 <span data-ttu-id="467e4-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="467e4-107">_ulFlags_</span></span>
  
> <span data-ttu-id="467e4-108">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="467e4-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="467e4-109">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="467e4-109">_lpObject_</span></span>
  
> <span data-ttu-id="467e4-110">[entrada] Puntero al objeto que se va a invalidar.</span><span class="sxs-lookup"><span data-stu-id="467e4-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="467e4-111">La interfaz del objeto debe derivar de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="467e4-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="467e4-112">_ulRefCount_</span><span class="sxs-lookup"><span data-stu-id="467e4-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="467e4-113">[entrada] Recuento de referencias presente del objeto.</span><span class="sxs-lookup"><span data-stu-id="467e4-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="467e4-114">_cMethods_</span><span class="sxs-lookup"><span data-stu-id="467e4-114">_cMethods_</span></span>
  
> <span data-ttu-id="467e4-115">[entrada] Recuento de métodos en la tabla virtual del objeto.</span><span class="sxs-lookup"><span data-stu-id="467e4-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="467e4-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="467e4-116">Return value</span></span>

<span data-ttu-id="467e4-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="467e4-117">S_OK</span></span> 
  
> <span data-ttu-id="467e4-118">El objeto se marcó correctamente como inutilizable.</span><span class="sxs-lookup"><span data-stu-id="467e4-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="467e4-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="467e4-119">Remarks</span></span>

<span data-ttu-id="467e4-120">El **método IMAPISupport::MakeInvalid** se implementa para todos los objetos de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="467e4-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="467e4-121">El objeto que se va a invalidar debe derivar de la interfaz **IUnknown** o de una interfaz derivada de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="467e4-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="467e4-122">**MakeInvalid** marca un objeto como inutilizable reemplazando la tabla virtual del objeto por una tabla de código auxiliar de tamaño similar en la que los métodos **IUnknown::AddRef** e **IUnknown::Release** tienen el rendimiento esperado.</span><span class="sxs-lookup"><span data-stu-id="467e4-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="467e4-123">Sin embargo, se producirá un error en cualquier otro método, devolviendo el valor MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="467e4-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="467e4-124">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="467e4-124">Notes to callers</span></span>

<span data-ttu-id="467e4-125">Los proveedores de servicios y los servicios de mensajes suelen **llamar a MakeInvalid en** el momento del apagado.</span><span class="sxs-lookup"><span data-stu-id="467e4-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="467e4-126">Sin embargo, se puede llamar a **MakeInvalid** en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="467e4-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="467e4-127">Por ejemplo, si un cliente libera un objeto sin liberar algunos de sus subobjetos, puede llamar a **MakeInvalid** inmediatamente para liberar esos subobjetos.</span><span class="sxs-lookup"><span data-stu-id="467e4-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="467e4-128">Debe ser el propietario del objeto que intenta invalidar.</span><span class="sxs-lookup"><span data-stu-id="467e4-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="467e4-129">Debe tener al menos 16 bytes de longitud y tener al menos tres métodos en su tabla virtual.</span><span class="sxs-lookup"><span data-stu-id="467e4-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="467e4-130">Puede llamar a **MakeInvalid** y, a continuación, realizar cualquier trabajo de cierre, como descartar las estructuras de datos asociadas, que normalmente se realiza durante la publicación de un objeto.</span><span class="sxs-lookup"><span data-stu-id="467e4-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="467e4-131">No es necesario conservar el código para admitir el objeto en la memoria, ya que MAPI libera la memoria llamando a [MAPIFreeBuffer](mapifreebuffer.md) y, a continuación, libera el objeto.</span><span class="sxs-lookup"><span data-stu-id="467e4-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="467e4-132">Puede liberar recursos, llamar **a MakeInvalid** y, a continuación, omitir el objeto invalidado.</span><span class="sxs-lookup"><span data-stu-id="467e4-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="467e4-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="467e4-133">See also</span></span>



[<span data-ttu-id="467e4-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="467e4-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="467e4-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="467e4-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

