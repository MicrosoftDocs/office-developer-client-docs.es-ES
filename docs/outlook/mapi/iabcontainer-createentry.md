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
ms.openlocfilehash: 2f8a6baa9a910b91e633084f1d9cd8ac52b24d5b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575605"
---
# <a name="iabcontainercreateentry"></a><span data-ttu-id="2e51f-103">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="2e51f-103">IABContainer::CreateEntry</span></span>

  
  
<span data-ttu-id="2e51f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e51f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e51f-105">Crea una nueva entrada, que puede ser un usuario de mensajería, una lista de distribución u otro contenedor.</span><span class="sxs-lookup"><span data-stu-id="2e51f-105">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a><span data-ttu-id="2e51f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e51f-106">Parameters</span></span>

 <span data-ttu-id="2e51f-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="2e51f-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="2e51f-108">[entrada] El número de bytes en el identificador de entrada indicada por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="2e51f-108">[in] The count of the bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="2e51f-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="2e51f-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="2e51f-110">[entrada] Un puntero al identificador de entrada de una plantilla para la creación de nuevas entradas de un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="2e51f-110">[in] A pointer to the entry identifier of a template for creating new entries of a particular type.</span></span> 
    
 <span data-ttu-id="2e51f-111">_ulCreateFlags_</span><span class="sxs-lookup"><span data-stu-id="2e51f-111">_ulCreateFlags_</span></span>
  
> <span data-ttu-id="2e51f-112">[entrada] Una máscara de bits de indicadores que controla cómo se lleva a cabo la creación de entrada.</span><span class="sxs-lookup"><span data-stu-id="2e51f-112">[in] A bitmask of flags that controls how entry creation is performed.</span></span> <span data-ttu-id="2e51f-113">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="2e51f-113">The following flags can be set:</span></span>
    
<span data-ttu-id="2e51f-114">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="2e51f-114">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="2e51f-115">Debe realizar un nivel separado de comprobación de la entrada duplicada.</span><span class="sxs-lookup"><span data-stu-id="2e51f-115">A loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="2e51f-116">La implementación de comprobación de la entrada duplicada suelto es específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="2e51f-116">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="2e51f-117">Por ejemplo, un proveedor puede definir a una coincidencia separada como las dos entradas que tienen el mismo nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="2e51f-117">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="2e51f-118">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="2e51f-118">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="2e51f-119">Debe realizar un nivel estricto de comprobación de la entrada duplicada.</span><span class="sxs-lookup"><span data-stu-id="2e51f-119">A strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="2e51f-120">La implementación de comprobación estricta entrada duplicada es específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="2e51f-120">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="2e51f-121">Por ejemplo, un proveedor puede definir a una coincidencia estricta como las dos entradas que tienen ambos el mismo nombre para mostrar y la dirección de mensajería.</span><span class="sxs-lookup"><span data-stu-id="2e51f-121">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="2e51f-122">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="2e51f-122">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="2e51f-123">Una nueva entrada debería reemplazar uno existente si se determina que las dos son duplicados.</span><span class="sxs-lookup"><span data-stu-id="2e51f-123">A new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
 <span data-ttu-id="2e51f-124">_lppMAPIPropEntry_</span><span class="sxs-lookup"><span data-stu-id="2e51f-124">_lppMAPIPropEntry_</span></span>
  
> <span data-ttu-id="2e51f-125">[out] Un puntero a un puntero a la entrada recién creada.</span><span class="sxs-lookup"><span data-stu-id="2e51f-125">[out] A pointer to a pointer to the newly created entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2e51f-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e51f-126">Return value</span></span>

<span data-ttu-id="2e51f-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="2e51f-127">S_OK</span></span> 
  
> <span data-ttu-id="2e51f-128">Se ha creado correctamente la nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="2e51f-128">The new entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2e51f-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2e51f-129">Remarks</span></span>

<span data-ttu-id="2e51f-130">El método **IABContainer::CreateEntry** crea una nueva entrada de un tipo determinado en el contenedor especificado, la devolución de un puntero a una implementación de la interfaz para obtener acceso a la entrada.</span><span class="sxs-lookup"><span data-stu-id="2e51f-130">The **IABContainer::CreateEntry** method creates a new entry of a particular type in the specified container, returning a pointer to an interface implementation for further access to the entry.</span></span> <span data-ttu-id="2e51f-131">La nueva entrada se crea mediante el uso de una plantilla que se ha seleccionado desde la lista del contenedor de plantillas disponibles publicado en su tabla de uso único.</span><span class="sxs-lookup"><span data-stu-id="2e51f-131">The new entry is created by using a template that has been selected from the container's list of available templates published in its one-off table.</span></span> <span data-ttu-id="2e51f-132">Los autores de llamadas tener acceso a la tabla de uso único de un contenedor llamando a su método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) y solicitar la propiedad de **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2e51f-132">Callers access a container's one-off table by calling its [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2e51f-133">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="2e51f-133">Notes to implementers</span></span>

<span data-ttu-id="2e51f-134">Todos los contenedores que admiten el método **IABContainer::CreateEntry** deben ser modificables.</span><span class="sxs-lookup"><span data-stu-id="2e51f-134">All containers that support the **IABContainer::CreateEntry** method must be modifiable.</span></span> <span data-ttu-id="2e51f-135">Establecer marca AB_MODIFIABLE de su contenedor en su propiedad **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) para indicar que es modificable.</span><span class="sxs-lookup"><span data-stu-id="2e51f-135">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="2e51f-136">Debe admitir todas las marcas de _ulCreateFlags_ .</span><span class="sxs-lookup"><span data-stu-id="2e51f-136">You should support all of the  _ulCreateFlags_ flags.</span></span> <span data-ttu-id="2e51f-137">Sin embargo, la interpretación y el uso de estos indicadores es específico de la implementación, es decir, puede determinar el significado de la semántica de CREATE_CHECK_DUP_LOOSE y CREATE_CHECK_DUP_STRICT en el contexto de su implementación.</span><span class="sxs-lookup"><span data-stu-id="2e51f-137">However, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT mean in the context of your implementation.</span></span> <span data-ttu-id="2e51f-138">Si no puede o no determinar si una entrada es un duplicado, permitir siempre la entrada que se creará.</span><span class="sxs-lookup"><span data-stu-id="2e51f-138">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be created.</span></span> 
  
<span data-ttu-id="2e51f-139">Algunos proveedores de implementan la entrada estricta de comprobación de forma que coincida con el nombre para mostrar, mensajería dirección y la clave de búsqueda en una entrada; otros proveedores de limitan la coincidencia para mostrar el nombre y la dirección.</span><span class="sxs-lookup"><span data-stu-id="2e51f-139">Some providers implement strict entry checking by matching the display name, messaging address, and search key in an entry; other providers limit the match to display name and address.</span></span> <span data-ttu-id="2e51f-140">A menudo se implementa la comprobación de entrada separado comprobando el nombre para mostrar sólo.</span><span class="sxs-lookup"><span data-stu-id="2e51f-140">Loose entry checking is often implemented by checking the display name only.</span></span> 
  
## <a name="notes-to-host-address-book-provider-implementers"></a><span data-ttu-id="2e51f-141">Notas para implementadores de proveedor de la libreta de direcciones de Host</span><span class="sxs-lookup"><span data-stu-id="2e51f-141">Notes to Host Address Book Provider Implementers</span></span>

<span data-ttu-id="2e51f-142">Si el contenedor puede crear las entradas de las plantillas de otros proveedores, la implementación de **CreateEntry** debe proporcionar almacenamiento para algunas o todas las propiedades asociadas con los movimientos creados.</span><span class="sxs-lookup"><span data-stu-id="2e51f-142">If your container can create entries from the templates of other providers, your implementation of **CreateEntry** should provide storage for some or all of the properties associated with the created entries.</span></span> <span data-ttu-id="2e51f-143">Por ejemplo, si proporciona almacenamiento para la propiedad de **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) de la entrada, puede generar su cuadro de diálogo detalles sin tener que dependen del proveedor externo.</span><span class="sxs-lookup"><span data-stu-id="2e51f-143">For example, if you provide storage for an entry's **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property, you can generate its details dialog box without having to depend on the foreign provider.</span></span> 
  
<span data-ttu-id="2e51f-144">Si el contenedor puede crear las entradas que admiten la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), la implementación de **CreateEntry** debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2e51f-144">If your container can create entries that support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, your implementation of **CreateEntry** must do the following:</span></span> 
  
1. <span data-ttu-id="2e51f-145">Llame al método [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) .</span><span class="sxs-lookup"><span data-stu-id="2e51f-145">Call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method.</span></span> <span data-ttu-id="2e51f-146">**OpenTemplateID** permite que el código del proveedor externo para la entrada enlazar a la nueva entrada que se está creando.</span><span class="sxs-lookup"><span data-stu-id="2e51f-146">**OpenTemplateID** enables the foreign provider's code for the entry to bind to the new entry being created.</span></span> <span data-ttu-id="2e51f-147">Proveedores de externos admiten este proceso de enlace para mantener el control sobre las entradas de creado a partir de sus plantillas en los contenedores de los proveedores de la libreta de direcciones de host.</span><span class="sxs-lookup"><span data-stu-id="2e51f-147">Foreign providers support this binding process to maintain control over entries created from their templates into the containers of host address book providers.</span></span> 
    
2. <span data-ttu-id="2e51f-148">Realizar cualquier inicialización necesaria y rellenar el objeto nuevo con todas las propiedades de la entrada en el proveedor extranjero que devuelve el objeto en el parámetro _lppMAPIPropNew_ desde **OpenTemplateID**.</span><span class="sxs-lookup"><span data-stu-id="2e51f-148">Perform any necessary initialization, and populate the new object with all of the properties from the entry in the foreign provider that the object returned in the  _lppMAPIPropNew_ parameter from **OpenTemplateID**.</span></span>
    
<span data-ttu-id="2e51f-149">Si se realiza correctamente **OpenTemplateID** , copie las propiedades para la implementación indicada por el parámetro _lppMAPIPropNew_ en lugar de hacerlo directamente a la implementación que apunta el parámetro _lpMAPIPropData_ .</span><span class="sxs-lookup"><span data-stu-id="2e51f-149">If **OpenTemplateID** succeeds, copy the properties to the implementation pointed to by the  _lppMAPIPropNew_ parameter rather than directly to the implementation pointed to by the  _lpMAPIPropData_ parameter.</span></span> <span data-ttu-id="2e51f-150">Inicializar la nueva entrada para su uso sin conexión tal y como lo haría con cualquier otra entrada de un proveedor externo.</span><span class="sxs-lookup"><span data-stu-id="2e51f-150">Initialize the new entry for offline use as you would any other entry from a foreign provider.</span></span> 
  
<span data-ttu-id="2e51f-151">Si **OpenTemplateID** devuelve un error, debe producirse un error en **CreateEntry** .</span><span class="sxs-lookup"><span data-stu-id="2e51f-151">If **OpenTemplateID** returns an error, **CreateEntry** should fail.</span></span> <span data-ttu-id="2e51f-152">No permitir la entrada que se creará.</span><span class="sxs-lookup"><span data-stu-id="2e51f-152">Do not allow the entry to be created.</span></span> <span data-ttu-id="2e51f-153">Debido a que el proveedor externo puede realizar suposiciones acerca de los datos de su proveedor, no cree una entrada con un identificador de plantilla que no se ha enlazado correctamente al proveedor externo.</span><span class="sxs-lookup"><span data-stu-id="2e51f-153">Because the foreign provider can make assumptions about the data in your provider, do not create an entry with a template identifier that has not been successfully bound to the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2e51f-154">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="2e51f-154">Notes to callers</span></span>

<span data-ttu-id="2e51f-155">Cuando se devuelve **CreateEntry** , puede o no inmediatamente obtener acceso el identificador de entrada para la nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="2e51f-155">When **CreateEntry** returns, you may or may not be able to immediately access the entry identifier for the new entry.</span></span> <span data-ttu-id="2e51f-156">Algunos proveedores de libreta de direcciones no permitir que esté disponible hasta después de llamar a (método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ) de la nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="2e51f-156">Some address book providers do not make it available until after you have called the new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="2e51f-157">Aunque los indicadores de comprobación duplicados se pasan como parámetros al **CreateEntry**, el duplicado en la operación de comprobación no se produce hasta que se llama **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="2e51f-157">Although duplicate checking flags are passed as parameters to **CreateEntry**, the duplicate checking operation does not occur until **SaveChanges** is called.</span></span> <span data-ttu-id="2e51f-158">Por lo tanto, se devuelven errores relacionados, como MAPI_E_COLLISION, que indica que se ha intentado crear una entrada ya existente, por **SaveChanges** en lugar de **CreateEntry**.</span><span class="sxs-lookup"><span data-stu-id="2e51f-158">Therefore, related errors such as MAPI_E_COLLISION, which indicates that an attempt was made to create an already existing entry, are returned by **SaveChanges** rather than **CreateEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2e51f-159">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="2e51f-159">See also</span></span>



[<span data-ttu-id="2e51f-160">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="2e51f-160">IABContainer::CopyEntries</span></span>](iabcontainer-copyentries.md)
  
[<span data-ttu-id="2e51f-161">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="2e51f-161">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="2e51f-162">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="2e51f-162">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="2e51f-163">Propiedad canónica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="2e51f-163">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="2e51f-164">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="2e51f-164">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

