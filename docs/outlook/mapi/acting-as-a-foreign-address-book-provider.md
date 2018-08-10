---
title: Que actúa como un proveedor de libreta de direcciones externa
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6d532ed4-7dc5-46a9-995a-72bc97d16f6e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 16c3518ab4efddbd68765d9de94db64b4fdc0b64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816375"
---
# <a name="acting-as-a-foreign-address-book-provider"></a><span data-ttu-id="216b9-103">Que actúa como un proveedor de libreta de direcciones externa</span><span class="sxs-lookup"><span data-stu-id="216b9-103">Acting as a foreign address book provider</span></span>

<span data-ttu-id="216b9-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="216b9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="216b9-105">Un proveedor externo es un proveedor de la libreta de direcciones que:</span><span class="sxs-lookup"><span data-stu-id="216b9-105">A foreign provider is an address book provider that:</span></span> 
  
- <span data-ttu-id="216b9-106">Asigna identificadores de plantilla para sus destinatarios.</span><span class="sxs-lookup"><span data-stu-id="216b9-106">Assigns template identifiers for its recipients.</span></span>
    
- <span data-ttu-id="216b9-107">Admite el método [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) .</span><span class="sxs-lookup"><span data-stu-id="216b9-107">Supports the [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> 
    
- <span data-ttu-id="216b9-108">Proporciona el código para el mantenimiento de los destinatarios que existen en los contenedores de otros proveedores de libreta de direcciones conocidos como proveedores de host.</span><span class="sxs-lookup"><span data-stu-id="216b9-108">Supplies code for maintaining recipients that exist in the containers of other address book providers known as host providers.</span></span> <span data-ttu-id="216b9-109">Este código implica un objeto property, normalmente una **IMAPIProp** implementación de interfaz, que se ajusta un objeto property desde el proveedor de host.</span><span class="sxs-lookup"><span data-stu-id="216b9-109">This code involves a property object, typically an **IMAPIProp** interface implementation, which wraps a property object from the host provider.</span></span> 
    
<span data-ttu-id="216b9-110">Actuar como un proveedor externo es una función opcional; No todos los proveedores deben admitir identificadores de plantilla y su código relacionado.</span><span class="sxs-lookup"><span data-stu-id="216b9-110">Acting as a foreign provider is an optional role; not all providers need to support template identifiers and their related code.</span></span> <span data-ttu-id="216b9-111">Implementar un proveedor como un proveedor externo si desea mantener el control sobre los destinatarios que los proveedores de host crean con plantillas suministradas por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="216b9-111">Implement your provider as a foreign provider if you want to maintain control over recipients that host providers create using templates supplied by your provider.</span></span> 
  
<span data-ttu-id="216b9-112">El formato que usa el proveedor para sus identificadores de entrada también puede usarse para sus identificadores de plantilla.</span><span class="sxs-lookup"><span data-stu-id="216b9-112">The format that your provider uses for its entry identifiers can also be used for its template identifiers.</span></span> <span data-ttu-id="216b9-113">Identificadores de plantilla deben incluir registrado de su proveedor **MAPIUID** para habilitar MAPI enlazar correctamente los destinatarios a los proveedores de adecuados.</span><span class="sxs-lookup"><span data-stu-id="216b9-113">Template identifiers must include your provider's registered **MAPIUID** to enable MAPI to successfully bind recipients to the appropriate providers.</span></span> 
  
<span data-ttu-id="216b9-114">MAPI llama a **IABLogon::OpenTemplateID** (método) su proveedor cuando un proveedor de host llama [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md).</span><span class="sxs-lookup"><span data-stu-id="216b9-114">MAPI calls your provider's **IABLogon::OpenTemplateID** method when a host provider calls [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md).</span></span> <span data-ttu-id="216b9-115">El proveedor de host pasa el identificador de plantilla del destinatario en el parámetro _lpTemplateID_ en su llamada a **IMAPISupport::OpenTemplateID**.</span><span class="sxs-lookup"><span data-stu-id="216b9-115">The host provider passes the template identifier of the recipient in the  _lpTemplateID_ parameter in its call to **IMAPISupport::OpenTemplateID**.</span></span> <span data-ttu-id="216b9-116">MAPI determina que el identificador de plantilla pertenece a su proveedor mediante la coincidencia de [MAPIUID](mapiuid.md) en el identificador de plantilla con el **MAPIUID** que su proveedor registrado en tiempo de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="216b9-116">MAPI determines that the template identifier belongs to your provider by matching the [MAPIUID](mapiuid.md) in the template identifier with the **MAPIUID** that your provider registered at logon time.</span></span> <span data-ttu-id="216b9-117">MAPI, a continuación, reenvía la llamada del proveedor de host a su proveedor de a través del método **IABLogon::OpenTemplateID** .</span><span class="sxs-lookup"><span data-stu-id="216b9-117">MAPI then forwards the host provider's call to your provider through the **IABLogon::OpenTemplateID** method.</span></span> 
  
<span data-ttu-id="216b9-118">El proveedor de host también pasa un puntero a su implementación de objeto de la propiedad para el destinatario en el parámetro _lpMAPIPropData_ , un identificador de interfaz en el parámetro _lpInterface_ que corresponde al tipo de implementación de la interfaz que se pasan en _lpMAPIPropData_y un indicador opcional, FILL_ENTRY.</span><span class="sxs-lookup"><span data-stu-id="216b9-118">The host provider also passes a pointer to its property object implementation for the recipient in the  _lpMAPIPropData_ parameter, an interface identifier in the  _lpInterface_ parameter that corresponds to the type of interface implementation passed in  _lpMAPIPropData_, and an optional flag, FILL_ENTRY.</span></span> <span data-ttu-id="216b9-119">Se espera que el proveedor para devolver en el parámetro _lppMAPIPropNew_ un puntero a una implementación de objeto de la propiedad del tipo especificado en _lpInterface_.</span><span class="sxs-lookup"><span data-stu-id="216b9-119">Your provider is expected to return in the  _lppMAPIPropNew_ parameter a pointer to a property object implementation of the type specified in  _lpInterface_.</span></span> <span data-ttu-id="216b9-120">El puntero devuelto puede ser al objeto ajustado (propiedad) implementada por el proveedor o para el objeto proporcionado por el proveedor de host en _lpMAPIPropData_.</span><span class="sxs-lookup"><span data-stu-id="216b9-120">The returned pointer can either be to the wrapped property object implemented by your provider or to the object supplied by the host provider in  _lpMAPIPropData_.</span></span> <span data-ttu-id="216b9-121">Su proveedor debe devolver un puntero de objeto de propiedad ajustado cuando:</span><span class="sxs-lookup"><span data-stu-id="216b9-121">Your provider should return a wrapped property object pointer when:</span></span>
  
- <span data-ttu-id="216b9-122">Tabla de presentación del destinatario contiene controles de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="216b9-122">The recipient's display table contains list box controls.</span></span>
    
- <span data-ttu-id="216b9-123">La dirección de correo electrónico para el destinatario debe montarse desde los datos en varios controles de tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="216b9-123">The email address for the recipient must be assembled from data in multiple display table controls.</span></span>
    
- <span data-ttu-id="216b9-124">Los problemas de proveedor Mostrar notificaciones de tabla.</span><span class="sxs-lookup"><span data-stu-id="216b9-124">Your provider issues display table notifications.</span></span>
    
<span data-ttu-id="216b9-125">El indicador FILL_ENTRY indica a su proveedor de que el proveedor de host requiere todas las propiedades del destinatario para actualizarse.</span><span class="sxs-lookup"><span data-stu-id="216b9-125">The FILL_ENTRY flag indicates to your provider that the host provider requires all the properties of the recipient to be updated.</span></span> <span data-ttu-id="216b9-126">Su proveedor es necesario para cumplir con esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="216b9-126">Your provider is required to fulfill this request.</span></span>
  
<span data-ttu-id="216b9-127">Cuando un proveedor de host llama al método **OpenTemplateID** de su proveedor, es posible que su proveedor:</span><span class="sxs-lookup"><span data-stu-id="216b9-127">When a host provider calls your provider's **OpenTemplateID** method, your provider might:</span></span> 
  
- <span data-ttu-id="216b9-128">Actualizar periódicamente los datos para una entrada de copiado.</span><span class="sxs-lookup"><span data-stu-id="216b9-128">Periodically update the data for a copied entry.</span></span>
    
- <span data-ttu-id="216b9-129">Mantener una entrada copiada sincronizada con su original, por ejemplo, cuando se copia una entrada de la libreta de direcciones a la libreta de direcciones personales.</span><span class="sxs-lookup"><span data-stu-id="216b9-129">Keep a copied entry synchronized with its original, such as when an address book entry is copied to the personal address book.</span></span>
    
- <span data-ttu-id="216b9-130">Implementar la funcionalidad que no se pueden implementar por el proveedor de host, como rellenar dinámicamente lista cuadros en la tabla de detalles de la entrada copiada desde los datos en un servidor.</span><span class="sxs-lookup"><span data-stu-id="216b9-130">Implement functionality that cannot be implemented by the host provider, such as dynamically populating list boxes in the copied entry's details table from data on a server.</span></span>
    
- <span data-ttu-id="216b9-131">Controlar la interacción entre las propiedades de una entrada copiada o ha creado una instancia de plantilla.</span><span class="sxs-lookup"><span data-stu-id="216b9-131">Control the interaction among properties in a copied entry or instantiated template.</span></span> <span data-ttu-id="216b9-132">Por ejemplo, los sistemas **PR_EMAIL_ADDRESS** de otras propiedades que se muestran en la tabla de detalles.</span><span class="sxs-lookup"><span data-stu-id="216b9-132">For example, computing **PR_EMAIL_ADDRESS** from other properties displayed in the details table.</span></span> 
    
<span data-ttu-id="216b9-133">Los dos primeros elementos son ejemplos de tareas que no requieren su proveedor suministrar un objeto property ajustado: una implementación de **IMAPIProp** que se basa en la implementación del proveedor de host.</span><span class="sxs-lookup"><span data-stu-id="216b9-133">The first two items are examples of tasks that do not require your provider to supply a wrapped property object — an implementation of **IMAPIProp** that is based on the host provider's implementation.</span></span> <span data-ttu-id="216b9-134">El proveedor simplemente puede actualizar las propiedades como devuelto y es necesario establecer el parámetro _lppMAPIPropNew_ para que apunte al puntero que se pasó por el proveedor de host en el parámetro _lpMAPIPropData_ .</span><span class="sxs-lookup"><span data-stu-id="216b9-134">Your provider can simply update the properties as necessary and return, setting the  _lppMAPIPropNew_ parameter to point to the pointer passed in by the host provider in the  _lpMAPIPropData_ parameter.</span></span> 
  
<span data-ttu-id="216b9-135">El segundo lugar dos tareas que requieren que el proveedor devuelva al proveedor de host un objeto de propiedad que se ajusta el objeto del proveedor de host con una funcionalidad adicional, como la capacidad para mostrar una hoja de propiedades para la entrada.</span><span class="sxs-lookup"><span data-stu-id="216b9-135">The second two tasks require that your provider return to the host provider a property object that wraps the host provider's object with additional functionality, such as the ability to display a property sheet for the entry.</span></span> <span data-ttu-id="216b9-136">Este objeto de la propiedad será una mensajería usuario o lista de distribución, según el tipo de objeto que se pasó por el proveedor de host en el parámetro _lpMAPIPropData_ e indicada por el identificador de interfaz en el parámetro _lpInterface_ .</span><span class="sxs-lookup"><span data-stu-id="216b9-136">This property object will either be a messaging user or distribution list, depending on the type of object passed in by the host provider in the  _lpMAPIPropData_ parameter and indicated by the interface identifier in the  _lpInterface_ parameter.</span></span> <span data-ttu-id="216b9-137">Si el parámetro _lpMAPIPropData_ señala a un usuario de mensajería, objeto ajustado (propiedad) de su proveedor debe ser una implementación de **IMailUser** .</span><span class="sxs-lookup"><span data-stu-id="216b9-137">If the  _lpMAPIPropData_ parameter points to a messaging user, your provider's wrapped property object must be an **IMailUser** implementation.</span></span> <span data-ttu-id="216b9-138">Si _lpMAPIPropData_ apunta a una lista de distribución, debe ser una implementación de **IDistList** .</span><span class="sxs-lookup"><span data-stu-id="216b9-138">If  _lpMAPIPropData_ points to a distribution list, it must be an **IDistList** implementation.</span></span> 
  
<span data-ttu-id="216b9-139">Objeto ajustado (propiedad) de su proveedor intercepta las llamadas al método **IMAPIProp** para llevar a cabo la manipulación de específicos del contexto del destinatario del proveedor de host, el objeto se ajuste.</span><span class="sxs-lookup"><span data-stu-id="216b9-139">Your provider's wrapped property object intercepts **IMAPIProp** method calls to perform context-specific manipulation of the host provider's recipient—the object it is wrapping.</span></span> <span data-ttu-id="216b9-140">MAPI sólo tiene un requisito para objetos property ajustado: todas las llamadas a [IMAPIProp::OpenProperty](imapiprop-openproperty.md) que solicita la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) se pasan al proveedor de host.</span><span class="sxs-lookup"><span data-stu-id="216b9-140">MAPI only has one requirement for wrapped property objects: all calls to [IMAPIProp::OpenProperty](imapiprop-openproperty.md) requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property should be passed to the host provider.</span></span> <span data-ttu-id="216b9-141">Implementación de su proveedor puede usar el objeto table devuelto para interceptar las notificaciones de tabla para mostrar o para agregar su propio si es necesario.</span><span class="sxs-lookup"><span data-stu-id="216b9-141">Your provider's implementation can use the returned table to intercept display table notifications or to add its own if necessary.</span></span> 
  
<span data-ttu-id="216b9-142">La siguiente lista incluye las tareas que normalmente se implementan en el objeto de propiedad ajustado implementado por proveedores externos:</span><span class="sxs-lookup"><span data-stu-id="216b9-142">The following list includes tasks that are typically implemented in the wrapped property object implemented by foreign providers:</span></span>
  
- <span data-ttu-id="216b9-143">Preprocesamiento y procesamiento posterior de los valores de propiedad para el destinatario de host en [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="216b9-143">Preprocessing and postprocessing property values for the host recipient in [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
- <span data-ttu-id="216b9-144">Detalles de tratamiento de mostrar los controles de la tabla, como botones y cuadros de lista, en **IMAPIProp::OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="216b9-144">Handling details display table controls, such as buttons and list boxes, in **IMAPIProp::OpenProperty**.</span></span>
    
- <span data-ttu-id="216b9-145">Validar o manipular los valores de propiedad para el destinatario de host en [IMAPIProp::SetProps](imapiprop-setprops.md).</span><span class="sxs-lookup"><span data-stu-id="216b9-145">Validating or manipulating property values for the host recipient in [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span>
    
- <span data-ttu-id="216b9-146">Los sistemas de propiedades necesarias como **PR_EMAIL_ADDRESS** y comprobar que todas las propiedades necesarias se han establecido antes de guardar al destinatario de host en [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="216b9-146">Computing required properties such as **PR_EMAIL_ADDRESS** and verifying that all of the necessary properties have been set before saving the host recipient in [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
### <a name="to-implement-iablogonopentemplateid"></a><span data-ttu-id="216b9-147">Para implementar IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="216b9-147">To implement IABLogon::OpenTemplateID</span></span>
  
1. <span data-ttu-id="216b9-148">Compruebe si el identificador de plantilla se pasa en con el parámetro _lpTemplateID_ es válido y se encuentra en un formato que el proveedor reconoce.</span><span class="sxs-lookup"><span data-stu-id="216b9-148">Check if the template identifier passed in with the  _lpTemplateID_ parameter is valid and is in a format that your provider recognizes.</span></span> <span data-ttu-id="216b9-149">Si no es así, se producirá un error y devolver MAPI_E_INVALID_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="216b9-149">If it is not, fail and return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="216b9-150">Crear un objeto del tipo indicado por el identificador de plantilla, un usuario de mensajería, una lista de distribución o un destinatario de uso único.</span><span class="sxs-lookup"><span data-stu-id="216b9-150">Create an object of the type indicated by the template identifier, either a messaging user, distribution list, or one-off recipient.</span></span> 
    
3. <span data-ttu-id="216b9-151">Llame al método **IUnknown:: AddRef** en el objeto de propiedad del proveedor de host, que es el objeto al que señala el parámetro _lpMAPIPropData_ .</span><span class="sxs-lookup"><span data-stu-id="216b9-151">Call the **IUnknown::AddRef** method in the host provider's property object, which is the object pointed to by the  _lpMAPIPropData_ parameter.</span></span> 
    
4. <span data-ttu-id="216b9-152">Si el parámetro _ulTemplateFlags_ se establece en FILL_ENTRY:</span><span class="sxs-lookup"><span data-stu-id="216b9-152">If the  _ulTemplateFlags_ parameter is set to FILL_ENTRY:</span></span> 
    
   1. <span data-ttu-id="216b9-153">Si el nuevo objeto es una lista de distribución o de usuario de mensajería:</span><span class="sxs-lookup"><span data-stu-id="216b9-153">If the new object is a messaging user or distribution list:</span></span>
      
      1. <span data-ttu-id="216b9-154">Recuperar todas las propiedades del nuevo objeto, posiblemente mediante una llamada a su método **IMAPIProp::GetProps** .</span><span class="sxs-lookup"><span data-stu-id="216b9-154">Retrieve all of the properties of the new object, possibly by calling its **IMAPIProp::GetProps** method.</span></span> 
          
      2. <span data-ttu-id="216b9-155">Llamar al método **IMAPIProp::SetProps** del proveedor de host para copiar todas las propiedades devueltas al objeto de la propiedad del proveedor de host.</span><span class="sxs-lookup"><span data-stu-id="216b9-155">Call the host provider's **IMAPIProp::SetProps** method to copy all of the retrieved properties to the host provider's property object.</span></span> 
      
   2. <span data-ttu-id="216b9-156">Si el nuevo objeto es un destinatario de uso único, llamar al método **IMAPIProp::SetProps** del proveedor de host para establecer las propiedades siguientes:</span><span class="sxs-lookup"><span data-stu-id="216b9-156">If the new object is a one-off recipient, call the host provider's **IMAPIProp::SetProps** method to set the following properties:</span></span> 
      
      - <span data-ttu-id="216b9-157">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) para el tipo de dirección controlado por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="216b9-157">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) to the address type handled by your provider.</span></span>
        
      - <span data-ttu-id="216b9-158">**Precio:\_identificador de plantilla** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) para el identificador de plantilla de los parámetros _lpTemplateID_ y _cbTemplateID_ .</span><span class="sxs-lookup"><span data-stu-id="216b9-158">**PR\_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) to the template identifier from the  _lpTemplateID_ and  _cbTemplateID_ parameters.</span></span> 
        
      - <span data-ttu-id="216b9-159">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) a DT_MAILUSER o DT_DISTLIST, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="216b9-159">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) to DT_MAILUSER or DT_DISTLIST, as appropriate.</span></span>
    
5. <span data-ttu-id="216b9-160">Establecer el contenido del parámetro _lppMAPIPropNew_ para que apunte al nuevo objeto de su proveedor o el objeto de la propiedad pasado con el parámetro _lpMAPIPropData_ , dependiendo de si su proveedor determina que es necesario un objeto ajustado.</span><span class="sxs-lookup"><span data-stu-id="216b9-160">Set the contents of the  _lppMAPIPropNew_ parameter to point to either your provider's new object or the property object passed in with the  _lpMAPIPropData_ parameter, depending on whether your provider determines a wrapped object is necessary.</span></span> 
    
6. <span data-ttu-id="216b9-161">Si se produce un error crítico, como un error de red o una condición de falta de memoria, devolver el valor de error apropiado.</span><span class="sxs-lookup"><span data-stu-id="216b9-161">If a critical error occurs, such as a network failure or an out of memory condition, return the appropriate error value.</span></span> <span data-ttu-id="216b9-162">Este valor debe obtener propaga al cliente con la estructura [MAPIERROR](mapierror.md) apropiado, una tarea realizada por el proveedor de host.</span><span class="sxs-lookup"><span data-stu-id="216b9-162">This value should get propagated to the client with the appropriate [MAPIERROR](mapierror.md) structure, a task performed by the host provider.</span></span> 
    
