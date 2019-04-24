---
title: Propiedad canónica PidTagContainerHierarchy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerHierarchy
api_type:
- HeaderDef
ms.assetid: 6917510d-ca1e-4049-9eab-09313753ecf0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f009d7ce5cd1856ccff1e00953188c8edde7a6bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332861"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a><span data-ttu-id="2a468-103">Propiedad canónica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="2a468-103">PidTagContainerHierarchy Canonical Property</span></span>

  
  
<span data-ttu-id="2a468-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a468-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a468-105">Contiene un objeto de tabla de jerarquía incrustada que proporciona información acerca de los contenedores secundarios.</span><span class="sxs-lookup"><span data-stu-id="2a468-105">Contains an embedded hierarchy table object that provides information about the child containers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2a468-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2a468-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2a468-107">PR_CONTAINER_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="2a468-107">PR_CONTAINER_HIERARCHY</span></span>  <br/> |
|<span data-ttu-id="2a468-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2a468-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2a468-109">0x360E</span><span class="sxs-lookup"><span data-stu-id="2a468-109">0x360E</span></span>  <br/> |
|<span data-ttu-id="2a468-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2a468-110">Data type:</span></span>  <br/> |<span data-ttu-id="2a468-111">PT OBJECT</span><span class="sxs-lookup"><span data-stu-id="2a468-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="2a468-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2a468-112">Area:</span></span>  <br/> |<span data-ttu-id="2a468-113">Container</span><span class="sxs-lookup"><span data-stu-id="2a468-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a468-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2a468-114">Remarks</span></span>

<span data-ttu-id="2a468-115">Esta propiedad se puede excluir en las operaciones de [IMAPIProp:: CopyTo](imapiprop-copyto.md) o incluirse en las operaciones de [IMAPIProp:: CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="2a468-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="2a468-116">Como una propiedad de tipo **PT Object**, el método [IMAPIProp:: GetProps](imapiprop-getprops.md) no puede recuperarlo correctamente; debe obtener acceso a su contenido mediante el método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , lo que solicita el identificador de interfaz IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="2a468-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="2a468-117">Los proveedores de servicios deben informar al método [IMAPIProp:: GetPropList](imapiprop-getproplist.md) si está establecido, pero, opcionalmente, puede informar de él o no si no se ha establecido.</span><span class="sxs-lookup"><span data-stu-id="2a468-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="2a468-118">Para recuperar el contenido de la tabla, una aplicación cliente debe llamar al método [IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md) .</span><span class="sxs-lookup"><span data-stu-id="2a468-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method.</span></span> <span data-ttu-id="2a468-119">Para obtener más información, vea [tablas](hierarchy-tables.md)de jerarquías.</span><span class="sxs-lookup"><span data-stu-id="2a468-119">For more information, see [Hierarchy Tables](hierarchy-tables.md).</span></span> 
  
 <span data-ttu-id="2a468-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) y esta propiedad son similares en uso.</span><span class="sxs-lookup"><span data-stu-id="2a468-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="2a468-121">Varias propiedades MAPI proporcionan acceso a las tablas:</span><span class="sxs-lookup"><span data-stu-id="2a468-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="2a468-122">**Property**</span><span class="sxs-lookup"><span data-stu-id="2a468-122">**Property**</span></span>|<span data-ttu-id="2a468-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="2a468-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2a468-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2a468-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2a468-125">Tabla contenido</span><span class="sxs-lookup"><span data-stu-id="2a468-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="2a468-126">**PR_CONTAINER_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="2a468-126">**PR_CONTAINER_HIERARCHY**</span></span> <br/> |<span data-ttu-id="2a468-127">Tabla de jerarquía</span><span class="sxs-lookup"><span data-stu-id="2a468-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="2a468-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2a468-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2a468-129">Tabla de contenido asociada</span><span class="sxs-lookup"><span data-stu-id="2a468-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="2a468-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2a468-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2a468-131">Tabla de datos adJuntos</span><span class="sxs-lookup"><span data-stu-id="2a468-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="2a468-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2a468-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2a468-133">Tabla de destinatarios</span><span class="sxs-lookup"><span data-stu-id="2a468-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="2a468-134">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a468-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2a468-135">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="2a468-135">Protocol specifications</span></span>

<span data-ttu-id="2a468-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a468-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a468-137">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="2a468-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2a468-138">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a468-138">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a468-139">Controla el orden y el flujo de transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="2a468-139">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="2a468-140">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a468-140">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a468-141">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="2a468-141">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2a468-142">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2a468-142">Header files</span></span>

<span data-ttu-id="2a468-143">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2a468-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="2a468-144">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2a468-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="2a468-145">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="2a468-145">Mapitags.h</span></span>
  
> <span data-ttu-id="2a468-146">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="2a468-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2a468-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a468-147">See also</span></span>



[<span data-ttu-id="2a468-148">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2a468-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2a468-149">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="2a468-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2a468-150">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2a468-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2a468-151">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="2a468-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

