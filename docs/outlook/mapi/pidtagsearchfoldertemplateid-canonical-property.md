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
ms.openlocfilehash: bee22a7a435b99f4b94473a3f6eb4b7f32517128
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336627"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a><span data-ttu-id="7f7c3-103">Propiedad canónica PidTagSearchFolderTemplateId</span><span class="sxs-lookup"><span data-stu-id="7f7c3-103">PidTagSearchFolderTemplateId Canonical Property</span></span>

  
  
<span data-ttu-id="7f7c3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f7c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f7c3-105">Contiene el identificador de la plantilla que se usa para la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="7f7c3-105">Contains the ID of the template that is being used for the search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f7c3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7f7c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7f7c3-107">PR_WB_SF_TEMPLATE_ID</span><span class="sxs-lookup"><span data-stu-id="7f7c3-107">PR_WB_SF_TEMPLATE_ID</span></span>  <br/> |
|<span data-ttu-id="7f7c3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7f7c3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7f7c3-109">0x6841</span><span class="sxs-lookup"><span data-stu-id="7f7c3-109">0x6841</span></span>  <br/> |
|<span data-ttu-id="7f7c3-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7f7c3-110">Data type:</span></span>  <br/> |<span data-ttu-id="7f7c3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7f7c3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7f7c3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7f7c3-112">Area:</span></span>  <br/> |<span data-ttu-id="7f7c3-113">Búsqueda</span><span class="sxs-lookup"><span data-stu-id="7f7c3-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f7c3-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7f7c3-114">Remarks</span></span>

<span data-ttu-id="7f7c3-115">Los criterios de carpeta de búsqueda se especifican mediante una plantilla.</span><span class="sxs-lookup"><span data-stu-id="7f7c3-115">Search folder criteria is specified by a template.</span></span> <span data-ttu-id="7f7c3-116">Esta propiedad del mensaje que define la carpeta de búsqueda identifica su plantilla correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7f7c3-116">This property on the message that defines the search folder identifies its corresponding template.</span></span> <span data-ttu-id="7f7c3-117">Además de definir criterios de búsqueda, una plantilla también define las carpetas que se excluirán de la búsqueda, define los elementos que se excluirán de la búsqueda y especifica el valor de **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7f7c3-117">In addition to defining search criteria, a template also defines folders to exclude from the search, defines items to exclude from the search, and specifies the value of **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span></span>
  
<span data-ttu-id="7f7c3-118">Para obtener más información acerca de las plantillas de carpeta de búsqueda, vea [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7f7c3-118">For more information about Search Folder Templates see [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7f7c3-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f7c3-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7f7c3-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="7f7c3-120">Protocol specifications</span></span>

<span data-ttu-id="7f7c3-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f7c3-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f7c3-122">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="7f7c3-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7f7c3-123">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f7c3-123">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f7c3-124">Especifica las propiedades y las operaciones para manipular una configuración de lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="7f7c3-124">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7f7c3-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7f7c3-125">Header files</span></span>

<span data-ttu-id="7f7c3-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7f7c3-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f7c3-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7f7c3-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="7f7c3-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7f7c3-128">Mapitags.h</span></span>
  
> <span data-ttu-id="7f7c3-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="7f7c3-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f7c3-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f7c3-130">See also</span></span>



[<span data-ttu-id="7f7c3-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7f7c3-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f7c3-132">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="7f7c3-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f7c3-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7f7c3-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f7c3-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="7f7c3-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

