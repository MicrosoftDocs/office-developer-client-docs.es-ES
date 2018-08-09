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
ms.openlocfilehash: 595d5fdba28634b038838921102d3125135452a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817505"
---
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="3068a-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="3068a-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="3068a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3068a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3068a-105">Marca un objeto como no utilizable.</span><span class="sxs-lookup"><span data-stu-id="3068a-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="3068a-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="3068a-106">Parameters</span></span>

 <span data-ttu-id="3068a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3068a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3068a-108">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3068a-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="3068a-109">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="3068a-109">_lpObject_</span></span>
  
> <span data-ttu-id="3068a-110">[entrada] Un puntero al objeto que se invalide.</span><span class="sxs-lookup"><span data-stu-id="3068a-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="3068a-111">La interfaz del objeto debe derivarse de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="3068a-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="3068a-112">_ulRefCount_</span><span class="sxs-lookup"><span data-stu-id="3068a-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="3068a-113">[entrada] Recuento de referencia presente del objeto.</span><span class="sxs-lookup"><span data-stu-id="3068a-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="3068a-114">_cMethods_</span><span class="sxs-lookup"><span data-stu-id="3068a-114">_cMethods_</span></span>
  
> <span data-ttu-id="3068a-115">[entrada] El recuento de métodos de vtable del objeto.</span><span class="sxs-lookup"><span data-stu-id="3068a-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3068a-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3068a-116">Return value</span></span>

<span data-ttu-id="3068a-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="3068a-117">S_OK</span></span> 
  
> <span data-ttu-id="3068a-118">El objeto se marcó correctamente como no utilizable.</span><span class="sxs-lookup"><span data-stu-id="3068a-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3068a-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3068a-119">Remarks</span></span>

<span data-ttu-id="3068a-120">El método **IMAPISupport::MakeInvalid** se implementa para todos los objetos de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="3068a-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="3068a-121">El objeto que se invalide se debe derivar de la interfaz **IUnknown** o desde una interfaz que se deriva de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="3068a-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="3068a-122">**MakeInvalid** marca un objeto como no utilizable mediante el reemplazo de vtable del objeto con un vtable de código auxiliar del tamaño similar en la que los métodos de **IUnknown:: AddRef** e **IUnknown:: Release** realizan según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="3068a-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="3068a-123">Sin embargo, cualquier otro método producirá un error, devuelve el valor MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="3068a-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3068a-124">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="3068a-124">Notes to callers</span></span>

<span data-ttu-id="3068a-125">Proveedores de servicios y los servicios de message normalmente llamada **MakeInvalid** durante el apagado.</span><span class="sxs-lookup"><span data-stu-id="3068a-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="3068a-126">Sin embargo, se puede llamar **MakeInvalid** en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="3068a-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="3068a-127">Por ejemplo, si un cliente suelta un objeto sin liberar algunos de sus objetos secundarios, puede llamar a **MakeInvalid** inmediatamente para liberar los subobjetos.</span><span class="sxs-lookup"><span data-stu-id="3068a-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="3068a-128">Debe ser propietario del objeto que intenta invalidar.</span><span class="sxs-lookup"><span data-stu-id="3068a-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="3068a-129">Debe tener una longitud de al menos 16 bytes y tener al menos tres métodos en su tabla vtable.</span><span class="sxs-lookup"><span data-stu-id="3068a-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="3068a-130">Puede llamar a **MakeInvalid** y, a continuación, realizar cualquier trabajo de cierre, como descartar las estructuras de datos asociado, que normalmente se realiza durante la versión de un objeto.</span><span class="sxs-lookup"><span data-stu-id="3068a-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="3068a-131">Código para admitir el objeto no necesita mantenerse en la memoria, ya que MAPI libera la memoria llamando [MAPIFreeBuffer](mapifreebuffer.md) y, a continuación, libera el objeto.</span><span class="sxs-lookup"><span data-stu-id="3068a-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="3068a-132">Puede liberar recursos, llame a **MakeInvalid**y, a continuación, omitir el objeto invalidado.</span><span class="sxs-lookup"><span data-stu-id="3068a-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3068a-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="3068a-133">See also</span></span>



[<span data-ttu-id="3068a-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="3068a-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="3068a-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3068a-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

