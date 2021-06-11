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
ms.openlocfilehash: 5f0717c2a6def6f99f1e53217764e8820125b79d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283131"
---
# <a name="pidtagcontainercontents-canonical-property"></a><span data-ttu-id="5cbad-103">Propiedad canónica PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="5cbad-103">PidTagContainerContents Canonical Property</span></span>

  
  
<span data-ttu-id="5cbad-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5cbad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5cbad-105">Contiene un objeto de tabla de contenido incrustado que proporciona información sobre un contenedor.</span><span class="sxs-lookup"><span data-stu-id="5cbad-105">Contains an embedded contents table object that provides information about a container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5cbad-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5cbad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5cbad-107">PR_CONTAINER_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="5cbad-107">PR_CONTAINER_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="5cbad-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5cbad-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5cbad-109">0x360F</span><span class="sxs-lookup"><span data-stu-id="5cbad-109">0x360F</span></span>  <br/> |
|<span data-ttu-id="5cbad-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5cbad-110">Data type:</span></span>  <br/> |<span data-ttu-id="5cbad-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="5cbad-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="5cbad-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5cbad-112">Area:</span></span>  <br/> |<span data-ttu-id="5cbad-113">Container</span><span class="sxs-lookup"><span data-stu-id="5cbad-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5cbad-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5cbad-114">Remarks</span></span>

<span data-ttu-id="5cbad-115">Esta propiedad puede excluirse en operaciones [IMAPIProp::CopyTo](imapiprop-copyto.md) o incluirse en [operaciones IMAPIProp::CopyProps.](imapiprop-copyprops.md)</span><span class="sxs-lookup"><span data-stu-id="5cbad-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="5cbad-116">Como una propiedad de tipo PT_OBJECT, el método [IMAPIProp::GetProps](imapiprop-getprops.md) no puede recuperarla correctamente; el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) debe tener acceso a su contenido, solicitando el IID_IMAPITable de interfaz.</span><span class="sxs-lookup"><span data-stu-id="5cbad-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="5cbad-117">Los proveedores de servicios deben notificarlo al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) si está establecido, pero opcionalmente pueden notificarlo o no si no está establecido.</span><span class="sxs-lookup"><span data-stu-id="5cbad-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="5cbad-118">Para recuperar el contenido de la tabla, una aplicación cliente debe llamar al [método IMAPIContainer::GetContentsTable.](imapicontainer-getcontentstable.md)</span><span class="sxs-lookup"><span data-stu-id="5cbad-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="5cbad-119">For more information, see [Tablas de contenido](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="5cbad-119">For more information, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="5cbad-120">Esta propiedad, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) y **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) son similares en el uso.</span><span class="sxs-lookup"><span data-stu-id="5cbad-120">This property, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) , and **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) are similar in usage.</span></span> <span data-ttu-id="5cbad-121">Varias propiedades MAPI proporcionan acceso a tablas:</span><span class="sxs-lookup"><span data-stu-id="5cbad-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="5cbad-122">**Property**</span><span class="sxs-lookup"><span data-stu-id="5cbad-122">**Property**</span></span>|<span data-ttu-id="5cbad-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="5cbad-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5cbad-124">PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="5cbad-124">PidTagContainerContents</span></span>  <br/> |<span data-ttu-id="5cbad-125">Tabla contenido</span><span class="sxs-lookup"><span data-stu-id="5cbad-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="5cbad-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5cbad-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5cbad-127">Tabla jerarquía</span><span class="sxs-lookup"><span data-stu-id="5cbad-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="5cbad-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5cbad-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5cbad-129">Tabla de contenido asociada</span><span class="sxs-lookup"><span data-stu-id="5cbad-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="5cbad-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5cbad-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5cbad-131">Tabla de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="5cbad-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="5cbad-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5cbad-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5cbad-133">Tabla de destinatarios</span><span class="sxs-lookup"><span data-stu-id="5cbad-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5cbad-134">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5cbad-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5cbad-135">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="5cbad-135">Protocol specifications</span></span>

<span data-ttu-id="5cbad-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5cbad-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5cbad-137">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="5cbad-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5cbad-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5cbad-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5cbad-139">Especifica las propiedades y las operaciones de listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="5cbad-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5cbad-140">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5cbad-140">Header files</span></span>

<span data-ttu-id="5cbad-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5cbad-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="5cbad-142">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5cbad-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="5cbad-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5cbad-143">Mapitags.h</span></span>
  
> <span data-ttu-id="5cbad-144">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="5cbad-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5cbad-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="5cbad-145">See also</span></span>



[<span data-ttu-id="5cbad-146">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5cbad-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5cbad-147">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="5cbad-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5cbad-148">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5cbad-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5cbad-149">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="5cbad-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

