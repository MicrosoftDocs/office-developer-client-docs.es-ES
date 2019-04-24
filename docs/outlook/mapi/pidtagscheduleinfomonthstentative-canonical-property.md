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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359762"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a><span data-ttu-id="601fe-103">Propiedad canónica PidTagScheduleInfoMonthsTentative</span><span class="sxs-lookup"><span data-stu-id="601fe-103">PidTagScheduleInfoMonthsTentative Canonical Property</span></span>

  
  
<span data-ttu-id="601fe-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="601fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="601fe-105">Contiene los meses marcados como provisional en el mensaje de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="601fe-105">Contains the months marked tentative in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="601fe-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="601fe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="601fe-107">PR_SCHDINFO_MONTHS_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="601fe-107">PR_SCHDINFO_MONTHS_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="601fe-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="601fe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="601fe-109">0x6851</span><span class="sxs-lookup"><span data-stu-id="601fe-109">0x6851</span></span>  <br/> |
|<span data-ttu-id="601fe-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="601fe-110">Data type:</span></span>  <br/> |<span data-ttu-id="601fe-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="601fe-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="601fe-112">Área:</span><span class="sxs-lookup"><span data-stu-id="601fe-112">Area:</span></span>  <br/> |<span data-ttu-id="601fe-113">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="601fe-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="601fe-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="601fe-114">Remarks</span></span>

<span data-ttu-id="601fe-115">El número de valores de esta propiedad debe estar comprendido entre cero y el número de meses cubiertos por el intervalo de publicación, que es el período entre el **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) y \*\*PR_FREEBUSY_PUBLISH_END \*\*([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) propiedades.</span><span class="sxs-lookup"><span data-stu-id="601fe-115">The number of values in this property must be between zero and the number of months covered by the publishing range, which is the period between the **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) and **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="601fe-116">Cada valor de esta propiedad tiene un mes y un año codificados.</span><span class="sxs-lookup"><span data-stu-id="601fe-116">Each value in this property, has a month and year encoded in it.</span></span> <span data-ttu-id="601fe-117">Se calcula mediante la expresión "Year × 16 + Month" donde Year y month se basan en el calendario gregoriano.</span><span class="sxs-lookup"><span data-stu-id="601fe-117">This is calculated by using the expression "year × 16 + month" where year and month are based on the Gregorian calendar.</span></span> <span data-ttu-id="601fe-118">Los valores se ordenan en orden ascendente y se codifican en formato Little-Endian.</span><span class="sxs-lookup"><span data-stu-id="601fe-118">The values are sorted in ascending order and are encoded in little-endian format.</span></span> <span data-ttu-id="601fe-119">Si un evento se extiende por varios meses o varios años, debe haber un valor para cada uno de los meses que se encuentran en el intervalo de publicación.</span><span class="sxs-lookup"><span data-stu-id="601fe-119">If an event is spread across multiple months, or multiple years, there must be one value for each of the months that fall in the publishing range.</span></span> <span data-ttu-id="601fe-120">Si no hay ningún evento tentativa en el intervalo de publicación, esta propiedad y **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) no se deben establecer o deben eliminarse si ya existen.</span><span class="sxs-lookup"><span data-stu-id="601fe-120">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="601fe-121">De lo contrario, se debe establecer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="601fe-121">Otherwise, this property must be set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="601fe-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="601fe-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="601fe-123">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="601fe-123">Protocol specifications</span></span>

<span data-ttu-id="601fe-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="601fe-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="601fe-125">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="601fe-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="601fe-126">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="601fe-126">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="601fe-127">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="601fe-127">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="601fe-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="601fe-128">Header files</span></span>

<span data-ttu-id="601fe-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="601fe-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="601fe-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="601fe-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="601fe-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="601fe-131">Mapitags.h</span></span>
  
> <span data-ttu-id="601fe-132">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="601fe-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="601fe-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="601fe-133">See also</span></span>



[<span data-ttu-id="601fe-134">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="601fe-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="601fe-135">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="601fe-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="601fe-136">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="601fe-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="601fe-137">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="601fe-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

