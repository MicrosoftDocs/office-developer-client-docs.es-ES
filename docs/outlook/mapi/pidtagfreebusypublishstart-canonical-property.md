---
title: Propiedad canónica PidTagFreeBusyPublishStart
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyPublishStart
api_type:
- HeaderDef
ms.assetid: d059f913-3d61-4bec-8215-5b07f0fba488
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8d262c17ed433222cbb037ab6e86120d300df93a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594064"
---
# <a name="pidtagfreebusypublishstart-canonical-property"></a><span data-ttu-id="66e1d-103">Propiedad canónica PidTagFreeBusyPublishStart</span><span class="sxs-lookup"><span data-stu-id="66e1d-103">PidTagFreeBusyPublishStart Canonical Property</span></span>

  
  
<span data-ttu-id="66e1d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66e1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66e1d-105">Contiene la hora de inicio del intervalo de publicación.</span><span class="sxs-lookup"><span data-stu-id="66e1d-105">Contains the start time of the publishing range.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="66e1d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="66e1d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="66e1d-107">PR_FREEBUSY_PUBLISH_START</span><span class="sxs-lookup"><span data-stu-id="66e1d-107">PR_FREEBUSY_PUBLISH_START</span></span>  <br/> |
|<span data-ttu-id="66e1d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="66e1d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="66e1d-109">0x6847</span><span class="sxs-lookup"><span data-stu-id="66e1d-109">0x6847</span></span>  <br/> |
|<span data-ttu-id="66e1d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="66e1d-110">Data type:</span></span>  <br/> |<span data-ttu-id="66e1d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="66e1d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="66e1d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="66e1d-112">Area:</span></span>  <br/> |<span data-ttu-id="66e1d-113">Libre/ocupado</span><span class="sxs-lookup"><span data-stu-id="66e1d-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66e1d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="66e1d-114">Remarks</span></span>

<span data-ttu-id="66e1d-115">El valor de esta propiedad es el número de minutos transcurridos desde la medianoche del 1 de enero de 1601 en hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="66e1d-115">The value for this property is the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="66e1d-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="66e1d-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="66e1d-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="66e1d-117">Protocol specifications</span></span>

<span data-ttu-id="66e1d-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66e1d-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66e1d-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="66e1d-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="66e1d-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66e1d-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66e1d-121">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="66e1d-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="66e1d-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="66e1d-122">Header files</span></span>

<span data-ttu-id="66e1d-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="66e1d-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="66e1d-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="66e1d-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="66e1d-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="66e1d-125">Mapitags.h</span></span>
  
> <span data-ttu-id="66e1d-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="66e1d-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="66e1d-127">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="66e1d-127">See also</span></span>



[<span data-ttu-id="66e1d-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="66e1d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="66e1d-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="66e1d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="66e1d-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="66e1d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="66e1d-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="66e1d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

