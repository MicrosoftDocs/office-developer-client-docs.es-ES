---
title: Propiedad canónica PidTagSearchFolderDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderDefinition
api_type:
- COM
ms.assetid: a61056e7-365c-4972-abf7-26e2ab07105d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3b4e5fa7228cf243c79a8ec0c9e2b73b7da21c6f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398790"
---
# <a name="pidtagsearchfolderdefinition-canonical-property"></a><span data-ttu-id="9ff10-103">Propiedad canónica PidTagSearchFolderDefinition</span><span class="sxs-lookup"><span data-stu-id="9ff10-103">PidTagSearchFolderDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="9ff10-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ff10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ff10-105">Contiene los datos que especifican los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9ff10-105">Contains data that specifies the search criteria.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9ff10-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9ff10-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ff10-107">PR_WB_SF_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="9ff10-107">PR_WB_SF_DEFINITION</span></span>  <br/> |
|<span data-ttu-id="9ff10-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9ff10-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9ff10-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="9ff10-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="9ff10-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9ff10-110">Data type:</span></span>  <br/> |<span data-ttu-id="9ff10-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9ff10-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9ff10-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9ff10-112">Area:</span></span>  <br/> |<span data-ttu-id="9ff10-113">Búsqueda</span><span class="sxs-lookup"><span data-stu-id="9ff10-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ff10-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9ff10-114">Remarks</span></span>

<span data-ttu-id="9ff10-115">El contenido específico de cada campo de los objetos binarios de grandes (BLOB) contenida en esta propiedad depende de que el identificador de plantilla que se especifica en la propiedad **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9ff10-115">The specific content of each field of the binary large object (BLOB) contained in this property is dependent upon the template ID that is specified in **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="9ff10-116">Para obtener información acerca de las plantillas de estructura y la búsqueda BLOB, vea [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9ff10-116">For information about the BLOB structure and search templates, see [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9ff10-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ff10-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9ff10-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="9ff10-118">Protocol specifications</span></span>

<span data-ttu-id="9ff10-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ff10-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ff10-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9ff10-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9ff10-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ff10-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ff10-122">Especifica las propiedades y operaciones para manipular la configuración de la lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9ff10-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9ff10-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9ff10-123">Header files</span></span>

<span data-ttu-id="9ff10-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9ff10-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ff10-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9ff10-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="9ff10-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9ff10-126">Mapitags.h</span></span>
  
> <span data-ttu-id="9ff10-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="9ff10-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ff10-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ff10-128">See also</span></span>



[<span data-ttu-id="9ff10-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9ff10-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ff10-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="9ff10-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ff10-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9ff10-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ff10-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="9ff10-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

