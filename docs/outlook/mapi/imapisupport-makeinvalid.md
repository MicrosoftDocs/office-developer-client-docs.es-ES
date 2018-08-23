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
ms.openlocfilehash: 75771670f58f4cd65e15a02d08e6f78ab9d71755
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570740"
---
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="579f1-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="579f1-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="579f1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="579f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="579f1-105">Marca un objeto como no utilizable.</span><span class="sxs-lookup"><span data-stu-id="579f1-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="579f1-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="579f1-106">Parameters</span></span>

 <span data-ttu-id="579f1-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="579f1-107">_ulFlags_</span></span>
  
> <span data-ttu-id="579f1-108">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="579f1-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="579f1-109">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="579f1-109">_lpObject_</span></span>
  
> <span data-ttu-id="579f1-110">[entrada] Un puntero al objeto que se invalide.</span><span class="sxs-lookup"><span data-stu-id="579f1-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="579f1-111">La interfaz del objeto debe derivarse de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="579f1-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="579f1-112">_ulRefCount_</span><span class="sxs-lookup"><span data-stu-id="579f1-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="579f1-113">[entrada] Recuento de referencia presente del objeto.</span><span class="sxs-lookup"><span data-stu-id="579f1-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="579f1-114">_cMethods_</span><span class="sxs-lookup"><span data-stu-id="579f1-114">_cMethods_</span></span>
  
> <span data-ttu-id="579f1-115">[entrada] El recuento de métodos de vtable del objeto.</span><span class="sxs-lookup"><span data-stu-id="579f1-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="579f1-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="579f1-116">Return value</span></span>

<span data-ttu-id="579f1-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="579f1-117">S_OK</span></span> 
  
> <span data-ttu-id="579f1-118">El objeto se marcó correctamente como no utilizable.</span><span class="sxs-lookup"><span data-stu-id="579f1-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="579f1-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="579f1-119">Remarks</span></span>

<span data-ttu-id="579f1-120">El método **IMAPISupport::MakeInvalid** se implementa para todos los objetos de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="579f1-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="579f1-121">El objeto que se invalide se debe derivar de la interfaz **IUnknown** o desde una interfaz que se deriva de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="579f1-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="579f1-122">**MakeInvalid** marca un objeto como no utilizable mediante el reemplazo de vtable del objeto con un vtable de código auxiliar del tamaño similar en la que los métodos de **IUnknown:: AddRef** e **IUnknown:: Release** realizan según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="579f1-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="579f1-123">Sin embargo, cualquier otro método producirá un error, devuelve el valor MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="579f1-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="579f1-124">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="579f1-124">Notes to callers</span></span>

<span data-ttu-id="579f1-125">Proveedores de servicios y los servicios de message normalmente llamada **MakeInvalid** durante el apagado.</span><span class="sxs-lookup"><span data-stu-id="579f1-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="579f1-126">Sin embargo, se puede llamar **MakeInvalid** en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="579f1-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="579f1-127">Por ejemplo, si un cliente suelta un objeto sin liberar algunos de sus objetos secundarios, puede llamar a **MakeInvalid** inmediatamente para liberar los subobjetos.</span><span class="sxs-lookup"><span data-stu-id="579f1-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="579f1-128">Debe ser propietario del objeto que intenta invalidar.</span><span class="sxs-lookup"><span data-stu-id="579f1-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="579f1-129">Debe tener una longitud de al menos 16 bytes y tener al menos tres métodos en su tabla vtable.</span><span class="sxs-lookup"><span data-stu-id="579f1-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="579f1-130">Puede llamar a **MakeInvalid** y, a continuación, realizar cualquier trabajo de cierre, como descartar las estructuras de datos asociado, que normalmente se realiza durante la versión de un objeto.</span><span class="sxs-lookup"><span data-stu-id="579f1-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="579f1-131">Código para admitir el objeto no necesita mantenerse en la memoria, ya que MAPI libera la memoria llamando [MAPIFreeBuffer](mapifreebuffer.md) y, a continuación, libera el objeto.</span><span class="sxs-lookup"><span data-stu-id="579f1-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="579f1-132">Puede liberar recursos, llame a **MakeInvalid**y, a continuación, omitir el objeto invalidado.</span><span class="sxs-lookup"><span data-stu-id="579f1-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="579f1-133">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="579f1-133">See also</span></span>



[<span data-ttu-id="579f1-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="579f1-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="579f1-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="579f1-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

