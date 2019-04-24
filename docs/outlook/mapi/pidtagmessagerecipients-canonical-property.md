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
ms.openlocfilehash: d30088ba7398669228a18be825323afa800ec536
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355688"
---
# <a name="pidtagmessagerecipients-canonical-property"></a><span data-ttu-id="9ab5c-103">Propiedad canónica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="9ab5c-103">PidTagMessageRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="9ab5c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ab5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ab5c-105">Contiene una tabla de restricciones que se pueden aplicar a una tabla de contenido para buscar todos los mensajes que contienen subobjetos de destinatarios que cumplen con las restricciones.</span><span class="sxs-lookup"><span data-stu-id="9ab5c-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain recipient subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ab5c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9ab5c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ab5c-107">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="9ab5c-107">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |
|<span data-ttu-id="9ab5c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9ab5c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9ab5c-109">0x0E12</span><span class="sxs-lookup"><span data-stu-id="9ab5c-109">0x0E12</span></span>  <br/> |
|<span data-ttu-id="9ab5c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9ab5c-110">Data type:</span></span>  <br/> |<span data-ttu-id="9ab5c-111">PT OBJECT</span><span class="sxs-lookup"><span data-stu-id="9ab5c-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="9ab5c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9ab5c-112">Area:</span></span>  <br/> |<span data-ttu-id="9ab5c-113">Mensajes generales</span><span class="sxs-lookup"><span data-stu-id="9ab5c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ab5c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9ab5c-114">Remarks</span></span>

<span data-ttu-id="9ab5c-115">Esta propiedad se puede excluir en las operaciones de [IMAPIProp:: CopyTo](imapiprop-copyto.md) o incluirse en las operaciones de [IMAPIProp:: CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="9ab5c-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="9ab5c-116">Como una propiedad de tipo **PT Object**, el método [IMAPIProp:: GetProps](imapiprop-getprops.md) no puede recuperarlo correctamente.</span><span class="sxs-lookup"><span data-stu-id="9ab5c-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="9ab5c-117">Debe obtener acceso a su contenido mediante el método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , lo que solicita el identificador de interfaz **IID_IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="9ab5c-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="9ab5c-118">Los proveedores de servicios deben informar al método [IMAPIProp:: GetPropList](imapiprop-getproplist.md) si está establecido, pero, opcionalmente, puede informar de él o no si no se ha establecido.</span><span class="sxs-lookup"><span data-stu-id="9ab5c-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="9ab5c-119">Para recuperar el contenido de la tabla, una aplicación cliente debe llamar al método [IMessage:: GetRecipientTable](imessage-getrecipienttable.md) .</span><span class="sxs-lookup"><span data-stu-id="9ab5c-119">To retrieve table contents, a client application should call the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> 
  
<span data-ttu-id="9ab5c-120">Esta propiedad se puede usar para la restricción de subobjeto al especificarla en la estructura [SSubRestriction](ssubrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="9ab5c-120">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="9ab5c-121">Esto permite a un cliente limitar la vista de un contenedor a los mensajes con los destinatarios que cumplen los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="9ab5c-121">This enables a client to limit the view of a container to messages with recipients meeting given criteria.</span></span> <span data-ttu-id="9ab5c-122">Un mensaje es apto para ver si al menos una fila de su tabla de destinatarios, es decir, un destinatario satisface la restricción de subobjeto.</span><span class="sxs-lookup"><span data-stu-id="9ab5c-122">A message qualifies for viewing if at least one row in its recipient table, that is, one recipient satisfies the subobject restriction.</span></span> 
  
 <span data-ttu-id="9ab5c-123">**Nota:** El uso de resultados de restricción de subobjeto es el equivalente de una llamada de [IMAPISession:: OpenEntry](imapisession-openentry.md) en todos los mensajes de la tabla.</span><span class="sxs-lookup"><span data-stu-id="9ab5c-123">**Note** Using subobject restriction results is the equivalent of an [IMAPISession::OpenEntry](imapisession-openentry.md) call on every message in the table.</span></span> <span data-ttu-id="9ab5c-124">Según la aplicación cliente y el número de mensajes que se va a buscar, puede afectar al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="9ab5c-124">Depending on the client application and the number of messages to be searched, it can affect performance.</span></span> 
  
<span data-ttu-id="9ab5c-125">La propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) y esta propiedad son de uso similar.</span><span class="sxs-lookup"><span data-stu-id="9ab5c-125">The **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property and this property are similar in usage.</span></span> <span data-ttu-id="9ab5c-126">Varias propiedades MAPI proporcionan acceso a las tablas:</span><span class="sxs-lookup"><span data-stu-id="9ab5c-126">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="9ab5c-127">**Property**</span><span class="sxs-lookup"><span data-stu-id="9ab5c-127">**Property**</span></span>|<span data-ttu-id="9ab5c-128">**Table**</span><span class="sxs-lookup"><span data-stu-id="9ab5c-128">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9ab5c-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ab5c-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9ab5c-130">Tabla contenido</span><span class="sxs-lookup"><span data-stu-id="9ab5c-130">Contents table</span></span>  <br/> |
|<span data-ttu-id="9ab5c-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ab5c-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9ab5c-132">Tabla de jerarquía</span><span class="sxs-lookup"><span data-stu-id="9ab5c-132">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="9ab5c-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ab5c-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9ab5c-134">Tabla de contenido asociada</span><span class="sxs-lookup"><span data-stu-id="9ab5c-134">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="9ab5c-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ab5c-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9ab5c-136">Tabla de datos adJuntos</span><span class="sxs-lookup"><span data-stu-id="9ab5c-136">Attachment table</span></span>  <br/> |
|<span data-ttu-id="9ab5c-137">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="9ab5c-137">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |<span data-ttu-id="9ab5c-138">Tabla de destinatarios</span><span class="sxs-lookup"><span data-stu-id="9ab5c-138">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="9ab5c-139">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ab5c-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9ab5c-140">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="9ab5c-140">Protocol specifications</span></span>

<span data-ttu-id="9ab5c-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ab5c-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ab5c-142">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9ab5c-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9ab5c-143">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ab5c-143">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ab5c-144">Controla el orden y el flujo de transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="9ab5c-144">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="9ab5c-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ab5c-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ab5c-146">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="9ab5c-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="9ab5c-147">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ab5c-147">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ab5c-148">Habilita el control de las listas de permitidos y bloqueados y la determinación de los mensajes de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="9ab5c-148">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="9ab5c-149">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ab5c-149">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ab5c-150">Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="9ab5c-150">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9ab5c-151">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9ab5c-151">Header files</span></span>

<span data-ttu-id="9ab5c-152">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9ab5c-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ab5c-153">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9ab5c-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="9ab5c-154">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="9ab5c-154">Mapitags.h</span></span>
  
> <span data-ttu-id="9ab5c-155">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="9ab5c-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ab5c-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ab5c-156">See also</span></span>



[<span data-ttu-id="9ab5c-157">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9ab5c-157">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ab5c-158">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="9ab5c-158">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ab5c-159">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9ab5c-159">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ab5c-160">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="9ab5c-160">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

