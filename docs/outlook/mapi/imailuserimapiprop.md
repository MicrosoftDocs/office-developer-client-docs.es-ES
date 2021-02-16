---
title: IMailUser IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMailUser
api_type:
- COM
ms.assetid: 74c25870-62d9-484a-9a99-4dc35c52479e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a0e109fe95120483e700bab5b82f6d7cb75e2e28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436597"
---
# <a name="imailuser--imapiprop"></a><span data-ttu-id="82a32-103">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="82a32-103">IMailUser : IMAPIProp</span></span>

  
  
<span data-ttu-id="82a32-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82a32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82a32-105">Proporciona acceso a las muchas propiedades asociadas con los usuarios de mensajería.</span><span class="sxs-lookup"><span data-stu-id="82a32-105">Provides access to the many properties that are associated with messaging users.</span></span> <span data-ttu-id="82a32-106">La **interfaz IMailUser** se implementa mediante objetos de usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="82a32-106">The **IMailUser** interface is implemented by messaging user objects.</span></span> <span data-ttu-id="82a32-107">**IMailUser** hereda de la [interfaz IMAPIProp : IUnknown](imapipropiunknown.md) y no tiene métodos únicos propios.</span><span class="sxs-lookup"><span data-stu-id="82a32-107">**IMailUser** inherits from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and has no unique methods of its own.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="82a32-108">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="82a32-108">Header file:</span></span>  <br/> |<span data-ttu-id="82a32-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="82a32-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="82a32-110">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="82a32-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="82a32-111">Objetos de usuario de mensajería</span><span class="sxs-lookup"><span data-stu-id="82a32-111">Messaging user objects</span></span>  <br/> |
|<span data-ttu-id="82a32-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="82a32-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="82a32-113">Proveedores de libretas de direcciones</span><span class="sxs-lookup"><span data-stu-id="82a32-113">Address book providers</span></span>  <br/> |
|<span data-ttu-id="82a32-114">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="82a32-114">Called by:</span></span>  <br/> |<span data-ttu-id="82a32-115">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="82a32-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="82a32-116">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="82a32-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="82a32-117">IID_IMailUser</span><span class="sxs-lookup"><span data-stu-id="82a32-117">IID_IMailUser</span></span>  <br/> |
|<span data-ttu-id="82a32-118">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="82a32-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="82a32-119">LPMAILUSER</span><span class="sxs-lookup"><span data-stu-id="82a32-119">LPMAILUSER</span></span>  <br/> |
|<span data-ttu-id="82a32-120">Modelo de transacción:</span><span class="sxs-lookup"><span data-stu-id="82a32-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="82a32-121">Transacted</span><span class="sxs-lookup"><span data-stu-id="82a32-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="82a32-122">Orden de tabla virtual</span><span class="sxs-lookup"><span data-stu-id="82a32-122">Vtable order</span></span>

<span data-ttu-id="82a32-123">Esta interfaz no tiene ningún método único.</span><span class="sxs-lookup"><span data-stu-id="82a32-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="82a32-124">**Propiedades requeridas**</span><span class="sxs-lookup"><span data-stu-id="82a32-124">**Required properties**</span></span>|<span data-ttu-id="82a32-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="82a32-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="82a32-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a32-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="82a32-127">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="82a32-127">Read/write</span></span>  <br/> |
|<span data-ttu-id="82a32-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a32-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="82a32-129">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="82a32-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="82a32-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a32-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="82a32-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="82a32-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="82a32-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a32-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="82a32-133">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="82a32-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="82a32-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a32-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="82a32-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="82a32-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="82a32-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a32-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="82a32-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="82a32-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="82a32-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a32-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="82a32-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="82a32-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="82a32-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a32-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="82a32-141">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="82a32-141">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82a32-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="82a32-142">Remarks</span></span>

<span data-ttu-id="82a32-143">Cinco de las propiedades necesarias se conocen como propiedades de dirección base para los destinatarios:</span><span class="sxs-lookup"><span data-stu-id="82a32-143">Five of the required properties are known as the base address properties for recipients:</span></span>
  
- <span data-ttu-id="82a32-144">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="82a32-144">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="82a32-145">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="82a32-145">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="82a32-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="82a32-146">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="82a32-147">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="82a32-147">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="82a32-148">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="82a32-148">**PR_SEARCH_KEY**</span></span>
    
<span data-ttu-id="82a32-149">Estas propiedades se consideran especiales porque muchos otros grupos de propiedades similares se basan en este grupo base.</span><span class="sxs-lookup"><span data-stu-id="82a32-149">These properties are considered special because many other groups of similar properties are built upon this base group.</span></span> <span data-ttu-id="82a32-150">Los demás grupos se usan para describir un destinatario en varios roles, como el remitente original o delegado de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="82a32-150">The other groups are used to describe a recipient in various roles, such as a message's original or delegate sender.</span></span> <span data-ttu-id="82a32-151">Para obtener más información acerca de estas propiedades y cómo usarlas, vea [Tipos de direcciones MAPI](mapi-address-types.md).</span><span class="sxs-lookup"><span data-stu-id="82a32-151">For more information about these properties and how to use them, see [MAPI Address Types](mapi-address-types.md).</span></span>
  
<span data-ttu-id="82a32-152">Los usuarios de mensajería pueden mostrar una colección de sus propiedades si admiten **la PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="82a32-152">Messaging users can display a collection of their properties by supporting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="82a32-153">**PR_DETAILS_TABLE** es una tabla para mostrar que describe el diseño de un cuadro de diálogo de detalles o una página de propiedades con fichas que muestra la información de la propiedad del destinatario.</span><span class="sxs-lookup"><span data-stu-id="82a32-153">**PR_DETAILS_TABLE** is a display table that describes the layout of a details dialog box or a tabbed property page that displays recipient property information.</span></span> <span data-ttu-id="82a32-154">MAPI crea cuadros de diálogo de detalles cuando un cliente llama al [método IAddrBook::D etails.](iaddrbook-details.md)</span><span class="sxs-lookup"><span data-stu-id="82a32-154">MAPI creates details dialog boxes when a client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="82a32-155">Los objetos de usuario de mensajería pueden tener otras propiedades opcionales asociadas.</span><span class="sxs-lookup"><span data-stu-id="82a32-155">Messaging user objects can have other optional properties associated with them.</span></span> <span data-ttu-id="82a32-156">MAPI define muchas propiedades que proporcionan información de direccionamiento adicional sobre un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="82a32-156">MAPI defines many properties that provide additional addressing information about a messaging user.</span></span> <span data-ttu-id="82a32-157">Todas estas propiedades son cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="82a32-157">All of these properties are character strings.</span></span> <span data-ttu-id="82a32-158">En la siguiente lista se muestran las propiedades más usadas:</span><span class="sxs-lookup"><span data-stu-id="82a32-158">The following list shows the more commonly used properties:</span></span>
  
- <span data-ttu-id="82a32-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a32-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span> 
    
- <span data-ttu-id="82a32-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a32-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span></span> 
    
- <span data-ttu-id="82a32-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a32-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="82a32-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a32-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="82a32-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a32-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="82a32-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a32-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span></span> 
    
- <span data-ttu-id="82a32-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="82a32-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span></span> 
    
<span data-ttu-id="82a32-166">Para obtener una lista completa de propiedades, vea [Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md).</span><span class="sxs-lookup"><span data-stu-id="82a32-166">For a complete list of properties, see [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="82a32-167">Consulte también</span><span class="sxs-lookup"><span data-stu-id="82a32-167">See also</span></span>



[<span data-ttu-id="82a32-168">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="82a32-168">MAPI Interfaces</span></span>](mapi-interfaces.md)

