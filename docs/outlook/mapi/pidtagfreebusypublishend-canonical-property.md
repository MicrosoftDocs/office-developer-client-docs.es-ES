---
title: Propiedad canónica PidTagFreeBusyPublishEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyPublishEnd
api_type:
- HeaderDef
ms.assetid: df239741-6a63-4cd4-9bbb-42c0f5c668a5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1f7f439b211b60f7acad3a9dd19c50a21923c1cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819540"
---
# <a name="pidtagfreebusypublishend-canonical-property"></a><span data-ttu-id="a8ec9-103">Propiedad canónica PidTagFreeBusyPublishEnd</span><span class="sxs-lookup"><span data-stu-id="a8ec9-103">PidTagFreeBusyPublishEnd Canonical Property</span></span>

  
  
<span data-ttu-id="a8ec9-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a8ec9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a8ec9-105">Contiene la hora de finalización del intervalo de publicación.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-105">Contains the end time of the publishing range.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a8ec9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a8ec9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a8ec9-107">PR_FREEBUSY_PUBLISH_END</span><span class="sxs-lookup"><span data-stu-id="a8ec9-107">PR_FREEBUSY_PUBLISH_END</span></span>  <br/> |
|<span data-ttu-id="a8ec9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a8ec9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a8ec9-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="a8ec9-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="a8ec9-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a8ec9-110">Data type:</span></span>  <br/> |<span data-ttu-id="a8ec9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a8ec9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a8ec9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a8ec9-112">Area:</span></span>  <br/> |<span data-ttu-id="a8ec9-113">Libre/ocupado</span><span class="sxs-lookup"><span data-stu-id="a8ec9-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8ec9-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a8ec9-114">Remarks</span></span>

<span data-ttu-id="a8ec9-115">El valor de esta propiedad se calcula agregando el valor de **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) para que la fecha de inicio del intervalo de publicación.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-115">The value for this property is computed by adding the value of **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) to the start date of the publishing range.</span></span> <span data-ttu-id="a8ec9-116">Este valor se expresa como el número de minutos transcurridos desde la medianoche del 1 de enero de 1601 en hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="a8ec9-116">This value is expressed as the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a8ec9-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a8ec9-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a8ec9-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="a8ec9-118">Protocol specifications</span></span>

<span data-ttu-id="a8ec9-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8ec9-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8ec9-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a8ec9-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8ec9-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8ec9-122">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a8ec9-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a8ec9-123">Header files</span></span>

<span data-ttu-id="a8ec9-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a8ec9-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="a8ec9-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="a8ec9-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a8ec9-126">Mapitags.h</span></span>
  
> <span data-ttu-id="a8ec9-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a8ec9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8ec9-128">See also</span></span>



[<span data-ttu-id="a8ec9-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a8ec9-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a8ec9-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="a8ec9-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a8ec9-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a8ec9-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a8ec9-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="a8ec9-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
