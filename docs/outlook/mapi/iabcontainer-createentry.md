---
title: IABContainerCreateEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CreateEntry
api_type:
- COM
ms.assetid: ea1daf74-d9e3-4304-bf5d-889afeea6ae9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9f80130279e3437dd9be947de97d3f0d4181165e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411277"
---
# <a name="iabcontainercreateentry"></a><span data-ttu-id="69775-103">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="69775-103">IABContainer::CreateEntry</span></span>

  
  
<span data-ttu-id="69775-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69775-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69775-105">Crea una nueva entrada, que puede ser un usuario de mensajería, una lista de distribución u otro contenedor.</span><span class="sxs-lookup"><span data-stu-id="69775-105">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a><span data-ttu-id="69775-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69775-106">Parameters</span></span>

 <span data-ttu-id="69775-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="69775-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="69775-108">[entrada] Recuento de los bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="69775-108">[in] The count of the bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="69775-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="69775-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="69775-110">[entrada] Puntero al identificador de entrada de una plantilla para crear nuevas entradas de un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="69775-110">[in] A pointer to the entry identifier of a template for creating new entries of a particular type.</span></span> 
    
 <span data-ttu-id="69775-111">_ulCreateFlags_</span><span class="sxs-lookup"><span data-stu-id="69775-111">_ulCreateFlags_</span></span>
  
> <span data-ttu-id="69775-112">[entrada] Máscara de bits de marcas que controla cómo se realiza la creación de entradas.</span><span class="sxs-lookup"><span data-stu-id="69775-112">[in] A bitmask of flags that controls how entry creation is performed.</span></span> <span data-ttu-id="69775-113">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="69775-113">The following flags can be set:</span></span>
    
<span data-ttu-id="69775-114">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="69775-114">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="69775-115">Debe realizarse un nivel suelto de comprobación de entradas duplicadas.</span><span class="sxs-lookup"><span data-stu-id="69775-115">A loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="69775-116">La implementación de la comprobación de entradas duplicadas sueltos es específica del proveedor.</span><span class="sxs-lookup"><span data-stu-id="69775-116">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="69775-117">Por ejemplo, un proveedor puede definir una coincidencia libre como cualquier dos entradas que tengan el mismo nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="69775-117">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="69775-118">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="69775-118">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="69775-119">Debe realizarse un nivel estricto de comprobación de entradas duplicadas.</span><span class="sxs-lookup"><span data-stu-id="69775-119">A strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="69775-120">La implementación de comprobación estricta de entradas duplicadas es específica del proveedor.</span><span class="sxs-lookup"><span data-stu-id="69775-120">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="69775-121">Por ejemplo, un proveedor puede definir una coincidencia estricta como cualquier dos entradas que tengan el mismo nombre para mostrar y la misma dirección de mensajería.</span><span class="sxs-lookup"><span data-stu-id="69775-121">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="69775-122">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="69775-122">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="69775-123">Una nueva entrada debe reemplazar una existente si se determina que las dos son duplicadas.</span><span class="sxs-lookup"><span data-stu-id="69775-123">A new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
 <span data-ttu-id="69775-124">_lppMAPIPropEntry_</span><span class="sxs-lookup"><span data-stu-id="69775-124">_lppMAPIPropEntry_</span></span>
  
> <span data-ttu-id="69775-125">[salida] Puntero a un puntero a la entrada recién creada.</span><span class="sxs-lookup"><span data-stu-id="69775-125">[out] A pointer to a pointer to the newly created entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="69775-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69775-126">Return value</span></span>

<span data-ttu-id="69775-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="69775-127">S_OK</span></span> 
  
> <span data-ttu-id="69775-128">La nueva entrada se creó correctamente.</span><span class="sxs-lookup"><span data-stu-id="69775-128">The new entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="69775-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="69775-129">Remarks</span></span>

<span data-ttu-id="69775-130">El **método IABContainer::CreateEntry** crea una nueva entrada de un tipo determinado en el contenedor especificado y devuelve un puntero a una implementación de interfaz para obtener más acceso a la entrada.</span><span class="sxs-lookup"><span data-stu-id="69775-130">The **IABContainer::CreateEntry** method creates a new entry of a particular type in the specified container, returning a pointer to an interface implementation for further access to the entry.</span></span> <span data-ttu-id="69775-131">La nueva entrada se crea mediante una plantilla que se ha seleccionado en la lista de plantillas disponibles del contenedor publicada en su tabla de uso único.</span><span class="sxs-lookup"><span data-stu-id="69775-131">The new entry is created by using a template that has been selected from the container's list of available templates published in its one-off table.</span></span> <span data-ttu-id="69775-132">Los autores de llamadas tienen acceso a la tabla de uso único de un contenedor llamando a su método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) y solicitando la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="69775-132">Callers access a container's one-off table by calling its [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="69775-133">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="69775-133">Notes to implementers</span></span>

<span data-ttu-id="69775-134">Todos los contenedores que admiten **el método IABContainer::CreateEntry** deben ser modificables.</span><span class="sxs-lookup"><span data-stu-id="69775-134">All containers that support the **IABContainer::CreateEntry** method must be modifiable.</span></span> <span data-ttu-id="69775-135">Establece la marca de AB_MODIFIABLE contenedor en su propiedad **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) para indicar que es modificable.</span><span class="sxs-lookup"><span data-stu-id="69775-135">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="69775-136">Debe admitir todas las marcas _ulCreateFlags._</span><span class="sxs-lookup"><span data-stu-id="69775-136">You should support all of the  _ulCreateFlags_ flags.</span></span> <span data-ttu-id="69775-137">Sin embargo, la interpretación y el uso de estas marcas es específico de la implementación; es decir, puedes determinar qué significa la semántica de CREATE_CHECK_DUP_LOOSE y CREATE_CHECK_DUP_STRICT en el contexto de la implementación.</span><span class="sxs-lookup"><span data-stu-id="69775-137">However, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT mean in the context of your implementation.</span></span> <span data-ttu-id="69775-138">Si no puede o no determina si una entrada es duplicada, permita siempre la creación de la entrada.</span><span class="sxs-lookup"><span data-stu-id="69775-138">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be created.</span></span> 
  
<span data-ttu-id="69775-139">Algunos proveedores implementan una comprobación de entrada estricta al hacer coincidir el nombre para mostrar, la dirección de mensajería y la clave de búsqueda de una entrada; otros proveedores limitan la coincidencia con el nombre para mostrar y la dirección.</span><span class="sxs-lookup"><span data-stu-id="69775-139">Some providers implement strict entry checking by matching the display name, messaging address, and search key in an entry; other providers limit the match to display name and address.</span></span> <span data-ttu-id="69775-140">La comprobación de entrada suelto se suele implementar comprobando solo el nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="69775-140">Loose entry checking is often implemented by checking the display name only.</span></span> 
  
## <a name="notes-to-host-address-book-provider-implementers"></a><span data-ttu-id="69775-141">Notas a los implementadores del proveedor de libretas de direcciones de host</span><span class="sxs-lookup"><span data-stu-id="69775-141">Notes to Host Address Book Provider Implementers</span></span>

<span data-ttu-id="69775-142">Si el contenedor puede crear entradas a partir de las plantillas de otros proveedores, la implementación de **CreateEntry** debe proporcionar almacenamiento para algunas o todas las propiedades asociadas con las entradas creadas.</span><span class="sxs-lookup"><span data-stu-id="69775-142">If your container can create entries from the templates of other providers, your implementation of **CreateEntry** should provide storage for some or all of the properties associated with the created entries.</span></span> <span data-ttu-id="69775-143">Por ejemplo, si proporciona almacenamiento para la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable)](pidtagdetailstable-canonical-property.md)de una entrada, puede generar su cuadro de diálogo de detalles sin tener que depender del proveedor externo.</span><span class="sxs-lookup"><span data-stu-id="69775-143">For example, if you provide storage for an entry's **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property, you can generate its details dialog box without having to depend on the foreign provider.</span></span> 
  
<span data-ttu-id="69775-144">Si el contenedor puede crear entradas que admitan **la propiedad PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), la implementación de **CreateEntry** debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="69775-144">If your container can create entries that support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, your implementation of **CreateEntry** must do the following:</span></span> 
  
1. <span data-ttu-id="69775-145">Llame al [método IMAPISupport::OpenTemplateID.](imapisupport-opentemplateid.md)</span><span class="sxs-lookup"><span data-stu-id="69775-145">Call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method.</span></span> <span data-ttu-id="69775-146">**OpenTemplateID permite** que el código del proveedor externo para la entrada se enlace a la nueva entrada que se está creando.</span><span class="sxs-lookup"><span data-stu-id="69775-146">**OpenTemplateID** enables the foreign provider's code for the entry to bind to the new entry being created.</span></span> <span data-ttu-id="69775-147">Los proveedores externos admiten este proceso de enlace para mantener el control sobre las entradas creadas a partir de sus plantillas en los contenedores de proveedores de libretas de direcciones host.</span><span class="sxs-lookup"><span data-stu-id="69775-147">Foreign providers support this binding process to maintain control over entries created from their templates into the containers of host address book providers.</span></span> 
    
2. <span data-ttu-id="69775-148">Realice cualquier inicialización necesaria y rellene el nuevo objeto con todas las propiedades de la entrada en el proveedor externo que el objeto devolvió en el parámetro  _lppMAPIPropNew_ de **OpenTemplateID**.</span><span class="sxs-lookup"><span data-stu-id="69775-148">Perform any necessary initialization, and populate the new object with all of the properties from the entry in the foreign provider that the object returned in the  _lppMAPIPropNew_ parameter from **OpenTemplateID**.</span></span>
    
<span data-ttu-id="69775-149">Si **OpenTemplateID** se realiza correctamente, copie las propiedades en la implementación a la que apunta el parámetro _lppMAPIPropNew_ en lugar de directamente a la implementación a la que apunta el parámetro _lpMAPIPropData._</span><span class="sxs-lookup"><span data-stu-id="69775-149">If **OpenTemplateID** succeeds, copy the properties to the implementation pointed to by the  _lppMAPIPropNew_ parameter rather than directly to the implementation pointed to by the  _lpMAPIPropData_ parameter.</span></span> <span data-ttu-id="69775-150">Inicialice la nueva entrada para su uso sin conexión como lo haría con cualquier otra entrada de un proveedor externo.</span><span class="sxs-lookup"><span data-stu-id="69775-150">Initialize the new entry for offline use as you would any other entry from a foreign provider.</span></span> 
  
<span data-ttu-id="69775-151">Si **OpenTemplateID devuelve** un error, **CreateEntry** debe producir un error.</span><span class="sxs-lookup"><span data-stu-id="69775-151">If **OpenTemplateID** returns an error, **CreateEntry** should fail.</span></span> <span data-ttu-id="69775-152">No permitir la creación de la entrada.</span><span class="sxs-lookup"><span data-stu-id="69775-152">Do not allow the entry to be created.</span></span> <span data-ttu-id="69775-153">Dado que el proveedor externo puede hacer suposiciones sobre los datos del proveedor, no cree una entrada con un identificador de plantilla que no se haya enlazado correctamente al proveedor externo.</span><span class="sxs-lookup"><span data-stu-id="69775-153">Because the foreign provider can make assumptions about the data in your provider, do not create an entry with a template identifier that has not been successfully bound to the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="69775-154">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="69775-154">Notes to callers</span></span>

<span data-ttu-id="69775-155">Cuando **CreateEntry** devuelve, es posible que pueda o no tener acceso inmediatamente al identificador de entrada de la nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="69775-155">When **CreateEntry** returns, you may or may not be able to immediately access the entry identifier for the new entry.</span></span> <span data-ttu-id="69775-156">Algunos proveedores de libretas de direcciones no lo hacen disponible hasta después de llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="69775-156">Some address book providers do not make it available until after you have called the new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="69775-157">Aunque las marcas de comprobación duplicadas se pasan como parámetros a **CreateEntry,** la operación de comprobación duplicada no se realiza hasta que se llama a **SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="69775-157">Although duplicate checking flags are passed as parameters to **CreateEntry**, the duplicate checking operation does not occur until **SaveChanges** is called.</span></span> <span data-ttu-id="69775-158">Por lo tanto, **SaveChanges** devuelve los errores relacionados, como MAPI_E_COLLISION, que indica que se ha intentado crear una entrada ya existente, en lugar de **CreateEntry**.</span><span class="sxs-lookup"><span data-stu-id="69775-158">Therefore, related errors such as MAPI_E_COLLISION, which indicates that an attempt was made to create an already existing entry, are returned by **SaveChanges** rather than **CreateEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="69775-159">Consulte también</span><span class="sxs-lookup"><span data-stu-id="69775-159">See also</span></span>



[<span data-ttu-id="69775-160">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="69775-160">IABContainer::CopyEntries</span></span>](iabcontainer-copyentries.md)
  
[<span data-ttu-id="69775-161">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="69775-161">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="69775-162">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="69775-162">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="69775-163">Propiedad canónica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="69775-163">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="69775-164">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="69775-164">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

