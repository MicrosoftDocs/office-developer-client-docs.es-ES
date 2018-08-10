---
title: Propiedad canónica PidTagContainerContents
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerContents
api_type:
- HeaderDef
ms.assetid: 66dbe65a-b9fd-41d5-946f-ec8888363043
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c2979a0825ad6c62dbbb7931255501e90d8450a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819347"
---
# <a name="pidtagcontainercontents-canonical-property"></a><span data-ttu-id="0066e-103">Propiedad canónica PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="0066e-103">PidTagContainerContents Canonical Property</span></span>

  
  
<span data-ttu-id="0066e-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0066e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0066e-105">Contiene un objeto de tabla de contenido incrustado que proporciona información sobre un contenedor.</span><span class="sxs-lookup"><span data-stu-id="0066e-105">Contains an embedded contents table object that provides information about a container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0066e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0066e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0066e-107">PR_CONTAINER_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="0066e-107">PR_CONTAINER_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="0066e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0066e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0066e-109">0x360F</span><span class="sxs-lookup"><span data-stu-id="0066e-109">0x360F</span></span>  <br/> |
|<span data-ttu-id="0066e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0066e-110">Data type:</span></span>  <br/> |<span data-ttu-id="0066e-111">PT OBJECT</span><span class="sxs-lookup"><span data-stu-id="0066e-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="0066e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0066e-112">Area:</span></span>  <br/> |<span data-ttu-id="0066e-113">Container</span><span class="sxs-lookup"><span data-stu-id="0066e-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0066e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0066e-114">Remarks</span></span>

<span data-ttu-id="0066e-115">Esta propiedad puede ser en las operaciones de [IMAPIProp::CopyTo](imapiprop-copyto.md) incluyen o excluyen de operaciones de [IMAPIProp::CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="0066e-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="0066e-116">Como una propiedad de tipo pt Object, no se correctamente puede recuperar mediante el método [IMAPIProp::GetProps](imapiprop-getprops.md) ; el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , que solicita el identificador de interfaz IID_IMAPITable debe tener acceso a su contenido.</span><span class="sxs-lookup"><span data-stu-id="0066e-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="0066e-117">Proveedores de servicios deben identificarlo al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) si está establecida, pero puede, opcionalmente, identificarlo o no, si no está establecido.</span><span class="sxs-lookup"><span data-stu-id="0066e-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="0066e-118">Para recuperar el contenido de la tabla, una aplicación de cliente debe llamar al método de [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) .</span><span class="sxs-lookup"><span data-stu-id="0066e-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="0066e-119">For more information, see [Tablas de contenido](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="0066e-119">For more information, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="0066e-120">Esta propiedad, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) y **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) son similares en uso.</span><span class="sxs-lookup"><span data-stu-id="0066e-120">This property, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) , and **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) are similar in usage.</span></span> <span data-ttu-id="0066e-121">Varias propiedades MAPI proporcionan acceso a las tablas:</span><span class="sxs-lookup"><span data-stu-id="0066e-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="0066e-122">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="0066e-122">**Property**</span></span>|<span data-ttu-id="0066e-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="0066e-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0066e-124">PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="0066e-124">PidTagContainerContents</span></span>  <br/> |<span data-ttu-id="0066e-125">Tabla de contenido</span><span class="sxs-lookup"><span data-stu-id="0066e-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="0066e-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0066e-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0066e-127">Tabla de jerarquía</span><span class="sxs-lookup"><span data-stu-id="0066e-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="0066e-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0066e-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0066e-129">Tabla de contenido asociada</span><span class="sxs-lookup"><span data-stu-id="0066e-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="0066e-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0066e-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0066e-131">Tabla de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="0066e-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="0066e-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0066e-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0066e-133">Tabla de destinatarios</span><span class="sxs-lookup"><span data-stu-id="0066e-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0066e-134">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0066e-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0066e-135">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0066e-135">Protocol specifications</span></span>

<span data-ttu-id="0066e-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0066e-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0066e-137">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0066e-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0066e-138">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0066e-138">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0066e-139">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="0066e-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0066e-140">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0066e-140">Header files</span></span>

<span data-ttu-id="0066e-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0066e-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="0066e-142">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0066e-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="0066e-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0066e-143">Mapitags.h</span></span>
  
> <span data-ttu-id="0066e-144">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0066e-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0066e-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="0066e-145">See also</span></span>



[<span data-ttu-id="0066e-146">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0066e-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0066e-147">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="0066e-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0066e-148">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0066e-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0066e-149">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="0066e-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
