---
title: Propiedad canónica PidTagScheduleInfoMonthsTentative
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsTentative
api_type:
- COM
ms.assetid: 3179442c-6499-464a-93af-eb0a7a5b0d30
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6fa0579dcd98a0d819e58e62d8a42cb2972a9d1e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391559"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a><span data-ttu-id="7c74b-103">Propiedad canónica PidTagScheduleInfoMonthsTentative</span><span class="sxs-lookup"><span data-stu-id="7c74b-103">PidTagScheduleInfoMonthsTentative Canonical Property</span></span>

  
  
<span data-ttu-id="7c74b-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c74b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c74b-105">Contiene los meses marcados como provisionales en el mensaje de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="7c74b-105">Contains the months marked tentative in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7c74b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7c74b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7c74b-107">PR_SCHDINFO_MONTHS_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="7c74b-107">PR_SCHDINFO_MONTHS_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="7c74b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7c74b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7c74b-109">0x6851</span><span class="sxs-lookup"><span data-stu-id="7c74b-109">0x6851</span></span>  <br/> |
|<span data-ttu-id="7c74b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7c74b-110">Data type:</span></span>  <br/> |<span data-ttu-id="7c74b-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="7c74b-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="7c74b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7c74b-112">Area:</span></span>  <br/> |<span data-ttu-id="7c74b-113">Libre/ocupado</span><span class="sxs-lookup"><span data-stu-id="7c74b-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c74b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7c74b-114">Remarks</span></span>

<span data-ttu-id="7c74b-115">El número de valores de esta propiedad debe estar comprendido entre cero y el número de meses cubierto por el intervalo de publicación, que es el período entre la **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) y \*\*PR_FREEBUSY_PUBLISH_END \*\*Propiedades ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7c74b-115">The number of values in this property must be between zero and the number of months covered by the publishing range, which is the period between the **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) and **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="7c74b-116">Cada valor de esta propiedad tiene un mes y año codificado en ella.</span><span class="sxs-lookup"><span data-stu-id="7c74b-116">Each value in this property, has a month and year encoded in it.</span></span> <span data-ttu-id="7c74b-117">Esto se calcula mediante el uso de la expresión "año × 16 + mes" donde el mes y el año se basan en el calendario gregoriano.</span><span class="sxs-lookup"><span data-stu-id="7c74b-117">This is calculated by using the expression "year × 16 + month" where year and month are based on the Gregorian calendar.</span></span> <span data-ttu-id="7c74b-118">Los valores se ordenan en orden ascendente y se codifican en formato "little-endian".</span><span class="sxs-lookup"><span data-stu-id="7c74b-118">The values are sorted in ascending order and are encoded in little-endian format.</span></span> <span data-ttu-id="7c74b-119">Si un evento es repartido por varios meses o años varios, debe ser un valor para cada uno de los meses que se encuentran en el intervalo de publicación.</span><span class="sxs-lookup"><span data-stu-id="7c74b-119">If an event is spread across multiple months, or multiple years, there must be one value for each of the months that fall in the publishing range.</span></span> <span data-ttu-id="7c74b-120">Si no hay ningún evento provisional en el intervalo de publicación, a continuación, esta propiedad y **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) no se deben establecer o se deben eliminar si ya existen.</span><span class="sxs-lookup"><span data-stu-id="7c74b-120">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="7c74b-121">De lo contrario, se debe establecer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="7c74b-121">Otherwise, this property must be set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7c74b-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7c74b-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7c74b-123">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="7c74b-123">Protocol specifications</span></span>

<span data-ttu-id="7c74b-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c74b-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c74b-125">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7c74b-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7c74b-126">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c74b-126">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c74b-127">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="7c74b-127">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7c74b-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7c74b-128">Header files</span></span>

<span data-ttu-id="7c74b-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7c74b-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="7c74b-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7c74b-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="7c74b-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7c74b-131">Mapitags.h</span></span>
  
> <span data-ttu-id="7c74b-132">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="7c74b-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c74b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c74b-133">See also</span></span>



[<span data-ttu-id="7c74b-134">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7c74b-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7c74b-135">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="7c74b-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7c74b-136">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7c74b-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7c74b-137">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="7c74b-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

