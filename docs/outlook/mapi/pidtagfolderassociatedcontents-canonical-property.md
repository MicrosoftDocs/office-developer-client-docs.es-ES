---
title: Propiedad canónica PidTagFolderAssociatedContents
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderAssociatedContents
api_type:
- HeaderDef
ms.assetid: d1f3f589-dc2d-4538-a13f-278dad29bcc7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c85c5d7c3e80508c4d328f69ac4ad15f0f2c355a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391065"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a><span data-ttu-id="4df01-103">Propiedad canónica PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="4df01-103">PidTagFolderAssociatedContents Canonical Property</span></span>

  
  
<span data-ttu-id="4df01-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4df01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4df01-105">Contiene un objeto de tabla de contenido incrustado que proporciona información acerca de la tabla de contenido asociada.</span><span class="sxs-lookup"><span data-stu-id="4df01-105">Contains an embedded contents table object that provides information about the associated contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4df01-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4df01-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4df01-107">PR_FOLDER_ASSOCIATED_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="4df01-107">PR_FOLDER_ASSOCIATED_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="4df01-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4df01-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4df01-109">0x3610</span><span class="sxs-lookup"><span data-stu-id="4df01-109">0x3610</span></span>  <br/> |
|<span data-ttu-id="4df01-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4df01-110">Data type:</span></span>  <br/> |<span data-ttu-id="4df01-111">PT OBJECT</span><span class="sxs-lookup"><span data-stu-id="4df01-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="4df01-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4df01-112">Area:</span></span>  <br/> |<span data-ttu-id="4df01-113">Contenedor MAPI</span><span class="sxs-lookup"><span data-stu-id="4df01-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4df01-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4df01-114">Remarks</span></span>

<span data-ttu-id="4df01-115">En la tabla de contenido asociada representa una subcarpeta que no aparecen en la tabla de contenido estándar.</span><span class="sxs-lookup"><span data-stu-id="4df01-115">The associated contents table represents a subfolder that does not appear in the standard contents table.</span></span> <span data-ttu-id="4df01-116">Contiene los mensajes asociado u ocultas, de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="4df01-116">It contains the folder's associated, or hidden, messages.</span></span> 
  
<span data-ttu-id="4df01-117">Esta propiedad puede ser en las operaciones de [IMAPIProp::CopyTo](imapiprop-copyto.md) incluyen o excluyen de operaciones de [IMAPIProp::CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="4df01-117">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="4df01-118">Como una propiedad de tipo **pt Object**, no se correctamente puede recuperar mediante el método [IMAPIProp::GetProps](imapiprop-getprops.md) ; el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , que solicita el identificador de interfaz **IID_IMAPITable** debe tener acceso a su contenido.</span><span class="sxs-lookup"><span data-stu-id="4df01-118">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="4df01-119">Proveedores de servicios deben identificarlo al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) si se establece, pero es posible que, opcionalmente, identificarlo o no, si no está establecido.</span><span class="sxs-lookup"><span data-stu-id="4df01-119">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="4df01-120">Para recuperar el contenido de la tabla, las aplicaciones cliente deben llamar al método de [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) .</span><span class="sxs-lookup"><span data-stu-id="4df01-120">To retrieve table contents, client applications should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="4df01-121">Para obtener más información sobre las tablas de contenido de carpeta, vea [Las tablas de contenido](contents-tables.md) y [Mostrar una tabla de contenido de carpeta](displaying-a-folder-contents-table.md).</span><span class="sxs-lookup"><span data-stu-id="4df01-121">For more information on folder contents tables, see [Contents Tables](contents-tables.md) and [Displaying a Folder Contents Table](displaying-a-folder-contents-table.md).</span></span> 
  
<span data-ttu-id="4df01-122">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) y esta propiedad son similares en uso.</span><span class="sxs-lookup"><span data-stu-id="4df01-122">The **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="4df01-123">Varias propiedades MAPI proporcionan acceso a las tablas:</span><span class="sxs-lookup"><span data-stu-id="4df01-123">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="4df01-124">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="4df01-124">**Property**</span></span>|<span data-ttu-id="4df01-125">**Table**</span><span class="sxs-lookup"><span data-stu-id="4df01-125">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4df01-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4df01-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4df01-127">Tabla de contenido</span><span class="sxs-lookup"><span data-stu-id="4df01-127">Contents table</span></span>  <br/> |
|<span data-ttu-id="4df01-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4df01-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4df01-129">Tabla de jerarquía</span><span class="sxs-lookup"><span data-stu-id="4df01-129">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="4df01-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="4df01-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span></span> <br/> |<span data-ttu-id="4df01-131">Tabla de contenido asociada</span><span class="sxs-lookup"><span data-stu-id="4df01-131">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="4df01-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4df01-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4df01-133">Tabla de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="4df01-133">Attachment table</span></span>  <br/> |
|<span data-ttu-id="4df01-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4df01-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4df01-135">Tabla de destinatarios</span><span class="sxs-lookup"><span data-stu-id="4df01-135">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4df01-136">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4df01-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4df01-137">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="4df01-137">Protocol specifications</span></span>

<span data-ttu-id="4df01-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4df01-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4df01-139">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="4df01-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4df01-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4df01-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4df01-141">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="4df01-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="4df01-142">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4df01-142">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4df01-143">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y elementos de reunión.</span><span class="sxs-lookup"><span data-stu-id="4df01-143">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4df01-144">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4df01-144">Header files</span></span>

<span data-ttu-id="4df01-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4df01-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="4df01-146">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4df01-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="4df01-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4df01-147">Mapitags.h</span></span>
  
> <span data-ttu-id="4df01-148">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="4df01-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4df01-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="4df01-149">See also</span></span>



[<span data-ttu-id="4df01-150">Propiedad canónica PidTagAssociatedContentCount</span><span class="sxs-lookup"><span data-stu-id="4df01-150">PidTagAssociatedContentCount Canonical Property</span></span>](pidtagassociatedcontentcount-canonical-property.md)


[<span data-ttu-id="4df01-151">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4df01-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4df01-152">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="4df01-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4df01-153">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4df01-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4df01-154">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="4df01-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

