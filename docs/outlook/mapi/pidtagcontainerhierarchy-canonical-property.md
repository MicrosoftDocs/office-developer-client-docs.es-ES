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
ms.openlocfilehash: 2c9598b583ba62adc42d6fb2b904dfe4981286ff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578111"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a><span data-ttu-id="f7b10-103">Propiedad canónica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="f7b10-103">PidTagContainerHierarchy Canonical Property</span></span>

  
  
<span data-ttu-id="f7b10-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7b10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7b10-105">Contiene un objeto de la tabla de jerarquía incrustado que proporciona información sobre el elemento secundario de contenedores.</span><span class="sxs-lookup"><span data-stu-id="f7b10-105">Contains an embedded hierarchy table object that provides information about the child containers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7b10-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f7b10-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f7b10-107">PR_CONTAINER_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="f7b10-107">PR_CONTAINER_HIERARCHY</span></span>  <br/> |
|<span data-ttu-id="f7b10-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f7b10-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f7b10-109">0x360E</span><span class="sxs-lookup"><span data-stu-id="f7b10-109">0x360E</span></span>  <br/> |
|<span data-ttu-id="f7b10-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f7b10-110">Data type:</span></span>  <br/> |<span data-ttu-id="f7b10-111">PT OBJECT</span><span class="sxs-lookup"><span data-stu-id="f7b10-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="f7b10-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f7b10-112">Area:</span></span>  <br/> |<span data-ttu-id="f7b10-113">Container</span><span class="sxs-lookup"><span data-stu-id="f7b10-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7b10-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f7b10-114">Remarks</span></span>

<span data-ttu-id="f7b10-115">Esta propiedad puede ser en las operaciones de [IMAPIProp::CopyTo](imapiprop-copyto.md) incluyen o excluyen de operaciones de [IMAPIProp::CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="f7b10-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="f7b10-116">Como una propiedad de tipo **pt Object**, no se correctamente puede recuperar mediante el método [IMAPIProp::GetProps](imapiprop-getprops.md) ; el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , que solicita el identificador de interfaz IID_IMAPITable debe tener acceso a su contenido.</span><span class="sxs-lookup"><span data-stu-id="f7b10-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="f7b10-117">Proveedores de servicios deben identificarlo al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) si está establecida, pero puede, opcionalmente, identificarlo o no, si no está establecido.</span><span class="sxs-lookup"><span data-stu-id="f7b10-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="f7b10-118">Para recuperar el contenido de la tabla, una aplicación de cliente debe llamar al método de [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) .</span><span class="sxs-lookup"><span data-stu-id="f7b10-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method.</span></span> <span data-ttu-id="f7b10-119">Para obtener más información, vea [Las tablas de jerarquía](hierarchy-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f7b10-119">For more information, see [Hierarchy Tables](hierarchy-tables.md).</span></span> 
  
 <span data-ttu-id="f7b10-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) y esta propiedad son similares en uso.</span><span class="sxs-lookup"><span data-stu-id="f7b10-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="f7b10-121">Varias propiedades MAPI proporcionan acceso a las tablas:</span><span class="sxs-lookup"><span data-stu-id="f7b10-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="f7b10-122">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="f7b10-122">**Property**</span></span>|<span data-ttu-id="f7b10-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="f7b10-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f7b10-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f7b10-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f7b10-125">Tabla de contenido</span><span class="sxs-lookup"><span data-stu-id="f7b10-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="f7b10-126">**PR_CONTAINER_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="f7b10-126">**PR_CONTAINER_HIERARCHY**</span></span> <br/> |<span data-ttu-id="f7b10-127">Tabla de jerarquía</span><span class="sxs-lookup"><span data-stu-id="f7b10-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="f7b10-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f7b10-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f7b10-129">Tabla de contenido asociada</span><span class="sxs-lookup"><span data-stu-id="f7b10-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="f7b10-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f7b10-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f7b10-131">Tabla de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="f7b10-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="f7b10-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f7b10-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f7b10-133">Tabla de destinatarios</span><span class="sxs-lookup"><span data-stu-id="f7b10-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f7b10-134">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7b10-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f7b10-135">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f7b10-135">Protocol specifications</span></span>

<span data-ttu-id="f7b10-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7b10-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7b10-137">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f7b10-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f7b10-138">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7b10-138">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7b10-139">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="f7b10-139">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="f7b10-140">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7b10-140">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7b10-141">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="f7b10-141">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f7b10-142">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f7b10-142">Header files</span></span>

<span data-ttu-id="f7b10-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7b10-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="f7b10-144">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f7b10-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="f7b10-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f7b10-145">Mapitags.h</span></span>
  
> <span data-ttu-id="f7b10-146">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f7b10-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7b10-147">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f7b10-147">See also</span></span>



[<span data-ttu-id="f7b10-148">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f7b10-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f7b10-149">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f7b10-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f7b10-150">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f7b10-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f7b10-151">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f7b10-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

