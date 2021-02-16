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
ms.openlocfilehash: 07aa508b473f4a87d5b4909f83771549c301a600
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418508"
---
# <a name="imapisupportopentemplateid"></a><span data-ttu-id="12d5a-103">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="12d5a-103">IMAPISupport::OpenTemplateID</span></span>

  
  
<span data-ttu-id="12d5a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12d5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12d5a-105">Abre una entrada de destinatario en un proveedor de libreta de direcciones externo.</span><span class="sxs-lookup"><span data-stu-id="12d5a-105">Opens a recipient entry in a foreign address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="12d5a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12d5a-106">Parameters</span></span>

 <span data-ttu-id="12d5a-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="12d5a-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="12d5a-108">[entrada] El recuento de bytes en el identificador de plantilla al que apunta  _lpTemplateID_.</span><span class="sxs-lookup"><span data-stu-id="12d5a-108">[in] The byte count in the template identifier pointed to by  _lpTemplateID_.</span></span> 
    
 <span data-ttu-id="12d5a-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="12d5a-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="12d5a-110">[entrada] Puntero al identificador de plantilla **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) de la entrada de destinatario que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="12d5a-110">[in] A pointer to the template identifier **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="12d5a-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="12d5a-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="12d5a-112">[entrada] Máscara de bits de marcas que se usa para describir cómo abrir la entrada.</span><span class="sxs-lookup"><span data-stu-id="12d5a-112">[in] A bitmask of flags used to describe how to open the entry.</span></span> <span data-ttu-id="12d5a-113">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="12d5a-113">The following flag can be set:</span></span>
    
<span data-ttu-id="12d5a-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="12d5a-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="12d5a-115">Se está creando una nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="12d5a-115">A new entry is being created.</span></span> <span data-ttu-id="12d5a-116">Cuando el proveedor externo recibe la llamada [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) posterior de MAPI, puede controlar cómo se crea la entrada modificando las propiedades a las que apunta el parámetro  _lpMAPIPropData_ o devolviendo una implementación de interfaz específica en  _lppMAPIPropNew_ para controlar cómo se establecen las propiedades de la nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="12d5a-116">When the foreign provider receives the subsequent [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) call from MAPI, it can control how the entry is created by modifying properties pointed to by the  _lpMAPIPropData_ parameter or by returning a specific interface implementation in  _lppMAPIPropNew_ to control how properties for the new entry are set.</span></span> 
    
 <span data-ttu-id="12d5a-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="12d5a-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="12d5a-118">[entrada] Puntero a la implementación de la interfaz que el autor de la llamada usa para obtener acceso a la entrada.</span><span class="sxs-lookup"><span data-stu-id="12d5a-118">[in] A pointer to the interface implementation that the caller uses to access the entry.</span></span> <span data-ttu-id="12d5a-119">Esta es la implementación que el proveedor externo puede encapsular con su propia implementación y devolver en el parámetro _lppMAPIPropNew._</span><span class="sxs-lookup"><span data-stu-id="12d5a-119">This is the implementation that the foreign provider can wrap with its own implementation and return in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="12d5a-120">El _parámetro lpMAPIPropData_ debe apuntar a una implementación de interfaz de lectura y escritura que deriva de [IMAPIProp : IUnknown](imapipropiunknown.md) y admite la interfaz que se solicita en el parámetro _lpInterface._</span><span class="sxs-lookup"><span data-stu-id="12d5a-120">The  _lpMAPIPropData_ parameter must point to a read/write interface implementation that derives from [IMAPIProp : IUnknown](imapipropiunknown.md) and supports the interface being requested in the  _lpInterface_ parameter.</span></span> 
    
 <span data-ttu-id="12d5a-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="12d5a-121">_lpInterface_</span></span>
  
> <span data-ttu-id="12d5a-122">[entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la entrada.</span><span class="sxs-lookup"><span data-stu-id="12d5a-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the entry.</span></span> <span data-ttu-id="12d5a-123">El  _parámetro lppMAPIPropNew_ apunta a una interfaz del tipo especificado por  _lpInterface_.</span><span class="sxs-lookup"><span data-stu-id="12d5a-123">The  _lppMAPIPropNew_ parameter points to an interface of the type specified by  _lpInterface_.</span></span> <span data-ttu-id="12d5a-124">Pasar NULL devuelve la interfaz estándar para un usuario de mensajería, IID_IMailUser.</span><span class="sxs-lookup"><span data-stu-id="12d5a-124">Passing NULL returns the standard interface for a messaging user, IID_IMailUser.</span></span> 
    
 <span data-ttu-id="12d5a-125">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="12d5a-125">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="12d5a-126">[salida] Puntero a la implementación de la interfaz que proporciona el proveedor externo para obtener acceso a la entrada.</span><span class="sxs-lookup"><span data-stu-id="12d5a-126">[out] A pointer to the interface implementation that the foreign provider supplies for accessing the entry.</span></span>
    
 <span data-ttu-id="12d5a-127">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="12d5a-127">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="12d5a-128">Reservado; debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="12d5a-128">Reserved; must be NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="12d5a-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12d5a-129">Return value</span></span>

<span data-ttu-id="12d5a-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="12d5a-130">S_OK</span></span> 
  
> <span data-ttu-id="12d5a-131">El proceso de enlace se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="12d5a-131">The binding process was successful.</span></span>
    
<span data-ttu-id="12d5a-132">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="12d5a-132">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="12d5a-133">El proveedor de libreta de direcciones externo no existe.</span><span class="sxs-lookup"><span data-stu-id="12d5a-133">The foreign address book provider doesn't exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="12d5a-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="12d5a-134">Remarks</span></span>

<span data-ttu-id="12d5a-135">El **método IMAPISupport::OpenTemplateID** solo se implementa para objetos de compatibilidad del proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="12d5a-135">The **IMAPISupport::OpenTemplateID** method is implemented only for address book provider support objects.</span></span> <span data-ttu-id="12d5a-136">**OpenTemplateID** solo lo llaman los proveedores de libretas de direcciones que pueden actuar como hosts para las entradas que pertenecen a otros proveedores de libretas de direcciones, también conocidos como proveedores externos.</span><span class="sxs-lookup"><span data-stu-id="12d5a-136">**OpenTemplateID** is called only by address book providers that can act as hosts for entries that belong to other address book providers, also known as foreign providers.</span></span> <span data-ttu-id="12d5a-137">Los proveedores de host llaman a **OpenTemplateID** para abrir una entrada externa, que se produce cuando los datos del proveedor de host están enlazados al código del proveedor externo.</span><span class="sxs-lookup"><span data-stu-id="12d5a-137">Host providers call **OpenTemplateID** to open a foreign entry, which occurs when data in the host provider is bound to code in the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="12d5a-138">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="12d5a-138">Notes to callers</span></span>

<span data-ttu-id="12d5a-139">Llame **a OpenTemplateID** solo si admite el almacenamiento de entradas con identificadores de plantilla de proveedores de libretas de direcciones externos.</span><span class="sxs-lookup"><span data-stu-id="12d5a-139">Call **OpenTemplateID** only if you support the storage of entries with template identifiers from foreign address book providers.</span></span> <span data-ttu-id="12d5a-140">Esta compatibilidad coloca requisitos adicionales en las implementaciones [IABContainer::CreateEntry](iabcontainer-createentry.md) e [IABLogon::OpenEntry.](iablogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="12d5a-140">Such support places additional requirements on your [IABContainer::CreateEntry](iabcontainer-createentry.md) and [IABLogon::OpenEntry](iablogon-openentry.md) implementations.</span></span> <span data-ttu-id="12d5a-141">Para obtener más información, vea las descripciones de estos métodos y [actuar como proveedor de libretas de direcciones de host.](acting-as-a-host-address-book-provider.md)</span><span class="sxs-lookup"><span data-stu-id="12d5a-141">For more information, see the descriptions of these methods and [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
<span data-ttu-id="12d5a-142">Si la **llamada a OpenTemplateID** devuelve como interfaz enlazada la misma implementación de objeto de propiedad que pasó, puede liberar la referencia al objeto de propiedad.</span><span class="sxs-lookup"><span data-stu-id="12d5a-142">If the **OpenTemplateID** call returns as the bound interface the same property object implementation that you passed in, you can release your reference to your property object.</span></span> <span data-ttu-id="12d5a-143">Esto se debe a que el proveedor externo ha llamado al método **AddRef** del objeto para mantener su propia referencia.</span><span class="sxs-lookup"><span data-stu-id="12d5a-143">This is because the foreign provider has called the object's **AddRef** method to keep its own reference.</span></span> <span data-ttu-id="12d5a-144">Si el proveedor externo no necesita mantener una referencia al objeto de propiedad, **OpenTemplateID** devolverá el objeto de propiedad independiente.</span><span class="sxs-lookup"><span data-stu-id="12d5a-144">If the foreign provider does not need to keep a reference to the property object, then **OpenTemplateID** will return the unbound property object.</span></span> 
  
<span data-ttu-id="12d5a-145">Si Se produce un error en **OpenTemplateID** MAPI_E_UNKNOWN_ENTRYID, intente continuar tratando la entrada como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="12d5a-145">If **OpenTemplateID** fails with MAPI_E_UNKNOWN_ENTRYID, try to continue by treating the entry as read-only.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="12d5a-146">Consulte también</span><span class="sxs-lookup"><span data-stu-id="12d5a-146">See also</span></span>



[<span data-ttu-id="12d5a-147">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="12d5a-147">IABLogon::OpenTemplateID</span></span>](iablogon-opentemplateid.md)
  
[<span data-ttu-id="12d5a-148">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="12d5a-148">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="12d5a-149">Propiedad canónica PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="12d5a-149">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="12d5a-150">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="12d5a-150">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

