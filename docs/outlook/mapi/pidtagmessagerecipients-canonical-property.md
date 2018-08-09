---
title: Propiedad canónica PidTagMessageRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipients
api_type:
- HeaderDef
ms.assetid: 7f8b0d96-99d6-4f1c-8ac4-4dbb83626382
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 980b1b81a0afbfe05fee915ddd730aad31811132
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819746"
---
# <a name="pidtagmessagerecipients-canonical-property"></a><span data-ttu-id="17b03-103">Propiedad canónica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="17b03-103">PidTagMessageRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="17b03-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="17b03-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="17b03-105">Contiene una tabla de las restricciones que se pueden aplicar a una tabla de contenido para buscar todos los mensajes que contienen destinatarios subobjetos que cumplen las restricciones.</span><span class="sxs-lookup"><span data-stu-id="17b03-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain recipient subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="17b03-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="17b03-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="17b03-107">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="17b03-107">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |
|<span data-ttu-id="17b03-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="17b03-108">Identifier:</span></span>  <br/> |<span data-ttu-id="17b03-109">0x0E12</span><span class="sxs-lookup"><span data-stu-id="17b03-109">0x0E12</span></span>  <br/> |
|<span data-ttu-id="17b03-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="17b03-110">Data type:</span></span>  <br/> |<span data-ttu-id="17b03-111">PT OBJECT</span><span class="sxs-lookup"><span data-stu-id="17b03-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="17b03-112">Área:</span><span class="sxs-lookup"><span data-stu-id="17b03-112">Area:</span></span>  <br/> |<span data-ttu-id="17b03-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="17b03-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17b03-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="17b03-114">Remarks</span></span>

<span data-ttu-id="17b03-115">Esta propiedad puede ser en las operaciones de [IMAPIProp::CopyTo](imapiprop-copyto.md) incluyen o excluyen de operaciones de [IMAPIProp::CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="17b03-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="17b03-116">Como una propiedad de tipo **pt Object**, no se correctamente puede recuperar mediante el método [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="17b03-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="17b03-117">El método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , que solicita el identificador de interfaz **IID_IMAPITable** debe tener acceso a su contenido.</span><span class="sxs-lookup"><span data-stu-id="17b03-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="17b03-118">Proveedores de servicios deben identificarlo al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) si se establece, pero es posible que, opcionalmente, identificarlo o no, si no está establecido.</span><span class="sxs-lookup"><span data-stu-id="17b03-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="17b03-119">Para recuperar el contenido de la tabla, una aplicación de cliente debe llamar al método de [IMessage::GetRecipientTable](imessage-getrecipienttable.md) .</span><span class="sxs-lookup"><span data-stu-id="17b03-119">To retrieve table contents, a client application should call the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> 
  
<span data-ttu-id="17b03-120">Esta propiedad se puede utilizar para la restricción de subobjetos mediante la especificación de la estructura de [SSubRestriction](ssubrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="17b03-120">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="17b03-121">Esto permite a un cliente limitar la vista de un contenedor para los mensajes con los destinatarios de la reunión criterios dados.</span><span class="sxs-lookup"><span data-stu-id="17b03-121">This enables a client to limit the view of a container to messages with recipients meeting given criteria.</span></span> <span data-ttu-id="17b03-122">Un mensaje se califica para ver si hay al menos una fila en su tabla de destinatarios, es decir, un destinatario satisface la restricción de subobjetos.</span><span class="sxs-lookup"><span data-stu-id="17b03-122">A message qualifies for viewing if at least one row in its recipient table, that is, one recipient satisfies the subobject restriction.</span></span> 
  
 <span data-ttu-id="17b03-123">**Nota** Uso de los resultados de restricción de subobjetos es el equivalente de un [IMAPISession::OpenEntry](imapisession-openentry.md) de llamadas en todos los mensajes en la tabla.</span><span class="sxs-lookup"><span data-stu-id="17b03-123">**Note** Using subobject restriction results is the equivalent of an [IMAPISession::OpenEntry](imapisession-openentry.md) call on every message in the table.</span></span> <span data-ttu-id="17b03-124">Dependiendo de la aplicación cliente y el número de mensajes que se desea buscar, puede afectar al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="17b03-124">Depending on the client application and the number of messages to be searched, it can affect performance.</span></span> 
  
<span data-ttu-id="17b03-125">La propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) y esta propiedad son similares en uso.</span><span class="sxs-lookup"><span data-stu-id="17b03-125">The **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property and this property are similar in usage.</span></span> <span data-ttu-id="17b03-126">Varias propiedades MAPI proporcionan acceso a las tablas:</span><span class="sxs-lookup"><span data-stu-id="17b03-126">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="17b03-127">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="17b03-127">**Property**</span></span>|<span data-ttu-id="17b03-128">**Table**</span><span class="sxs-lookup"><span data-stu-id="17b03-128">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="17b03-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="17b03-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="17b03-130">Tabla de contenido</span><span class="sxs-lookup"><span data-stu-id="17b03-130">Contents table</span></span>  <br/> |
|<span data-ttu-id="17b03-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="17b03-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="17b03-132">Tabla de jerarquía</span><span class="sxs-lookup"><span data-stu-id="17b03-132">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="17b03-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="17b03-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="17b03-134">Tabla de contenido asociada</span><span class="sxs-lookup"><span data-stu-id="17b03-134">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="17b03-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="17b03-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="17b03-136">Tabla de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="17b03-136">Attachment table</span></span>  <br/> |
|<span data-ttu-id="17b03-137">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="17b03-137">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |<span data-ttu-id="17b03-138">Tabla de destinatarios</span><span class="sxs-lookup"><span data-stu-id="17b03-138">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="17b03-139">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="17b03-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="17b03-140">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="17b03-140">Protocol specifications</span></span>

<span data-ttu-id="17b03-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17b03-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17b03-142">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="17b03-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="17b03-143">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17b03-143">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17b03-144">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="17b03-144">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="17b03-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17b03-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17b03-146">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="17b03-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="17b03-147">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17b03-147">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17b03-148">Permite la manipulación de las listas Permitir o bloquear y la determinación de los mensajes de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="17b03-148">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="17b03-149">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17b03-149">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17b03-150">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="17b03-150">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="17b03-151">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="17b03-151">Header files</span></span>

<span data-ttu-id="17b03-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="17b03-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="17b03-153">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="17b03-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="17b03-154">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="17b03-154">Mapitags.h</span></span>
  
> <span data-ttu-id="17b03-155">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="17b03-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="17b03-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="17b03-156">See also</span></span>



[<span data-ttu-id="17b03-157">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="17b03-157">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="17b03-158">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="17b03-158">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="17b03-159">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="17b03-159">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="17b03-160">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="17b03-160">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

