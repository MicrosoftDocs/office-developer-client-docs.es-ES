---
title: Propiedad canónica PidTagSearchFolderTemplateId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderTemplateId
api_type:
- COM
ms.assetid: 56288f55-b3ba-42df-9c90-f9b5857f19a1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4e752d3264a64ad7b467947c44d01eb7c47ec863
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820257"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a><span data-ttu-id="eb118-103">Propiedad canónica PidTagSearchFolderTemplateId</span><span class="sxs-lookup"><span data-stu-id="eb118-103">PidTagSearchFolderTemplateId Canonical Property</span></span>

  
  
<span data-ttu-id="eb118-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eb118-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eb118-105">Contiene el identificador de la plantilla que se utiliza para la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="eb118-105">Contains the ID of the template that is being used for the search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eb118-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="eb118-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eb118-107">PR_WB_SF_TEMPLATE_ID</span><span class="sxs-lookup"><span data-stu-id="eb118-107">PR_WB_SF_TEMPLATE_ID</span></span>  <br/> |
|<span data-ttu-id="eb118-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="eb118-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eb118-109">0x6841</span><span class="sxs-lookup"><span data-stu-id="eb118-109">0x6841</span></span>  <br/> |
|<span data-ttu-id="eb118-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="eb118-110">Data type:</span></span>  <br/> |<span data-ttu-id="eb118-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="eb118-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="eb118-112">Área:</span><span class="sxs-lookup"><span data-stu-id="eb118-112">Area:</span></span>  <br/> |<span data-ttu-id="eb118-113">Búsqueda</span><span class="sxs-lookup"><span data-stu-id="eb118-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb118-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eb118-114">Remarks</span></span>

<span data-ttu-id="eb118-115">Criterios de carpeta de búsqueda se especifica mediante una plantilla.</span><span class="sxs-lookup"><span data-stu-id="eb118-115">Search folder criteria is specified by a template.</span></span> <span data-ttu-id="eb118-116">Esta propiedad en el mensaje que define la carpeta de búsqueda identifica la plantilla correspondiente.</span><span class="sxs-lookup"><span data-stu-id="eb118-116">This property on the message that defines the search folder identifies its corresponding template.</span></span> <span data-ttu-id="eb118-117">Además de definir los criterios de búsqueda, una plantilla también define las carpetas para excluir de la búsqueda, define los elementos que se deben excluir de la búsqueda y especifica el valor de **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="eb118-117">In addition to defining search criteria, a template also defines folders to exclude from the search, defines items to exclude from the search, and specifies the value of **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span></span>
  
<span data-ttu-id="eb118-118">Para obtener más información acerca de las plantillas de la carpeta de búsqueda, vea [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="eb118-118">For more information about Search Folder Templates see [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="eb118-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="eb118-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eb118-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="eb118-120">Protocol specifications</span></span>

<span data-ttu-id="eb118-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb118-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb118-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="eb118-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="eb118-123">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb118-123">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb118-124">Especifica las propiedades y operaciones para manipular la configuración de la lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="eb118-124">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="eb118-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="eb118-125">Header files</span></span>

<span data-ttu-id="eb118-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eb118-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="eb118-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="eb118-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="eb118-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="eb118-128">Mapitags.h</span></span>
  
> <span data-ttu-id="eb118-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="eb118-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eb118-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb118-130">See also</span></span>



[<span data-ttu-id="eb118-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="eb118-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eb118-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="eb118-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eb118-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="eb118-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eb118-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="eb118-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

