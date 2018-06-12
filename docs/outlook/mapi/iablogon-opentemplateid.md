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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: f2fedd98fe84d7359aebaca8d03a20f392dae2b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817111"
---
# <a name="iablogonopentemplateid"></a><span data-ttu-id="0edd6-103">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="0edd6-103">IABLogon::OpenTemplateID</span></span>

  
  
<span data-ttu-id="0edd6-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0edd6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0edd6-105">Se abre una entrada del destinatario que tiene datos que residen en un proveedor de libreta de direcciones de host.</span><span class="sxs-lookup"><span data-stu-id="0edd6-105">Opens a recipient entry that has data residing in a host address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="0edd6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0edd6-106">Parameters</span></span>

 <span data-ttu-id="0edd6-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="0edd6-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="0edd6-108">[entrada] El número de bytes en el identificador de plantilla indicado por el parámetro _lpTemplateID_ .</span><span class="sxs-lookup"><span data-stu-id="0edd6-108">[in] The byte count in the template identifier pointed to by the  _lpTemplateID_ parameter.</span></span> 
    
 <span data-ttu-id="0edd6-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="0edd6-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="0edd6-110">[entrada] Un puntero al identificador de plantilla, o la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), de la entrada del destinatario que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="0edd6-110">[in] A pointer to the template identifier, or **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="0edd6-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="0edd6-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="0edd6-112">[entrada] Una máscara de bits de indicadores que se utilizan para indicar cómo abrir la entrada representada por el identificador de plantilla.</span><span class="sxs-lookup"><span data-stu-id="0edd6-112">[in] A bitmask of flags used to indicate how to open the entry represented by the template identifier.</span></span> <span data-ttu-id="0edd6-113">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="0edd6-113">The following flag can be set:</span></span>
    
<span data-ttu-id="0edd6-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="0edd6-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="0edd6-115">El proveedor de host está creando una nueva entrada en su contenedor en función de la entrada representada por el identificador de plantilla.</span><span class="sxs-lookup"><span data-stu-id="0edd6-115">The host provider is creating a new entry in its container based on the entry represented by the template identifier.</span></span> <span data-ttu-id="0edd6-116">El método **IABLogon::OpenTemplateID** ya sea debe realizar la inicialización específica de entrada del proveedor de host mediante el uso de la [IMAPIProp: IUnknown](imapipropiunknown.md) implementación en el parámetro _lpMAPIPropData_ o retorno personalizado **IMAPIProp **implementación en el parámetro _lppMAPIPropNew_ de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="0edd6-116">The **IABLogon::OpenTemplateID** method should either perform specific initialization of the host provider's entry by using the [IMAPIProp : IUnknown](imapipropiunknown.md) implementation in the  _lpMAPIPropData_ parameter, or return a custom **IMAPIProp** interface implementation in the  _lppMAPIPropNew_ parameter.</span></span> 
    
 <span data-ttu-id="0edd6-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="0edd6-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="0edd6-118">[entrada] Un puntero al objeto de la propiedad del proveedor de host y la implementación de una interfaz deriva de **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="0edd6-118">[in] A pointer to the host provider's property object and implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="0edd6-119">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0edd6-119">_lpInterface_</span></span>
  
> <span data-ttu-id="0edd6-120">[entrada] Un puntero al identificador de interfaz (IID) que representa el tipo de puntero de interfaz que se devuelve en el parámetro _lppMAPIPropNew_ .</span><span class="sxs-lookup"><span data-stu-id="0edd6-120">[in] A pointer to the interface identifier (IID) that represents the type of interface pointer to be returned in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="0edd6-121">Si se pasa **null** devuelve el estándar de mensajería de la interfaz de usuario, [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="0edd6-121">Passing **null** returns the standard messaging user interface, [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span>
    
 <span data-ttu-id="0edd6-122">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="0edd6-122">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="0edd6-123">[out] Un puntero al objeto de la propiedad enlazada y una implementación de una interfaz que se deriva de **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="0edd6-123">[out] A pointer to the bound property object and an implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="0edd6-124">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="0edd6-124">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="0edd6-125">[out] Reservado; debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="0edd6-125">[out] Reserved; must be **null**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0edd6-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0edd6-126">Return value</span></span>

<span data-ttu-id="0edd6-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="0edd6-127">S_OK</span></span> 
  
> <span data-ttu-id="0edd6-128">El código correspondiente se enlazó correctamente a los datos relacionados en el proveedor de host.</span><span class="sxs-lookup"><span data-stu-id="0edd6-128">The appropriate code was successfully bound to related data in the host provider.</span></span>
    
<span data-ttu-id="0edd6-129">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="0edd6-129">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="0edd6-130">El objeto no es compatible con los identificadores de plantilla.</span><span class="sxs-lookup"><span data-stu-id="0edd6-130">The object does not support template IDs.</span></span>
    
<span data-ttu-id="0edd6-131">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0edd6-131">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="0edd6-132">No se reconoce el identificador de plantilla que se pasa en el parámetro _lpTemplateID_ por el proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="0edd6-132">The template identifier passed in the  _lpTemplateID_ parameter is not recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0edd6-133">Notas</span><span class="sxs-lookup"><span data-stu-id="0edd6-133">Remarks</span></span>

<span data-ttu-id="0edd6-134">El método **IABLogon::OpenTemplateID** se implementa sólo por los proveedores de la libreta de direcciones que necesitan para mantener el control sobre las copias de sus entradas que se encuentran en los contenedores de los proveedores de host.</span><span class="sxs-lookup"><span data-stu-id="0edd6-134">The **IABLogon::OpenTemplateID** method is implemented only by address book providers that need to maintain control over copies of their entries that are located in the containers of host providers.</span></span> <span data-ttu-id="0edd6-135">Proveedores que implementan **OpenTemplateID** se conocen como los proveedores de la libreta de direcciones externa.</span><span class="sxs-lookup"><span data-stu-id="0edd6-135">Providers that implement **OpenTemplateID** are known as foreign address book providers.</span></span> <span data-ttu-id="0edd6-136">Proveedores de host llame a [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para crear una entrada copiada o abrir la entrada copiada y MAPI se pasa en la llamada a **IABLogon::OpenTemplateID**.</span><span class="sxs-lookup"><span data-stu-id="0edd6-136">Host providers call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to create a copied entry or open the copied entry, and MAPI passes on the call to **IABLogon::OpenTemplateID**.</span></span> <span data-ttu-id="0edd6-137">**IABLogon::OpenTemplateID** abre la entrada y enlaza el código que controla a los datos en el proveedor de host.</span><span class="sxs-lookup"><span data-stu-id="0edd6-137">**IABLogon::OpenTemplateID** opens the entry and binds the code that controls it to data in the host provider.</span></span> 
  
<span data-ttu-id="0edd6-138">En lugar de usar un identificador de entrada, **IABLogon::OpenTemplateID** usa otra propiedad, identificador de la plantilla de la entrada, **PR_TEMPLATEID**.</span><span class="sxs-lookup"><span data-stu-id="0edd6-138">Rather than use an entry identifier, **IABLogon::OpenTemplateID** uses another property, the entry's template identifier, **PR_TEMPLATEID**.</span></span> <span data-ttu-id="0edd6-139">Identificadores de plantilla deben admitirse en entradas cuyo código debe estar enlazado a datos en un proveedor de host.</span><span class="sxs-lookup"><span data-stu-id="0edd6-139">Template identifiers should be supported for entries whose code must be bound to data in a host provider.</span></span>
  
<span data-ttu-id="0edd6-140">Algunos ejemplos de cuándo un proveedor de la libreta de direcciones debe implementar **IABLogon::OpenTemplateID** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="0edd6-140">Some examples of when an address book provider should implement **IABLogon::OpenTemplateID** are as follows:</span></span> 
  
- <span data-ttu-id="0edd6-141">Para actualizar los datos para una entrada de copiado periódicamente para que se mantenga sincronizada con el original.</span><span class="sxs-lookup"><span data-stu-id="0edd6-141">To periodically update the data for a copied entry so that it stays synchronized with the original.</span></span>
    
- <span data-ttu-id="0edd6-142">Para implementar la funcionalidad que no se puede implementar el proveedor de host, como rellenar dinámicamente una lista que aparece en la tabla de detalles de la entrada de datos en un servidor.</span><span class="sxs-lookup"><span data-stu-id="0edd6-142">To implement functionality that the host provider cannot implement, such as dynamically populating a list that appears in the entry's details table from data on a server.</span></span>
    
- <span data-ttu-id="0edd6-143">Para controlar la interacción entre las propiedades de entrada del proveedor de host y la entrada original, como los sistemas de la **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) de los valores de los controles de edición en la pantalla de detalles que contienen diferentes componentes de la dirección.</span><span class="sxs-lookup"><span data-stu-id="0edd6-143">To control the interaction between properties in the host provider's entry and the original entry, such as computing the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) from the values of the edit controls in the details display that contain different components of the address.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="0edd6-144">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="0edd6-144">Notes to implementers</span></span>

<span data-ttu-id="0edd6-145">Cuando un proveedor de host copia o crea una entrada de su proveedor y proporcionar una implementación de objeto de la propiedad a través de **IABLogon::OpenTemplateID**, controlar la mayoría de las llamadas para mantener la entrada.</span><span class="sxs-lookup"><span data-stu-id="0edd6-145">When a host provider copies or creates an entry from your provider and you supply a property object implementation through **IABLogon::OpenTemplateID**, you handle most of the calls to maintain the entry.</span></span> <span data-ttu-id="0edd6-146">Sin embargo, porque es el proveedor de host para reenviar estas llamadas a usted, el proveedor de host puede interceptar cualquier llamada y realizar un procesamiento personalizado antes de reenviar la llamada.</span><span class="sxs-lookup"><span data-stu-id="0edd6-146">However, because it is up to the host provider to forward these calls to you, the host provider can intercept any call and perform custom processing before forwarding the call.</span></span>
  
<span data-ttu-id="0edd6-147">Debe usar las siguientes instrucciones en las implementaciones de objeto de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="0edd6-147">You should use the following guidelines in your property object implementations:</span></span>
  
- <span data-ttu-id="0edd6-148">Cuando se llama a [IMAPIProp::GetProps](imapiprop-getprops.md) , determine si la solicitud es para una propiedad calculada y, si es así, controlarla.</span><span class="sxs-lookup"><span data-stu-id="0edd6-148">When [IMAPIProp::GetProps](imapiprop-getprops.md) is called, determine whether the request is for a computed property and, if it is, handle it.</span></span> <span data-ttu-id="0edd6-149">Transferir todas las solicitudes de propiedades no calculadas para el proveedor de host.</span><span class="sxs-lookup"><span data-stu-id="0edd6-149">Transfer all requests for noncomputed properties to the host provider.</span></span> 
    
- <span data-ttu-id="0edd6-150">Cuando se llama a [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir cualquier tabla excepto los detalles de mostrar tabla, controlar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0edd6-150">When [IMAPIProp::OpenProperty](imapiprop-openproperty.md) is called to open any table except the details display table, handle the request.</span></span> <span data-ttu-id="0edd6-151">La mayoría de las tablas no se puede copiar con exactitud para el proveedor de host.</span><span class="sxs-lookup"><span data-stu-id="0edd6-151">Most tables cannot be copied accurately to the host provider.</span></span> <span data-ttu-id="0edd6-152">Debe generar la implementación de **IMAPITable** para estas tablas solicitadas.</span><span class="sxs-lookup"><span data-stu-id="0edd6-152">You must generate the **IMAPITable** implementation for these requested tables.</span></span> <span data-ttu-id="0edd6-153">La propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) de tabla de detalles debe copiarse en el proveedor de host.</span><span class="sxs-lookup"><span data-stu-id="0edd6-153">The details table **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property must be copied to the host provider.</span></span> <span data-ttu-id="0edd6-154">Esto permite que este proveedor generar la tabla localmente.</span><span class="sxs-lookup"><span data-stu-id="0edd6-154">This allows this provider to generate the table locally.</span></span> <span data-ttu-id="0edd6-155">Es posible que desee ajustar la implementación de la tabla para mostrar para generar notificaciones de tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="0edd6-155">You might want to wrap the display table implementation to generate display table notifications.</span></span> 
    
- <span data-ttu-id="0edd6-156">Cuando se llama a [IMAPIProp::SetProps](imapiprop-setprops.md) , el proveedor de host puede validar los datos antes de lo que le permite establecer las propiedades.</span><span class="sxs-lookup"><span data-stu-id="0edd6-156">When [IMAPIProp::SetProps](imapiprop-setprops.md) is called, the host provider can validate the data before letting you set the properties.</span></span> <span data-ttu-id="0edd6-157">Puede comprobar que todas las propiedades necesarias se han establecido o calculado.</span><span class="sxs-lookup"><span data-stu-id="0edd6-157">You can verify that all of the necessary properties were set or computed.</span></span> <span data-ttu-id="0edd6-158">Si se detecta un error, devuelva el valor de error apropiado y, si es posible, cualquier explicación adicional a través de [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span><span class="sxs-lookup"><span data-stu-id="0edd6-158">If an error is detected, return the appropriate error value and, if you can, any additional explanation through [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span>
    
- <span data-ttu-id="0edd6-159">Cuando se llama a [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , el proveedor de host es posible que desee realizar un procesamiento antes de guardar la entrada.</span><span class="sxs-lookup"><span data-stu-id="0edd6-159">When [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called, the host provider might want to perform processing before you save the entry.</span></span> <span data-ttu-id="0edd6-160">Debe guardar todos los datos que se ve afectados por las propiedades modificadas, como una dirección nueva, en la entrada del proveedor de host.</span><span class="sxs-lookup"><span data-stu-id="0edd6-160">You should save any data that is affected by the changed properties, such as a new address, in the host provider's entry.</span></span> 
    
<span data-ttu-id="0edd6-161">En general, hacer que la implementación de la entrada que se pasa al proveedor de host todos los métodos para manipular los específicos del contexto de las propiedades relevantes intercept.</span><span class="sxs-lookup"><span data-stu-id="0edd6-161">In general, make your implementation of the entry that you pass back to the host provider intercept all of the methods to perform context-specific manipulation of the relevant properties.</span></span> <span data-ttu-id="0edd6-162">Si la marca FILL_ENTRY se pasa en el parámetro _ulTemplateFlags_ , establezca todas las propiedades de la entrada.</span><span class="sxs-lookup"><span data-stu-id="0edd6-162">If the FILL_ENTRY flag is passed in the  _ulTemplateFlags_ parameter, set all properties for the entry.</span></span> 
  
<span data-ttu-id="0edd6-163">Si se devuelve un nuevo objeto property en el parámetro _lppMAPIPropNew_ , llame al método [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) del objeto de propiedad del proveedor de host para mantener una referencia.</span><span class="sxs-lookup"><span data-stu-id="0edd6-163">If you return a new property object in the  _lppMAPIPropNew_ parameter, call the [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) method of the host provider's property object to maintain a reference.</span></span> <span data-ttu-id="0edd6-164">Todas las llamadas a través del objeto dependiente que devuelve la implementación de **IMAPIProp** en _lppMAPIPropNew_ deben enrutarse a su método correspondiente en el objeto de la propiedad host después de que se tratarán por el objeto dependiente.</span><span class="sxs-lookup"><span data-stu-id="0edd6-164">All calls through the bound object that the **IMAPIProp** implementation returned in  _lppMAPIPropNew_ should be routed to their corresponding method in the host property object after they are dealt with by the bound object.</span></span> 
  
<span data-ttu-id="0edd6-165">Los identificadores de propiedad de las propiedades con nombre que se pasan a través de su objeto dependiente (propiedad) se encuentran en el espacio de nombres de identificador del proveedor.</span><span class="sxs-lookup"><span data-stu-id="0edd6-165">The property identifiers of any named properties that are passed through your bound property object are in your provider's identifier namespace.</span></span> <span data-ttu-id="0edd6-166">La implementación del método [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) debe determinar los nombres de las propiedades de modo que pueda realizar las tareas específicas de las plantillas.</span><span class="sxs-lookup"><span data-stu-id="0edd6-166">Your implementation of the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method should determine the names of the properties so that it can perform any template-specific tasks.</span></span> <span data-ttu-id="0edd6-167">De forma similar, también deben ser propiedades que pasa el proveedor el proveedor de host en el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="0edd6-167">Similarly, properties that your provider passes on to the host provider must also be in your namespace.</span></span> <span data-ttu-id="0edd6-168">Por ejemplo, si establece una propiedad con nombre en **OpenTemplateID**, se debe utilizar uno de los identificadores para el nombre, crear, si es necesario, llamando al método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="0edd6-168">For example, if you set a named property in **OpenTemplateID**, you should use one of your identifiers for the name—creating it, if necessary, by calling the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="0edd6-169">Si no reconoce el identificador de entrada que se pasan en _lpTemplateID_, devolver MAPI_E_UNKNOWN_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="0edd6-169">If you do not recognize the entry identifier passed in  _lpTemplateID_, return MAPI_E_UNKNOWN_ENTRYID.</span></span>
  
<span data-ttu-id="0edd6-170">Para obtener más información acerca de cómo trabajar con identificadores de plantilla de la libreta de direcciones, vea [actuar como un proveedor de libreta de direcciones externa](acting-as-a-foreign-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0edd6-170">For more information about how to work with address book template identifiers, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0edd6-171">Ver también</span><span class="sxs-lookup"><span data-stu-id="0edd6-171">See also</span></span>



[<span data-ttu-id="0edd6-172">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="0edd6-172">IMAPISupport::OpenTemplateID</span></span>](imapisupport-opentemplateid.md)
  
[<span data-ttu-id="0edd6-173">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0edd6-173">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="0edd6-174">Propiedad canónico PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="0edd6-174">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="0edd6-175">IABLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0edd6-175">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

