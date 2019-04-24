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
# <a name="pidtagcontainercontents-canonical-property"></a><span data-ttu-id="7ac8a-103">Propiedad canónica PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="7ac8a-103">PidTagContainerContents Canonical Property</span></span>

  
  
<span data-ttu-id="7ac8a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ac8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ac8a-105">Contiene un objeto de tabla de contenido incrustado que proporciona información acerca de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="7ac8a-105">Contains an embedded contents table object that provides information about a container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7ac8a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7ac8a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7ac8a-107">PR_CONTAINER_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="7ac8a-107">PR_CONTAINER_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="7ac8a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7ac8a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7ac8a-109">0x360F</span><span class="sxs-lookup"><span data-stu-id="7ac8a-109">0x360F</span></span>  <br/> |
|<span data-ttu-id="7ac8a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7ac8a-110">Data type:</span></span>  <br/> |<span data-ttu-id="7ac8a-111">PT OBJECT</span><span class="sxs-lookup"><span data-stu-id="7ac8a-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="7ac8a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7ac8a-112">Area:</span></span>  <br/> |<span data-ttu-id="7ac8a-113">Container</span><span class="sxs-lookup"><span data-stu-id="7ac8a-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ac8a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7ac8a-114">Remarks</span></span>

<span data-ttu-id="7ac8a-115">Esta propiedad se puede excluir en las operaciones de [IMAPIProp:: CopyTo](imapiprop-copyto.md) o incluirse en las operaciones de [IMAPIProp:: CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="7ac8a-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="7ac8a-116">Como una propiedad de tipo PT Object, el método [IMAPIProp:: GetProps](imapiprop-getprops.md) no puede recuperarlo correctamente; debe obtener acceso a su contenido mediante el método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , lo que solicita el identificador de interfaz IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="7ac8a-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="7ac8a-117">Los proveedores de servicios deben informar al método [IMAPIProp:: GetPropList](imapiprop-getproplist.md) si está establecido, pero, opcionalmente, puede informar de él o no si no se ha establecido.</span><span class="sxs-lookup"><span data-stu-id="7ac8a-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="7ac8a-118">Para recuperar el contenido de la tabla, una aplicación cliente debe llamar al método [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md) .</span><span class="sxs-lookup"><span data-stu-id="7ac8a-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="7ac8a-119">For more information, see [Tablas de contenido](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="7ac8a-119">For more information, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="7ac8a-120">Esta propiedad, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) y **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) son similares en cuanto a uso.</span><span class="sxs-lookup"><span data-stu-id="7ac8a-120">This property, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) , and **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) are similar in usage.</span></span> <span data-ttu-id="7ac8a-121">Varias propiedades MAPI proporcionan acceso a las tablas:</span><span class="sxs-lookup"><span data-stu-id="7ac8a-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="7ac8a-122">**Property**</span><span class="sxs-lookup"><span data-stu-id="7ac8a-122">**Property**</span></span>|<span data-ttu-id="7ac8a-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="7ac8a-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7ac8a-124">PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="7ac8a-124">PidTagContainerContents</span></span>  <br/> |<span data-ttu-id="7ac8a-125">Tabla contenido</span><span class="sxs-lookup"><span data-stu-id="7ac8a-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="7ac8a-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7ac8a-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7ac8a-127">Tabla de jerarquía</span><span class="sxs-lookup"><span data-stu-id="7ac8a-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="7ac8a-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7ac8a-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7ac8a-129">Tabla de contenido asociada</span><span class="sxs-lookup"><span data-stu-id="7ac8a-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="7ac8a-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7ac8a-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7ac8a-131">Tabla de datos adJuntos</span><span class="sxs-lookup"><span data-stu-id="7ac8a-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="7ac8a-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7ac8a-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7ac8a-133">Tabla de destinatarios</span><span class="sxs-lookup"><span data-stu-id="7ac8a-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7ac8a-134">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ac8a-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7ac8a-135">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="7ac8a-135">Protocol specifications</span></span>

<span data-ttu-id="7ac8a-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7ac8a-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7ac8a-137">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7ac8a-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7ac8a-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7ac8a-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7ac8a-139">Especifica las propiedades y operaciones de las listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="7ac8a-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7ac8a-140">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7ac8a-140">Header files</span></span>

<span data-ttu-id="7ac8a-141">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7ac8a-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="7ac8a-142">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7ac8a-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="7ac8a-143">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7ac8a-143">Mapitags.h</span></span>
  
> <span data-ttu-id="7ac8a-144">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="7ac8a-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7ac8a-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ac8a-145">See also</span></span>



[<span data-ttu-id="7ac8a-146">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7ac8a-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7ac8a-147">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="7ac8a-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7ac8a-148">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7ac8a-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7ac8a-149">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="7ac8a-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

