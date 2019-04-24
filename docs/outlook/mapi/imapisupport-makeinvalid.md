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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316663"
---
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="f3d80-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="f3d80-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="f3d80-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3d80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3d80-105">Marca un objeto como inutilizable.</span><span class="sxs-lookup"><span data-stu-id="f3d80-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="f3d80-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f3d80-106">Parameters</span></span>

 <span data-ttu-id="f3d80-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f3d80-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f3d80-108">Reserve debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f3d80-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="f3d80-109">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="f3d80-109">_lpObject_</span></span>
  
> <span data-ttu-id="f3d80-110">a Un puntero al objeto que se va a invalidar.</span><span class="sxs-lookup"><span data-stu-id="f3d80-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="f3d80-111">La interfaz del objeto debe derivarse de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="f3d80-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="f3d80-112">_ulRefCount_</span><span class="sxs-lookup"><span data-stu-id="f3d80-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="f3d80-113">a El recuento de referencia actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="f3d80-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="f3d80-114">_cMethods_</span><span class="sxs-lookup"><span data-stu-id="f3d80-114">_cMethods_</span></span>
  
> <span data-ttu-id="f3d80-115">a El número de métodos en la vtable del objeto.</span><span class="sxs-lookup"><span data-stu-id="f3d80-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f3d80-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3d80-116">Return value</span></span>

<span data-ttu-id="f3d80-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3d80-117">S_OK</span></span> 
  
> <span data-ttu-id="f3d80-118">El objeto se marcó correctamente como inutilizable.</span><span class="sxs-lookup"><span data-stu-id="f3d80-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f3d80-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f3d80-119">Remarks</span></span>

<span data-ttu-id="f3d80-120">El método **IMAPISupport:: MakeInvalid** se implementa para todos los objetos de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="f3d80-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="f3d80-121">El objeto que se va a invalidar debe derivarse de la interfaz **IUnknown** o de una interfaz derivada de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="f3d80-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="f3d80-122">**MakeInvalid** marca un objeto como inutilizable reemplazando la vtable del objeto con una vtable de código auxiliar de un tamaño similar en el que los métodos **IUnknown:: AddRef** e **IUnknown:: Release** funcionan según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="f3d80-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="f3d80-123">Sin embargo, si se produce un error en cualquier otro método, se devuelve el valor MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="f3d80-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f3d80-124">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="f3d80-124">Notes to callers</span></span>

<span data-ttu-id="f3d80-125">Los proveedores de servicios y los servicios de mensajes normalmente llaman a **MakeInvalid** en el momento del cierre.</span><span class="sxs-lookup"><span data-stu-id="f3d80-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="f3d80-126">Sin embargo, se puede llamar a **MakeInvalid** en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="f3d80-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="f3d80-127">Por ejemplo, si un cliente libera un objeto sin liberar algunos de sus subobjetos, puede llamar a **MakeInvalid** inmediatamente para liberar esos subobjetos.</span><span class="sxs-lookup"><span data-stu-id="f3d80-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="f3d80-128">Debe ser el propietario del objeto que intenta invalidar.</span><span class="sxs-lookup"><span data-stu-id="f3d80-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="f3d80-129">Debe tener al menos 16 bytes de longitud y tener al menos tres métodos en la tabla vtable.</span><span class="sxs-lookup"><span data-stu-id="f3d80-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="f3d80-130">Puede llamar a **MakeInvalid** y, a continuación, realizar cualquier trabajo de cierre, como descartar estructuras de datos asociadas, que normalmente se realiza durante la liberación de un objeto.</span><span class="sxs-lookup"><span data-stu-id="f3d80-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="f3d80-131">No es necesario mantener el código para admitir el objeto en la memoria, ya que MAPI libera la memoria al llamar a [MAPIFreeBuffer](mapifreebuffer.md) y, a continuación, libera el objeto.</span><span class="sxs-lookup"><span data-stu-id="f3d80-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="f3d80-132">Puede liberar recursos, llamar a **MakeInvalid**y, a continuación, omitir el objeto invalidado.</span><span class="sxs-lookup"><span data-stu-id="f3d80-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f3d80-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3d80-133">See also</span></span>



[<span data-ttu-id="f3d80-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="f3d80-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="f3d80-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f3d80-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

