---
title: Propiedad canónica PidTagScheduleInfoFreeBusyTentative
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyTentative
api_type:
- COM
ms.assetid: 28453d29-30c5-405b-84d2-5bb5f281756c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a00505b765abdcb7b8fe9d68052774b30bbdf692
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820234"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a><span data-ttu-id="8df74-103">Propiedad canónica PidTagScheduleInfoFreeBusyTentative</span><span class="sxs-lookup"><span data-stu-id="8df74-103">PidTagScheduleInfoFreeBusyTentative Canonical Property</span></span>

  
  
<span data-ttu-id="8df74-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8df74-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8df74-105">Contiene los bloques de veces para que el estado de disponibilidad es provisional.</span><span class="sxs-lookup"><span data-stu-id="8df74-105">Contains the blocks of times for which the free/busy status is tentative.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8df74-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8df74-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8df74-107">PR_SCHDINFO_FREEBUSY_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="8df74-107">PR_SCHDINFO_FREEBUSY_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="8df74-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8df74-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8df74-109">0x6852</span><span class="sxs-lookup"><span data-stu-id="8df74-109">0x6852</span></span>  <br/> |
|<span data-ttu-id="8df74-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8df74-110">Data type:</span></span>  <br/> |<span data-ttu-id="8df74-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="8df74-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="8df74-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8df74-112">Area:</span></span>  <br/> |<span data-ttu-id="8df74-113">Libre/ocupado</span><span class="sxs-lookup"><span data-stu-id="8df74-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8df74-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8df74-114">Remarks</span></span>

<span data-ttu-id="8df74-115">Esta propiedad tiene tantos valores como el número de valores en **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8df74-115">This property has as many values as the number of values in **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)).</span></span> <span data-ttu-id="8df74-116">Cada valor binario representa un mes y se corresponde con el valor en el mismo índice en **PR_SCHDINFO_MONTHS_TENTATIVE**.</span><span class="sxs-lookup"><span data-stu-id="8df74-116">Each binary value represents a month and corresponds to the value at the same index in **PR_SCHDINFO_MONTHS_TENTATIVE**.</span></span> <span data-ttu-id="8df74-117">Los valores binarios se ordenan en el mismo orden que los valores de **PR_SCHDINFO_MONTHS_TENTATIVE**.</span><span class="sxs-lookup"><span data-stu-id="8df74-117">The binary values are sorted in the same order as the values in **PR_SCHDINFO_MONTHS_TENTATIVE**.</span></span>
  
<span data-ttu-id="8df74-118">Cada valor binario tiene uno o más bloques de 4 bytes y cada uno de ellos contiene la hora de inicio en los dos primeros bytes y la hora de finalización de la segunda de dos bytes en formato "little-endian".</span><span class="sxs-lookup"><span data-stu-id="8df74-118">Each binary value has one or more 4-BYTE blocks and each of them contains the start time in the first two bytes and end time in the second two bytes in little-endian format.</span></span> <span data-ttu-id="8df74-119">La hora de inicio es el número de minutos entre la medianoche de la hora Universal coordinada (UTC) del primer día del mes y la hora de inicio del evento en UTC.</span><span class="sxs-lookup"><span data-stu-id="8df74-119">The start time is the number of minutes between midnight Coordinated Universal Time (UTC) of the first day of the month and the start time of the event in UTC.</span></span> <span data-ttu-id="8df74-120">La hora de finalización es el número de minutos entre la medianoche UTC del primer día del mes y la hora de finalización del evento en UTC.</span><span class="sxs-lookup"><span data-stu-id="8df74-120">The end time is the number of minutes between midnight UTC of the first day of the month and the end time of the event in UTC.</span></span> <span data-ttu-id="8df74-121">Los bloques de 4 bytes se ordenan en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="8df74-121">The 4-BYTE blocks are sorted in ascending order.</span></span>
  
<span data-ttu-id="8df74-122">Bloques consecutivos o superposición de tiempo se combinan en un bloque con la hora de inicio como la hora de inicio de la primer bloque y la hora de finalización como la hora de finalización del último bloque.</span><span class="sxs-lookup"><span data-stu-id="8df74-122">Consecutive or overlapping blocks of time are merged into one block with start time as the start time of the first block and end time as the end time of the last block.</span></span> <span data-ttu-id="8df74-123">Si un evento es repartido por varios meses o años, el evento se divide en varios bloques, uno para cada mes.</span><span class="sxs-lookup"><span data-stu-id="8df74-123">If an event is spread across multiple months or years, the event is split into multiple blocks, one for each month.</span></span> <span data-ttu-id="8df74-124">Si no hay ningún evento provisional en el intervalo de publicación, a continuación, esta propiedad y **PR_SCHDINFO_MONTHS_TENTATIVE** no se deben establecer o se deben eliminar si ya existen.</span><span class="sxs-lookup"><span data-stu-id="8df74-124">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_MONTHS_TENTATIVE** must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="8df74-125">De lo contrario, se debe establecer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="8df74-125">Otherwise, this property must be set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8df74-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8df74-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8df74-127">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="8df74-127">Protocol specifications</span></span>

<span data-ttu-id="8df74-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8df74-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8df74-129">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8df74-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8df74-130">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8df74-130">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8df74-131">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="8df74-131">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8df74-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8df74-132">Header files</span></span>

<span data-ttu-id="8df74-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8df74-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="8df74-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8df74-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="8df74-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8df74-135">Mapitags.h</span></span>
  
> <span data-ttu-id="8df74-136">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="8df74-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8df74-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="8df74-137">See also</span></span>



[<span data-ttu-id="8df74-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8df74-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8df74-139">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="8df74-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8df74-140">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8df74-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8df74-141">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="8df74-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

