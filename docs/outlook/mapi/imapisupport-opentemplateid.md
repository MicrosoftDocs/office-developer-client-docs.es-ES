---
title: IMAPISupportOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenTemplateID
api_type:
- COM
ms.assetid: 532f7af0-b2cc-49dd-b1de-e3ec1dc9a3e7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f99843bcdf3689acad72145a33d6a9804175a413
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817539"
---
# <a name="imapisupportopentemplateid"></a><span data-ttu-id="90651-103">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="90651-103">IMAPISupport::OpenTemplateID</span></span>

  
  
<span data-ttu-id="90651-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="90651-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="90651-105">Se abre una entrada del destinatario en un proveedor de libreta de direcciones externa.</span><span class="sxs-lookup"><span data-stu-id="90651-105">Opens a recipient entry in a foreign address book provider.</span></span>
  
```cpp
HRESULT OpenTemplateID(
ULONG cbTemplateID,
LPENTRYID lpTemplateID,
ULONG ulTemplateFlags,
LPMAPIPROP lpMAPIPropData,
LPCIID lpInterface,
LPMAPIPROP FAR * lppMAPIPropNew,
LPMAPIPROP lpMAPIPropSibling
);
```

## <a name="parameters"></a><span data-ttu-id="90651-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90651-106">Parameters</span></span>

 <span data-ttu-id="90651-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="90651-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="90651-108">[entrada] El número de bytes en el identificador de plantilla que señala _lpTemplateID_.</span><span class="sxs-lookup"><span data-stu-id="90651-108">[in] The byte count in the template identifier pointed to by  _lpTemplateID_.</span></span> 
    
 <span data-ttu-id="90651-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="90651-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="90651-110">[entrada] Un puntero al identificador de plantilla **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) (propiedad) de la entrada del destinatario que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="90651-110">[in] A pointer to the template identifier **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="90651-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="90651-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="90651-112">[entrada] Una máscara de bits de indicadores que se utilizan para describir cómo abrir la entrada.</span><span class="sxs-lookup"><span data-stu-id="90651-112">[in] A bitmask of flags used to describe how to open the entry.</span></span> <span data-ttu-id="90651-113">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="90651-113">The following flag can be set:</span></span>
    
<span data-ttu-id="90651-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="90651-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="90651-115">Se creará una nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="90651-115">A new entry is being created.</span></span> <span data-ttu-id="90651-116">Cuando el proveedor externo recibe la llamada de [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) posterior de MAPI, puede controlar cómo se creó la entrada mediante la modificación de las propiedades que señala el parámetro _lpMAPIPropData_ o devolviendo una interfaz específica implementación en _lppMAPIPropNew_ para controlar cómo se establecen las propiedades de la nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="90651-116">When the foreign provider receives the subsequent [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) call from MAPI, it can control how the entry is created by modifying properties pointed to by the  _lpMAPIPropData_ parameter or by returning a specific interface implementation in  _lppMAPIPropNew_ to control how properties for the new entry are set.</span></span> 
    
 <span data-ttu-id="90651-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="90651-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="90651-118">[entrada] Un puntero a la implementación de la interfaz que el autor de la llamada se usa para tener acceso a la entrada.</span><span class="sxs-lookup"><span data-stu-id="90651-118">[in] A pointer to the interface implementation that the caller uses to access the entry.</span></span> <span data-ttu-id="90651-119">Ésta es la implementación que el proveedor externo puede ajustar con su propia implementación y devolver en el parámetro _lppMAPIPropNew_ .</span><span class="sxs-lookup"><span data-stu-id="90651-119">This is the implementation that the foreign provider can wrap with its own implementation and return in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="90651-120">El parámetro _lpMAPIPropData_ debe apuntar a una implementación de la interfaz de lectura y escritura que se deriva de [IMAPIProp: IUnknown](imapipropiunknown.md) y es compatible con la interfaz que se solicita en el parámetro _lpInterface_ .</span><span class="sxs-lookup"><span data-stu-id="90651-120">The  _lpMAPIPropData_ parameter must point to a read/write interface implementation that derives from [IMAPIProp : IUnknown](imapipropiunknown.md) and supports the interface being requested in the  _lpInterface_ parameter.</span></span> 
    
 <span data-ttu-id="90651-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="90651-121">_lpInterface_</span></span>
  
> <span data-ttu-id="90651-122">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la entrada.</span><span class="sxs-lookup"><span data-stu-id="90651-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the entry.</span></span> <span data-ttu-id="90651-123">El parámetro _lppMAPIPropNew_ apunta a una interfaz del tipo especificado por _lpInterface_.</span><span class="sxs-lookup"><span data-stu-id="90651-123">The  _lppMAPIPropNew_ parameter points to an interface of the type specified by  _lpInterface_.</span></span> <span data-ttu-id="90651-124">Pasando NULL, devuelve la interfaz estándar para un usuario de mensajería, IID_IMailUser.</span><span class="sxs-lookup"><span data-stu-id="90651-124">Passing NULL returns the standard interface for a messaging user, IID_IMailUser.</span></span> 
    
 <span data-ttu-id="90651-125">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="90651-125">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="90651-126">[out] Un puntero a la implementación de la interfaz que suministra el proveedor externo para obtener acceso a la entrada.</span><span class="sxs-lookup"><span data-stu-id="90651-126">[out] A pointer to the interface implementation that the foreign provider supplies for accessing the entry.</span></span>
    
 <span data-ttu-id="90651-127">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="90651-127">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="90651-128">Reservado; debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="90651-128">Reserved; must be NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="90651-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90651-129">Return value</span></span>

<span data-ttu-id="90651-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="90651-130">S_OK</span></span> 
  
> <span data-ttu-id="90651-131">El proceso de enlace fue correcto.</span><span class="sxs-lookup"><span data-stu-id="90651-131">The binding process was successful.</span></span>
    
<span data-ttu-id="90651-132">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="90651-132">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="90651-133">El proveedor de libreta de direcciones externa no existe.</span><span class="sxs-lookup"><span data-stu-id="90651-133">The foreign address book provider doesn't exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="90651-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="90651-134">Remarks</span></span>

<span data-ttu-id="90651-135">El método **IMAPISupport::OpenTemplateID** se implementa sólo para los objetos de compatibilidad con de proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="90651-135">The **IMAPISupport::OpenTemplateID** method is implemented only for address book provider support objects.</span></span> <span data-ttu-id="90651-136">Se denomina **OpenTemplateID** sólo por los proveedores de la libreta de direcciones que pueden actuar como hosts para las entradas que pertenecen a otros proveedores de libreta de direcciones, también conocido como externos proveedores.</span><span class="sxs-lookup"><span data-stu-id="90651-136">**OpenTemplateID** is called only by address book providers that can act as hosts for entries that belong to other address book providers, also known as foreign providers.</span></span> <span data-ttu-id="90651-137">Proveedores de host llame a **OpenTemplateID** para abrir una entrada externa, que se produce cuando se enlazan datos en el proveedor de host al código en el proveedor extranjero.</span><span class="sxs-lookup"><span data-stu-id="90651-137">Host providers call **OpenTemplateID** to open a foreign entry, which occurs when data in the host provider is bound to code in the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="90651-138">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="90651-138">Notes to callers</span></span>

<span data-ttu-id="90651-139">Llamar a **OpenTemplateID** sólo si se admite el almacenamiento de entradas con identificadores de plantilla desde los proveedores de la libreta de direcciones externa.</span><span class="sxs-lookup"><span data-stu-id="90651-139">Call **OpenTemplateID** only if you support the storage of entries with template identifiers from foreign address book providers.</span></span> <span data-ttu-id="90651-140">Este soporte coloca los requisitos adicionales en sus implementaciones de [IABContainer::CreateEntry](iabcontainer-createentry.md) y [IABLogon::OpenEntry](iablogon-openentry.md) .</span><span class="sxs-lookup"><span data-stu-id="90651-140">Such support places additional requirements on your [IABContainer::CreateEntry](iabcontainer-createentry.md) and [IABLogon::OpenEntry](iablogon-openentry.md) implementations.</span></span> <span data-ttu-id="90651-141">Para obtener más información, consulte las descripciones de estos métodos y [actúa como un proveedor de libreta de direcciones de Host](acting-as-a-host-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="90651-141">For more information, see the descriptions of these methods and [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
<span data-ttu-id="90651-142">Si la llamada **OpenTemplateID** devuelve como la interfaz enlazada la misma implementación de objeto de propiedad que pasa en, puede liberar la referencia al objeto (propiedad).</span><span class="sxs-lookup"><span data-stu-id="90651-142">If the **OpenTemplateID** call returns as the bound interface the same property object implementation that you passed in, you can release your reference to your property object.</span></span> <span data-ttu-id="90651-143">Esto es debido a que el proveedor externo ha llamado al método del objeto **AddRef** para mantener su propia referencia.</span><span class="sxs-lookup"><span data-stu-id="90651-143">This is because the foreign provider has called the object's **AddRef** method to keep its own reference.</span></span> <span data-ttu-id="90651-144">Si el proveedor externo no es necesario mantener una referencia al objeto de la propiedad, **OpenTemplateID** devolverá el objeto de propiedad independiente.</span><span class="sxs-lookup"><span data-stu-id="90651-144">If the foreign provider does not need to keep a reference to the property object, then **OpenTemplateID** will return the unbound property object.</span></span> 
  
<span data-ttu-id="90651-145">Si se produce un error en **OpenTemplateID** con MAPI_E_UNKNOWN_ENTRYID, intente continuar por el tratamiento de la entrada como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="90651-145">If **OpenTemplateID** fails with MAPI_E_UNKNOWN_ENTRYID, try to continue by treating the entry as read-only.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="90651-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="90651-146">See also</span></span>



[<span data-ttu-id="90651-147">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="90651-147">IABLogon::OpenTemplateID</span></span>](iablogon-opentemplateid.md)
  
[<span data-ttu-id="90651-148">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="90651-148">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="90651-149">Propiedad canónica PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="90651-149">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="90651-150">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="90651-150">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

