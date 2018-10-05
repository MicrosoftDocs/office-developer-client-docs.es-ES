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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387205"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a><span data-ttu-id="f7b4c-103">Propiedad canónica PidTagSearchFolderTemplateId</span><span class="sxs-lookup"><span data-stu-id="f7b4c-103">PidTagSearchFolderTemplateId Canonical Property</span></span>

  
  
<span data-ttu-id="f7b4c-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7b4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7b4c-105">Contiene el identificador de la plantilla que se utiliza para la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f7b4c-105">Contains the ID of the template that is being used for the search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f7b4c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f7b4c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f7b4c-107">PR_WB_SF_TEMPLATE_ID</span><span class="sxs-lookup"><span data-stu-id="f7b4c-107">PR_WB_SF_TEMPLATE_ID</span></span>  <br/> |
|<span data-ttu-id="f7b4c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f7b4c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f7b4c-109">0x6841</span><span class="sxs-lookup"><span data-stu-id="f7b4c-109">0x6841</span></span>  <br/> |
|<span data-ttu-id="f7b4c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f7b4c-110">Data type:</span></span>  <br/> |<span data-ttu-id="f7b4c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f7b4c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f7b4c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f7b4c-112">Area:</span></span>  <br/> |<span data-ttu-id="f7b4c-113">Búsqueda</span><span class="sxs-lookup"><span data-stu-id="f7b4c-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7b4c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f7b4c-114">Remarks</span></span>

<span data-ttu-id="f7b4c-115">Criterios de carpeta de búsqueda se especifica mediante una plantilla.</span><span class="sxs-lookup"><span data-stu-id="f7b4c-115">Search folder criteria is specified by a template.</span></span> <span data-ttu-id="f7b4c-116">Esta propiedad en el mensaje que define la carpeta de búsqueda identifica la plantilla correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f7b4c-116">This property on the message that defines the search folder identifies its corresponding template.</span></span> <span data-ttu-id="f7b4c-117">Además de definir los criterios de búsqueda, una plantilla también define las carpetas para excluir de la búsqueda, define los elementos que se deben excluir de la búsqueda y especifica el valor de **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f7b4c-117">In addition to defining search criteria, a template also defines folders to exclude from the search, defines items to exclude from the search, and specifies the value of **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span></span>
  
<span data-ttu-id="f7b4c-118">Para obtener más información acerca de las plantillas de la carpeta de búsqueda, vea [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f7b4c-118">For more information about Search Folder Templates see [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f7b4c-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7b4c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f7b4c-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f7b4c-120">Protocol specifications</span></span>

<span data-ttu-id="f7b4c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7b4c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7b4c-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f7b4c-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f7b4c-123">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7b4c-123">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7b4c-124">Especifica las propiedades y operaciones para manipular la configuración de la lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f7b4c-124">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f7b4c-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f7b4c-125">Header files</span></span>

<span data-ttu-id="f7b4c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7b4c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f7b4c-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f7b4c-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="f7b4c-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f7b4c-128">Mapitags.h</span></span>
  
> <span data-ttu-id="f7b4c-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f7b4c-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7b4c-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7b4c-130">See also</span></span>



[<span data-ttu-id="f7b4c-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f7b4c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f7b4c-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f7b4c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f7b4c-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f7b4c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f7b4c-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f7b4c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

