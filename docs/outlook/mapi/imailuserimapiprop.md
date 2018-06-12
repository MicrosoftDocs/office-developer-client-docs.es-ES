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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 0c70d16d294426d30f3ac5f00b6bc46992386a86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817201"
---
# <a name="imailuser--imapiprop"></a><span data-ttu-id="39f4f-103">IMailUser: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="39f4f-103">IMailUser : IMAPIProp</span></span>

  
  
<span data-ttu-id="39f4f-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="39f4f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="39f4f-105">Proporciona acceso a las muchas propiedades que se asocian con los usuarios de mensajería.</span><span class="sxs-lookup"><span data-stu-id="39f4f-105">Provides access to the many properties that are associated with messaging users.</span></span> <span data-ttu-id="39f4f-106">La interfaz de **IMailUser** se implementa mediante objetos de usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="39f4f-106">The **IMailUser** interface is implemented by messaging user objects.</span></span> <span data-ttu-id="39f4f-107">**IMailUser** hereda de la [IMAPIProp: IUnknown](imapipropiunknown.md) de la interfaz y no tiene ningún método único de su propio.</span><span class="sxs-lookup"><span data-stu-id="39f4f-107">**IMailUser** inherits from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and has no unique methods of its own.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39f4f-108">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="39f4f-108">Header file:</span></span>  <br/> |<span data-ttu-id="39f4f-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="39f4f-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="39f4f-110">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="39f4f-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="39f4f-111">Objetos de usuario de mensajería</span><span class="sxs-lookup"><span data-stu-id="39f4f-111">Messaging user objects</span></span>  <br/> |
|<span data-ttu-id="39f4f-112">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="39f4f-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="39f4f-113">Proveedores de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="39f4f-113">Address book providers</span></span>  <br/> |
|<span data-ttu-id="39f4f-114">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="39f4f-114">Called by:</span></span>  <br/> |<span data-ttu-id="39f4f-115">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="39f4f-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="39f4f-116">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="39f4f-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="39f4f-117">IID_IMailUser</span><span class="sxs-lookup"><span data-stu-id="39f4f-117">IID_IMailUser</span></span>  <br/> |
|<span data-ttu-id="39f4f-118">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="39f4f-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="39f4f-119">LPMAILUSER</span><span class="sxs-lookup"><span data-stu-id="39f4f-119">LPMAILUSER</span></span>  <br/> |
|<span data-ttu-id="39f4f-120">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="39f4f-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="39f4f-121">Negocian</span><span class="sxs-lookup"><span data-stu-id="39f4f-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="39f4f-122">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="39f4f-122">Vtable order</span></span>

<span data-ttu-id="39f4f-123">Esta interfaz no tiene ningún método único.</span><span class="sxs-lookup"><span data-stu-id="39f4f-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="39f4f-124">**Propiedades necesarias**</span><span class="sxs-lookup"><span data-stu-id="39f4f-124">**Required properties**</span></span>|<span data-ttu-id="39f4f-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="39f4f-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="39f4f-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39f4f-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="39f4f-127">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="39f4f-127">Read/write</span></span>  <br/> |
|<span data-ttu-id="39f4f-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39f4f-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="39f4f-129">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="39f4f-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="39f4f-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39f4f-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="39f4f-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="39f4f-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="39f4f-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39f4f-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="39f4f-133">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="39f4f-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="39f4f-134">**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39f4f-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="39f4f-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="39f4f-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="39f4f-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39f4f-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="39f4f-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="39f4f-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="39f4f-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39f4f-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="39f4f-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="39f4f-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="39f4f-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39f4f-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="39f4f-141">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="39f4f-141">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39f4f-142">Notas</span><span class="sxs-lookup"><span data-stu-id="39f4f-142">Remarks</span></span>

<span data-ttu-id="39f4f-143">Cinco de las propiedades necesarias se conocen como las propiedades de la dirección base para los destinatarios:</span><span class="sxs-lookup"><span data-stu-id="39f4f-143">Five of the required properties are known as the base address properties for recipients:</span></span>
  
- <span data-ttu-id="39f4f-144">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="39f4f-144">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="39f4f-145">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="39f4f-145">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="39f4f-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="39f4f-146">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="39f4f-147">**ENTRADA DEL OBJETO**</span><span class="sxs-lookup"><span data-stu-id="39f4f-147">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="39f4f-148">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="39f4f-148">**PR_SEARCH_KEY**</span></span>
    
<span data-ttu-id="39f4f-149">Estas propiedades se consideran especiales debido a que muchos otros grupos de propiedades similares se basan en este grupo de base.</span><span class="sxs-lookup"><span data-stu-id="39f4f-149">These properties are considered special because many other groups of similar properties are built upon this base group.</span></span> <span data-ttu-id="39f4f-150">Los otros grupos se utilizan para describir a un destinatario en diversas funciones, como un mensaje s original o delegación el remitente.</span><span class="sxs-lookup"><span data-stu-id="39f4f-150">The other groups are used to describe a recipient in various roles, such as a message's original or delegate sender.</span></span> <span data-ttu-id="39f4f-151">Para obtener más información acerca de estas propiedades y cómo usarlos, vea [Tipos de direcciones de MAPI](mapi-address-types.md).</span><span class="sxs-lookup"><span data-stu-id="39f4f-151">For more information about these properties and how to use them, see [MAPI Address Types](mapi-address-types.md).</span></span>
  
<span data-ttu-id="39f4f-152">Los usuarios de mensajería puede mostrar una colección de sus propiedades al ser compatible con la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="39f4f-152">Messaging users can display a collection of their properties by supporting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="39f4f-153">**PR_DETAILS_TABLE** es una tabla para mostrar que describe el diseño de un cuadro de diálogo detalles o una página de propiedades con fichas que muestra información de propiedades de los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="39f4f-153">**PR_DETAILS_TABLE** is a display table that describes the layout of a details dialog box or a tabbed property page that displays recipient property information.</span></span> <span data-ttu-id="39f4f-154">MAPI crea cuadros de diálogo de detalles cuando un cliente llama al método [IAddrBook::Details](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="39f4f-154">MAPI creates details dialog boxes when a client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="39f4f-155">Objetos de usuario de mensajería pueden tener otras propiedades opcionales asociadas a ellos.</span><span class="sxs-lookup"><span data-stu-id="39f4f-155">Messaging user objects can have other optional properties associated with them.</span></span> <span data-ttu-id="39f4f-156">MAPI define muchas propiedades que proporcionan información de direccionamiento adicional acerca de un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="39f4f-156">MAPI defines many properties that provide additional addressing information about a messaging user.</span></span> <span data-ttu-id="39f4f-157">Todas estas propiedades son cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="39f4f-157">All of these properties are character strings.</span></span> <span data-ttu-id="39f4f-158">La siguiente lista se muestran más usan con frecuencia las propiedades:</span><span class="sxs-lookup"><span data-stu-id="39f4f-158">The following list shows the more commonly used properties:</span></span>
  
- <span data-ttu-id="39f4f-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39f4f-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span> 
    
- <span data-ttu-id="39f4f-160">**PR_ASSISTANT** ([Pidtagassistant de MAPI](pidtagassistant-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39f4f-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span></span> 
    
- <span data-ttu-id="39f4f-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39f4f-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="39f4f-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39f4f-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="39f4f-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39f4f-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="39f4f-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39f4f-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span></span> 
    
- <span data-ttu-id="39f4f-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39f4f-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span></span> 
    
<span data-ttu-id="39f4f-166">Para obtener una lista completa de propiedades, vea [Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md).</span><span class="sxs-lookup"><span data-stu-id="39f4f-166">For a complete list of properties, see [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="39f4f-167">Ver también</span><span class="sxs-lookup"><span data-stu-id="39f4f-167">See also</span></span>



[<span data-ttu-id="39f4f-168">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="39f4f-168">MAPI Interfaces</span></span>](mapi-interfaces.md)

