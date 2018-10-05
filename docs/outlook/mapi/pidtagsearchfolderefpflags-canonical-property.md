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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400666"
---
# <a name="pidtagsearchfolderefpflags-canonical-property"></a><span data-ttu-id="1e9ee-103">Propiedad canónica PidTagSearchFolderEfpFlags</span><span class="sxs-lookup"><span data-stu-id="1e9ee-103">PidTagSearchFolderEfpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="1e9ee-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e9ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e9ee-105">Contiene los indicadores de carpeta extendida que se aplican en el contenedor de la carpeta de búsqueda para la carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1e9ee-105">Contains extended folder flags that apply to the search folder container for the search folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1e9ee-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1e9ee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1e9ee-107">PR_WB_SF_EFP_FLAGS</span><span class="sxs-lookup"><span data-stu-id="1e9ee-107">PR_WB_SF_EFP_FLAGS</span></span>  <br/> |
|<span data-ttu-id="1e9ee-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1e9ee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1e9ee-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="1e9ee-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="1e9ee-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1e9ee-110">Data type:</span></span>  <br/> |<span data-ttu-id="1e9ee-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1e9ee-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1e9ee-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1e9ee-112">Area:</span></span>  <br/> |<span data-ttu-id="1e9ee-113">Búsqueda</span><span class="sxs-lookup"><span data-stu-id="1e9ee-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e9ee-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1e9ee-114">Remarks</span></span>

<span data-ttu-id="1e9ee-115">Esta propiedad debe contener específicamente los indicadores de la propiedad **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) y la propiedad subcaracterística **ExtendedFlags** , en el campo b para la carpeta.</span><span class="sxs-lookup"><span data-stu-id="1e9ee-115">This property should specifically contain the flags in the **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) property, and the **ExtendedFlags** sub-property, in field b for the folder.</span></span> <span data-ttu-id="1e9ee-116">Para obtener información acerca de los indicadores de carpeta, consulte el [[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="1e9ee-116">For information about folder flags see the [[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1e9ee-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e9ee-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1e9ee-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="1e9ee-118">Protocol specifications</span></span>

<span data-ttu-id="1e9ee-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e9ee-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e9ee-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1e9ee-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1e9ee-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e9ee-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e9ee-122">Especifica las propiedades y operaciones para manipular la configuración de la lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1e9ee-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
<span data-ttu-id="1e9ee-123">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e9ee-123">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e9ee-124">Especifica la ubicación y las propiedades de datos de configuración de cliente y servidor, como las listas de categoría compartida y horas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="1e9ee-124">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1e9ee-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1e9ee-125">Header files</span></span>

<span data-ttu-id="1e9ee-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1e9ee-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1e9ee-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1e9ee-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="1e9ee-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1e9ee-128">Mapitags.h</span></span>
  
> <span data-ttu-id="1e9ee-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="1e9ee-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e9ee-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e9ee-130">See also</span></span>



[<span data-ttu-id="1e9ee-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1e9ee-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1e9ee-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="1e9ee-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1e9ee-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1e9ee-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1e9ee-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="1e9ee-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

