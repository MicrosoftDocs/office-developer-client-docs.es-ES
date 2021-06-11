---
title: IABLogonOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenTemplateID
api_type:
- COM
ms.assetid: 751c36d3-c39e-4357-a60a-88685a378de0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bc68878a25873533162df7e1671e483c3bb77865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334751"
---
# <a name="iablogonopentemplateid"></a><span data-ttu-id="e2d0e-103">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="e2d0e-103">IABLogon::OpenTemplateID</span></span>

  
  
<span data-ttu-id="e2d0e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2d0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2d0e-105">Abre una entrada de destinatario que tiene datos que residen en un proveedor de libreta de direcciones host.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-105">Opens a recipient entry that has data residing in a host address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="e2d0e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e2d0e-106">Parameters</span></span>

 <span data-ttu-id="e2d0e-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="e2d0e-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="e2d0e-108">[in] Recuento de bytes en el identificador de plantilla al que apunta el _parámetro lpTemplateID._</span><span class="sxs-lookup"><span data-stu-id="e2d0e-108">[in] The byte count in the template identifier pointed to by the  _lpTemplateID_ parameter.</span></span> 
    
 <span data-ttu-id="e2d0e-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="e2d0e-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="e2d0e-110">[in] Puntero al identificador de plantilla o **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) de la entrada de destinatario que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-110">[in] A pointer to the template identifier, or **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="e2d0e-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="e2d0e-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="e2d0e-112">[in] Máscara de bits de marcas usadas para indicar cómo abrir la entrada representada por el identificador de plantilla.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-112">[in] A bitmask of flags used to indicate how to open the entry represented by the template identifier.</span></span> <span data-ttu-id="e2d0e-113">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="e2d0e-113">The following flag can be set:</span></span>
    
<span data-ttu-id="e2d0e-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="e2d0e-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="e2d0e-115">El proveedor de host está creando una nueva entrada en su contenedor en función de la entrada representada por el identificador de plantilla.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-115">The host provider is creating a new entry in its container based on the entry represented by the template identifier.</span></span> <span data-ttu-id="e2d0e-116">El método **IABLogon::OpenTemplateID** debe realizar una inicialización específica de la entrada del proveedor de host mediante la implementación [IMAPIProp : IUnknown](imapipropiunknown.md) en el parámetro _lpMAPIPropData_ o devolver una implementación de interfaz **IMAPIProp** personalizada en el parámetro _lppMAPIPropNew._</span><span class="sxs-lookup"><span data-stu-id="e2d0e-116">The **IABLogon::OpenTemplateID** method should either perform specific initialization of the host provider's entry by using the [IMAPIProp : IUnknown](imapipropiunknown.md) implementation in the  _lpMAPIPropData_ parameter, or return a custom **IMAPIProp** interface implementation in the  _lppMAPIPropNew_ parameter.</span></span> 
    
 <span data-ttu-id="e2d0e-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="e2d0e-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="e2d0e-118">[in] Puntero al objeto de propiedad del proveedor de host e implementación de una interfaz derivada de **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-118">[in] A pointer to the host provider's property object and implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="e2d0e-119">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="e2d0e-119">_lpInterface_</span></span>
  
> <span data-ttu-id="e2d0e-120">[in] Puntero al identificador de interfaz (IID) que representa el tipo de puntero de interfaz que se devolverá en el parámetro _lppMAPIPropNew._</span><span class="sxs-lookup"><span data-stu-id="e2d0e-120">[in] A pointer to the interface identifier (IID) that represents the type of interface pointer to be returned in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="e2d0e-121">Si **se pasa null,** se devuelve la interfaz de usuario de mensajería estándar, [IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="e2d0e-121">Passing **null** returns the standard messaging user interface, [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span>
    
 <span data-ttu-id="e2d0e-122">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="e2d0e-122">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="e2d0e-123">[salida] Puntero al objeto de propiedad enlazado y una implementación de una interfaz derivada de **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-123">[out] A pointer to the bound property object and an implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="e2d0e-124">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="e2d0e-124">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="e2d0e-125">[salida] Reservado; debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-125">[out] Reserved; must be **null**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e2d0e-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2d0e-126">Return value</span></span>

<span data-ttu-id="e2d0e-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="e2d0e-127">S_OK</span></span> 
  
> <span data-ttu-id="e2d0e-128">El código adecuado se enlaza correctamente a datos relacionados en el proveedor de host.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-128">The appropriate code was successfully bound to related data in the host provider.</span></span>
    
<span data-ttu-id="e2d0e-129">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e2d0e-129">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="e2d0e-130">El objeto no admite los IDs de plantilla.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-130">The object does not support template IDs.</span></span>
    
<span data-ttu-id="e2d0e-131">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e2d0e-131">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="e2d0e-132">El proveedor de libreta de direcciones no reconoce el identificador de plantilla pasado en el parámetro _lpTemplateID._</span><span class="sxs-lookup"><span data-stu-id="e2d0e-132">The template identifier passed in the  _lpTemplateID_ parameter is not recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e2d0e-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2d0e-133">Remarks</span></span>

<span data-ttu-id="e2d0e-134">El **método IABLogon::OpenTemplateID** solo lo implementan los proveedores de libreta de direcciones que necesitan mantener el control sobre las copias de sus entradas que se encuentran en los contenedores de los proveedores de host.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-134">The **IABLogon::OpenTemplateID** method is implemented only by address book providers that need to maintain control over copies of their entries that are located in the containers of host providers.</span></span> <span data-ttu-id="e2d0e-135">Los proveedores que implementan **OpenTemplateID** se conocen como proveedores de libretas de direcciones externos.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-135">Providers that implement **OpenTemplateID** are known as foreign address book providers.</span></span> <span data-ttu-id="e2d0e-136">Los proveedores de host llaman a [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para crear una entrada copiada o abrir la entrada copiada, y MAPI pasa la llamada a **IABLogon::OpenTemplateID**.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-136">Host providers call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to create a copied entry or open the copied entry, and MAPI passes on the call to **IABLogon::OpenTemplateID**.</span></span> <span data-ttu-id="e2d0e-137">**IABLogon::OpenTemplateID** abre la entrada y enlaza el código que la controla a los datos del proveedor de host.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-137">**IABLogon::OpenTemplateID** opens the entry and binds the code that controls it to data in the host provider.</span></span> 
  
<span data-ttu-id="e2d0e-138">En lugar de usar un identificador de entrada, **IABLogon::OpenTemplateID** usa otra propiedad, el identificador de plantilla de la **entrada, PR_TEMPLATEID**.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-138">Rather than use an entry identifier, **IABLogon::OpenTemplateID** uses another property, the entry's template identifier, **PR_TEMPLATEID**.</span></span> <span data-ttu-id="e2d0e-139">Los identificadores de plantilla deben ser compatibles con entradas cuyo código debe enlazarse a datos en un proveedor de host.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-139">Template identifiers should be supported for entries whose code must be bound to data in a host provider.</span></span>
  
<span data-ttu-id="e2d0e-140">Algunos ejemplos de cuándo un proveedor de libreta de direcciones debe implementar **IABLogon::OpenTemplateID** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e2d0e-140">Some examples of when an address book provider should implement **IABLogon::OpenTemplateID** are as follows:</span></span> 
  
- <span data-ttu-id="e2d0e-141">Para actualizar periódicamente los datos de una entrada copiada de modo que se mantenga sincronizado con el original.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-141">To periodically update the data for a copied entry so that it stays synchronized with the original.</span></span>
    
- <span data-ttu-id="e2d0e-142">Para implementar funciones que el proveedor de host no puede implementar, como rellenar dinámicamente una lista que aparece en la tabla de detalles de la entrada a partir de datos de un servidor.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-142">To implement functionality that the host provider cannot implement, such as dynamically populating a list that appears in the entry's details table from data on a server.</span></span>
    
- <span data-ttu-id="e2d0e-143">Para controlar la interacción entre las propiedades de la entrada del proveedor de host y la entrada original, como calcular **el PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) a partir de los valores de los controles de edición en la presentación de detalles que contienen diferentes componentes de la dirección.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-143">To control the interaction between properties in the host provider's entry and the original entry, such as computing the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) from the values of the edit controls in the details display that contain different components of the address.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="e2d0e-144">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="e2d0e-144">Notes to implementers</span></span>

<span data-ttu-id="e2d0e-145">Cuando un proveedor de host copia o crea una entrada del proveedor y proporciona una implementación de objeto de propiedad a través de **IABLogon::OpenTemplateID,** controla la mayoría de las llamadas para mantener la entrada.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-145">When a host provider copies or creates an entry from your provider and you supply a property object implementation through **IABLogon::OpenTemplateID**, you handle most of the calls to maintain the entry.</span></span> <span data-ttu-id="e2d0e-146">Sin embargo, dado que es el proveedor de host el que le reenvía estas llamadas, el proveedor de host puede interceptar cualquier llamada y realizar un procesamiento personalizado antes de reenviar la llamada.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-146">However, because it is up to the host provider to forward these calls to you, the host provider can intercept any call and perform custom processing before forwarding the call.</span></span>
  
<span data-ttu-id="e2d0e-147">Debe usar las siguientes directrices en las implementaciones de objetos de propiedad:</span><span class="sxs-lookup"><span data-stu-id="e2d0e-147">You should use the following guidelines in your property object implementations:</span></span>
  
- <span data-ttu-id="e2d0e-148">Cuando se llama a [IMAPIProp::GetProps,](imapiprop-getprops.md) determine si la solicitud es para una propiedad calculada y, si es así, controlarla.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-148">When [IMAPIProp::GetProps](imapiprop-getprops.md) is called, determine whether the request is for a computed property and, if it is, handle it.</span></span> <span data-ttu-id="e2d0e-149">Transferir todas las solicitudes de propiedades no comedida al proveedor de host.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-149">Transfer all requests for noncomputed properties to the host provider.</span></span> 
    
- <span data-ttu-id="e2d0e-150">Cuando [se llama a IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir cualquier tabla excepto la tabla para mostrar detalles, controla la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-150">When [IMAPIProp::OpenProperty](imapiprop-openproperty.md) is called to open any table except the details display table, handle the request.</span></span> <span data-ttu-id="e2d0e-151">La mayoría de las tablas no se pueden copiar con precisión en el proveedor de host.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-151">Most tables cannot be copied accurately to the host provider.</span></span> <span data-ttu-id="e2d0e-152">Debe generar la implementación **de IMAPITable** para estas tablas solicitadas.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-152">You must generate the **IMAPITable** implementation for these requested tables.</span></span> <span data-ttu-id="e2d0e-153">La tabla de **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) debe copiarse en el proveedor de host.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-153">The details table **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property must be copied to the host provider.</span></span> <span data-ttu-id="e2d0e-154">Esto permite a este proveedor generar la tabla localmente.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-154">This allows this provider to generate the table locally.</span></span> <span data-ttu-id="e2d0e-155">Es posible que desee ajustar la implementación de la tabla para mostrar para generar notificaciones de tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-155">You might want to wrap the display table implementation to generate display table notifications.</span></span> 
    
- <span data-ttu-id="e2d0e-156">Cuando [se llama a IMAPIProp::SetProps,](imapiprop-setprops.md) el proveedor de host puede validar los datos antes de permitirle establecer las propiedades.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-156">When [IMAPIProp::SetProps](imapiprop-setprops.md) is called, the host provider can validate the data before letting you set the properties.</span></span> <span data-ttu-id="e2d0e-157">Puede comprobar que todas las propiedades necesarias se han establecido o calculado.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-157">You can verify that all of the necessary properties were set or computed.</span></span> <span data-ttu-id="e2d0e-158">Si se detecta un error, devuelva el valor de error adecuado y, si puede, cualquier explicación adicional a través de [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span><span class="sxs-lookup"><span data-stu-id="e2d0e-158">If an error is detected, return the appropriate error value and, if you can, any additional explanation through [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span>
    
- <span data-ttu-id="e2d0e-159">Cuando [se llama a IMAPIProp::SaveChanges,](imapiprop-savechanges.md) es posible que el proveedor de host desee realizar el procesamiento antes de guardar la entrada.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-159">When [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called, the host provider might want to perform processing before you save the entry.</span></span> <span data-ttu-id="e2d0e-160">Debe guardar los datos que se ven afectados por las propiedades modificadas, como una nueva dirección, en la entrada del proveedor de host.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-160">You should save any data that is affected by the changed properties, such as a new address, in the host provider's entry.</span></span> 
    
<span data-ttu-id="e2d0e-161">En general, realice la implementación de la entrada que pase de nuevo al proveedor de host interceptar todos los métodos para realizar una manipulación específica del contexto de las propiedades relevantes.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-161">In general, make your implementation of the entry that you pass back to the host provider intercept all of the methods to perform context-specific manipulation of the relevant properties.</span></span> <span data-ttu-id="e2d0e-162">Si la FILL_ENTRY se pasa en el  _parámetro ulTemplateFlags,_ establezca todas las propiedades de la entrada.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-162">If the FILL_ENTRY flag is passed in the  _ulTemplateFlags_ parameter, set all properties for the entry.</span></span> 
  
<span data-ttu-id="e2d0e-163">Si devuelve un nuevo objeto de propiedad en el parámetro  _lppMAPIPropNew,_ llame al método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) del objeto de propiedad del proveedor de host para mantener una referencia.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-163">If you return a new property object in the  _lppMAPIPropNew_ parameter, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method of the host provider's property object to maintain a reference.</span></span> <span data-ttu-id="e2d0e-164">Todas las llamadas a través del objeto enlazado que la implementación **IMAPIProp** devuelta en  _lppMAPIPropNew_ se deben enrutar a su método correspondiente en el objeto de propiedad host después de que el objeto enlazado las ocupe.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-164">All calls through the bound object that the **IMAPIProp** implementation returned in  _lppMAPIPropNew_ should be routed to their corresponding method in the host property object after they are dealt with by the bound object.</span></span> 
  
<span data-ttu-id="e2d0e-165">Los identificadores de propiedad de las propiedades con nombre que se pasan a través del objeto de propiedad enlazada se encuentran en el espacio de nombres de identificador del proveedor.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-165">The property identifiers of any named properties that are passed through your bound property object are in your provider's identifier namespace.</span></span> <span data-ttu-id="e2d0e-166">La implementación del método [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) debe determinar los nombres de las propiedades para que pueda realizar tareas específicas de plantilla.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-166">Your implementation of the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method should determine the names of the properties so that it can perform any template-specific tasks.</span></span> <span data-ttu-id="e2d0e-167">Del mismo modo, las propiedades que el proveedor pasa al proveedor de host también deben estar en el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-167">Similarly, properties that your provider passes on to the host provider must also be in your namespace.</span></span> <span data-ttu-id="e2d0e-168">Por ejemplo, si establece una propiedad con nombre en **OpenTemplateID,** debe usar uno de los identificadores para el nombre, para crearla, si es necesario, llamando al método [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="e2d0e-168">For example, if you set a named property in **OpenTemplateID**, you should use one of your identifiers for the name—creating it, if necessary, by calling the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="e2d0e-169">Si no reconoce el identificador de entrada pasado en  _lpTemplateID,_ devuelva MAPI_E_UNKNOWN_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-169">If you do not recognize the entry identifier passed in  _lpTemplateID_, return MAPI_E_UNKNOWN_ENTRYID.</span></span>
  
<span data-ttu-id="e2d0e-170">Para obtener más información acerca de cómo trabajar con identificadores de plantilla de libreta de direcciones, vea [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e2d0e-170">For more information about how to work with address book template identifiers, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e2d0e-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2d0e-171">See also</span></span>



[<span data-ttu-id="e2d0e-172">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="e2d0e-172">IMAPISupport::OpenTemplateID</span></span>](imapisupport-opentemplateid.md)
  
[<span data-ttu-id="e2d0e-173">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e2d0e-173">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="e2d0e-174">Propiedad canónica PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="e2d0e-174">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="e2d0e-175">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2d0e-175">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

