---
title: Propiedad canónico PidTagSearchFolderDefinition
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: d19904b65b95468bd38df75aa8e05afdf0075961
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820235"
---
# <a name="pidtagsearchfolderdefinition-canonical-property"></a><span data-ttu-id="fe752-103">Propiedad canónico PidTagSearchFolderDefinition</span><span class="sxs-lookup"><span data-stu-id="fe752-103">PidTagSearchFolderDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="fe752-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fe752-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fe752-105">Contiene los datos que especifican los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="fe752-105">Contains data that specifies the search criteria.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fe752-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fe752-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fe752-107">PR_WB_SF_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="fe752-107">PR_WB_SF_DEFINITION</span></span>  <br/> |
|<span data-ttu-id="fe752-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fe752-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fe752-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="fe752-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="fe752-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fe752-110">Data type:</span></span>  <br/> |<span data-ttu-id="fe752-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fe752-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fe752-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fe752-112">Area:</span></span>  <br/> |<span data-ttu-id="fe752-113">B?squeda</span><span class="sxs-lookup"><span data-stu-id="fe752-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe752-114">Notas</span><span class="sxs-lookup"><span data-stu-id="fe752-114">Remarks</span></span>

<span data-ttu-id="fe752-115">El contenido específico de cada campo de los objetos binarios de grandes (BLOB) contenida en esta propiedad depende de que el identificador de plantilla que se especifica en la propiedad **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fe752-115">The specific content of each field of the binary large object (BLOB) contained in this property is dependent upon the template ID that is specified in **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="fe752-116">Para obtener información acerca de las plantillas de estructura y la búsqueda BLOB, vea [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="fe752-116">For information about the BLOB structure and search templates, see [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fe752-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fe752-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fe752-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="fe752-118">Protocol specifications</span></span>

<span data-ttu-id="fe752-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe752-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe752-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fe752-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fe752-121">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe752-121">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe752-122">Especifica las propiedades y operaciones para manipular la configuración de la lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="fe752-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fe752-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fe752-123">Header files</span></span>

<span data-ttu-id="fe752-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fe752-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="fe752-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fe752-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="fe752-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fe752-126">Mapitags.h</span></span>
  
> <span data-ttu-id="fe752-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="fe752-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fe752-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="fe752-128">See also</span></span>



[<span data-ttu-id="fe752-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fe752-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fe752-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="fe752-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fe752-131">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="fe752-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fe752-132">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="fe752-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

