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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316306"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a><span data-ttu-id="63ac4-103">Propiedad canónica PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="63ac4-103">PidTagFolderAssociatedContents Canonical Property</span></span>

  
  
<span data-ttu-id="63ac4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63ac4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63ac4-105">Contiene un objeto de tabla de contenido incrustado que proporciona información acerca de la tabla de contenido asociada.</span><span class="sxs-lookup"><span data-stu-id="63ac4-105">Contains an embedded contents table object that provides information about the associated contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="63ac4-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="63ac4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="63ac4-107">PR_FOLDER_ASSOCIATED_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="63ac4-107">PR_FOLDER_ASSOCIATED_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="63ac4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="63ac4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="63ac4-109">0x3610</span><span class="sxs-lookup"><span data-stu-id="63ac4-109">0x3610</span></span>  <br/> |
|<span data-ttu-id="63ac4-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="63ac4-110">Data type:</span></span>  <br/> |<span data-ttu-id="63ac4-111">PT OBJECT</span><span class="sxs-lookup"><span data-stu-id="63ac4-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="63ac4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="63ac4-112">Area:</span></span>  <br/> |<span data-ttu-id="63ac4-113">Contenedor de MAPI</span><span class="sxs-lookup"><span data-stu-id="63ac4-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63ac4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="63ac4-114">Remarks</span></span>

<span data-ttu-id="63ac4-115">La tabla contenido asociado representa una subcarpeta que no aparece en la tabla contenido estándar.</span><span class="sxs-lookup"><span data-stu-id="63ac4-115">The associated contents table represents a subfolder that does not appear in the standard contents table.</span></span> <span data-ttu-id="63ac4-116">Contiene los mensajes de la carpeta asociados u ocultos.</span><span class="sxs-lookup"><span data-stu-id="63ac4-116">It contains the folder's associated, or hidden, messages.</span></span> 
  
<span data-ttu-id="63ac4-117">Esta propiedad se puede excluir en las operaciones de [IMAPIProp:: CopyTo](imapiprop-copyto.md) o incluirse en las operaciones de [IMAPIProp:: CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="63ac4-117">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="63ac4-118">Como una propiedad de tipo **PT Object**, el método [IMAPIProp:: GetProps](imapiprop-getprops.md) no puede recuperarlo correctamente; debe obtener acceso a su contenido mediante el método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , lo que solicita el identificador de interfaz **IID_IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="63ac4-118">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="63ac4-119">Los proveedores de servicios deben informar al método [IMAPIProp:: GetPropList](imapiprop-getproplist.md) si está establecido, pero, opcionalmente, puede informar de él o no si no se ha establecido.</span><span class="sxs-lookup"><span data-stu-id="63ac4-119">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="63ac4-120">Para recuperar el contenido de la tabla, las aplicaciones cliente deben llamar al método [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md) .</span><span class="sxs-lookup"><span data-stu-id="63ac4-120">To retrieve table contents, client applications should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="63ac4-121">Para obtener más información sobre las tablas de contenido de carpetas, consulte [tablas de contenido](contents-tables.md) y [Mostrar una tabla de contenido de carpetas](displaying-a-folder-contents-table.md).</span><span class="sxs-lookup"><span data-stu-id="63ac4-121">For more information on folder contents tables, see [Contents Tables](contents-tables.md) and [Displaying a Folder Contents Table](displaying-a-folder-contents-table.md).</span></span> 
  
<span data-ttu-id="63ac4-122">El **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) y esta propiedad son similares en uso.</span><span class="sxs-lookup"><span data-stu-id="63ac4-122">The **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="63ac4-123">Varias propiedades MAPI proporcionan acceso a las tablas:</span><span class="sxs-lookup"><span data-stu-id="63ac4-123">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="63ac4-124">**Property**</span><span class="sxs-lookup"><span data-stu-id="63ac4-124">**Property**</span></span>|<span data-ttu-id="63ac4-125">**Table**</span><span class="sxs-lookup"><span data-stu-id="63ac4-125">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="63ac4-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="63ac4-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="63ac4-127">Tabla contenido</span><span class="sxs-lookup"><span data-stu-id="63ac4-127">Contents table</span></span>  <br/> |
|<span data-ttu-id="63ac4-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="63ac4-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="63ac4-129">Tabla de jerarquía</span><span class="sxs-lookup"><span data-stu-id="63ac4-129">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="63ac4-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="63ac4-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span></span> <br/> |<span data-ttu-id="63ac4-131">Tabla de contenido asociada</span><span class="sxs-lookup"><span data-stu-id="63ac4-131">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="63ac4-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="63ac4-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="63ac4-133">Tabla de datos adJuntos</span><span class="sxs-lookup"><span data-stu-id="63ac4-133">Attachment table</span></span>  <br/> |
|<span data-ttu-id="63ac4-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="63ac4-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="63ac4-135">Tabla de destinatarios</span><span class="sxs-lookup"><span data-stu-id="63ac4-135">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="63ac4-136">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="63ac4-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="63ac4-137">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="63ac4-137">Protocol specifications</span></span>

<span data-ttu-id="63ac4-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63ac4-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63ac4-139">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="63ac4-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="63ac4-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63ac4-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63ac4-141">Controla el orden y el flujo de transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="63ac4-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="63ac4-142">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63ac4-142">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63ac4-143">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y elementos de citas y reuniones.</span><span class="sxs-lookup"><span data-stu-id="63ac4-143">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="63ac4-144">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="63ac4-144">Header files</span></span>

<span data-ttu-id="63ac4-145">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="63ac4-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="63ac4-146">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="63ac4-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="63ac4-147">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="63ac4-147">Mapitags.h</span></span>
  
> <span data-ttu-id="63ac4-148">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="63ac4-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63ac4-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="63ac4-149">See also</span></span>



[<span data-ttu-id="63ac4-150">Propiedad canónica PidTagAssociatedContentCount</span><span class="sxs-lookup"><span data-stu-id="63ac4-150">PidTagAssociatedContentCount Canonical Property</span></span>](pidtagassociatedcontentcount-canonical-property.md)


[<span data-ttu-id="63ac4-151">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="63ac4-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="63ac4-152">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="63ac4-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="63ac4-153">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="63ac4-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="63ac4-154">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="63ac4-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

