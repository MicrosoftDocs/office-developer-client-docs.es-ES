---
title: Propiedad canónica PidTagScheduleInfoDisallowRecurringAppts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowRecurringAppts
api_type:
- COM
ms.assetid: 61e082dd-f5bc-479b-990a-c9c0360f883e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 19e2cc0b95aaefbca1ec618c55b8d397de4d340e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593693"
---
# <a name="pidtagscheduleinfodisallowrecurringappts-canonical-property"></a><span data-ttu-id="6f2cd-103">Propiedad canónica PidTagScheduleInfoDisallowRecurringAppts</span><span class="sxs-lookup"><span data-stu-id="6f2cd-103">PidTagScheduleInfoDisallowRecurringAppts Canonical Property</span></span>

  
  
<span data-ttu-id="6f2cd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f2cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f2cd-105">Contiene TRUE cuando la respuesta automática a citas periódicas es rechazar.</span><span class="sxs-lookup"><span data-stu-id="6f2cd-105">Contains TRUE when the automatic response to recurring appointments is decline.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6f2cd-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6f2cd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6f2cd-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span><span class="sxs-lookup"><span data-stu-id="6f2cd-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span></span>  <br/> |
|<span data-ttu-id="6f2cd-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6f2cd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6f2cd-109">0x686E</span><span class="sxs-lookup"><span data-stu-id="6f2cd-109">0x686E</span></span>  <br/> |
|<span data-ttu-id="6f2cd-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6f2cd-110">Data type:</span></span>  <br/> |<span data-ttu-id="6f2cd-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6f2cd-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6f2cd-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6f2cd-112">Area:</span></span>  <br/> |<span data-ttu-id="6f2cd-113">Libre/ocupado</span><span class="sxs-lookup"><span data-stu-id="6f2cd-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f2cd-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6f2cd-114">Remarks</span></span>

<span data-ttu-id="6f2cd-115">Esta propiedad sólo es significativa cuando el valor de la propiedad **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) es TRUE.</span><span class="sxs-lookup"><span data-stu-id="6f2cd-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="6f2cd-116">La ausencia de esta propiedad indica que se deben aceptar las reuniones periódicas.</span><span class="sxs-lookup"><span data-stu-id="6f2cd-116">The absence of this property indicates that recurring meetings must be accepted.</span></span> <span data-ttu-id="6f2cd-117">No es una propiedad necesaria.</span><span class="sxs-lookup"><span data-stu-id="6f2cd-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6f2cd-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6f2cd-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6f2cd-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="6f2cd-119">Protocol specifications</span></span>

<span data-ttu-id="6f2cd-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f2cd-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f2cd-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="6f2cd-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6f2cd-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f2cd-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f2cd-123">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="6f2cd-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="6f2cd-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f2cd-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f2cd-125">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="6f2cd-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6f2cd-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6f2cd-126">Header files</span></span>

<span data-ttu-id="6f2cd-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6f2cd-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="6f2cd-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6f2cd-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="6f2cd-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6f2cd-129">Mapitags.h</span></span>
  
> <span data-ttu-id="6f2cd-130">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="6f2cd-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f2cd-131">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="6f2cd-131">See also</span></span>



[<span data-ttu-id="6f2cd-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6f2cd-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6f2cd-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="6f2cd-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6f2cd-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="6f2cd-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6f2cd-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="6f2cd-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

