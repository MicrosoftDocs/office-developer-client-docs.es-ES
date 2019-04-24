---
title: Propiedad canónica PidTagSearchFolderEfpFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderEfpFlags
api_type:
- COM
ms.assetid: ef82a75f-a09f-4880-ba6a-e739b16422a3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d670aa91cc60c051f8464f9d83536b888b44ca9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336431"
---
# <a name="pidtagsearchfolderefpflags-canonical-property"></a><span data-ttu-id="c8ba6-103">Propiedad canónica PidTagSearchFolderEfpFlags</span><span class="sxs-lookup"><span data-stu-id="c8ba6-103">PidTagSearchFolderEfpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="c8ba6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8ba6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8ba6-105">Contiene las marcas de carpeta extendidas que se aplican al contenedor de la carpeta de búsqueda de la carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c8ba6-105">Contains extended folder flags that apply to the search folder container for the search folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c8ba6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c8ba6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c8ba6-107">PR_WB_SF_EFP_FLAGS</span><span class="sxs-lookup"><span data-stu-id="c8ba6-107">PR_WB_SF_EFP_FLAGS</span></span>  <br/> |
|<span data-ttu-id="c8ba6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c8ba6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c8ba6-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="c8ba6-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="c8ba6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c8ba6-110">Data type:</span></span>  <br/> |<span data-ttu-id="c8ba6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c8ba6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c8ba6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c8ba6-112">Area:</span></span>  <br/> |<span data-ttu-id="c8ba6-113">Buscar </span><span class="sxs-lookup"><span data-stu-id="c8ba6-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8ba6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c8ba6-114">Remarks</span></span>

<span data-ttu-id="c8ba6-115">Esta propiedad debe contener expresamente los indicadores en la propiedad **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) y la subpropiedad **ExtendedFlags** en el campo b para la carpeta.</span><span class="sxs-lookup"><span data-stu-id="c8ba6-115">This property should specifically contain the flags in the **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) property, and the **ExtendedFlags** sub-property, in field b for the folder.</span></span> <span data-ttu-id="c8ba6-116">Para obtener información acerca de las marcas de carpeta, vea [[ms-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c8ba6-116">For information about folder flags see the [[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c8ba6-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c8ba6-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c8ba6-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c8ba6-118">Protocol specifications</span></span>

<span data-ttu-id="c8ba6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8ba6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8ba6-120">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c8ba6-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c8ba6-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8ba6-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8ba6-122">Especifica las propiedades y operaciones para manipular una configuración de lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c8ba6-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
<span data-ttu-id="c8ba6-123">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8ba6-123">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8ba6-124">Especifica la ubicación y las propiedades de los datos de configuración del cliente y el servidor, como las listas de categorías compartidas y las horas laborables.</span><span class="sxs-lookup"><span data-stu-id="c8ba6-124">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c8ba6-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c8ba6-125">Header files</span></span>

<span data-ttu-id="c8ba6-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c8ba6-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c8ba6-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c8ba6-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="c8ba6-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="c8ba6-128">Mapitags.h</span></span>
  
> <span data-ttu-id="c8ba6-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c8ba6-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8ba6-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8ba6-130">See also</span></span>



[<span data-ttu-id="c8ba6-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c8ba6-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c8ba6-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="c8ba6-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c8ba6-133">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c8ba6-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c8ba6-134">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="c8ba6-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

