---
title: Propiedad canónica PidTagScheduleInfoAutoAcceptAppointments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAutoAcceptAppointments
api_type:
- COM
ms.assetid: 79505b29-2706-472b-b084-ab74be7b3405
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 15feea923c31bd7f88fcb3b346905e37af106d84
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564076"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a><span data-ttu-id="435fc-103">Propiedad canónica PidTagScheduleInfoAutoAcceptAppointments</span><span class="sxs-lookup"><span data-stu-id="435fc-103">PidTagScheduleInfoAutoAcceptAppointments Canonical Property</span></span>

  
  
<span data-ttu-id="435fc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="435fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="435fc-105">Contiene TRUE si un cliente o servidor debe responder automáticamente a todas las solicitudes de reunión para el asistente o un recurso.</span><span class="sxs-lookup"><span data-stu-id="435fc-105">Contains TRUE if a client or server should automatically respond to all meeting requests for the attendee or resource.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="435fc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="435fc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="435fc-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span><span class="sxs-lookup"><span data-stu-id="435fc-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span></span>  <br/> |
|<span data-ttu-id="435fc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="435fc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="435fc-109">0x686D</span><span class="sxs-lookup"><span data-stu-id="435fc-109">0x686D</span></span>  <br/> |
|<span data-ttu-id="435fc-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="435fc-110">Data type:</span></span>  <br/> |<span data-ttu-id="435fc-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="435fc-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="435fc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="435fc-112">Area:</span></span>  <br/> |<span data-ttu-id="435fc-113">Libre/ocupado</span><span class="sxs-lookup"><span data-stu-id="435fc-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="435fc-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="435fc-114">Remarks</span></span>

<span data-ttu-id="435fc-115">Al responder, la respuesta debe ser la aceptación, a menos que para una restricción adicional se especifica mediante la **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) o **PR_SCHDINFO_DISALLOW_ OVERLAPPING_APPTS** se cumple las propiedades ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="435fc-115">When responding, the response must be acceptance, unless for an additional constraint that is specified by the **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) or **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) properties is met.</span></span> <span data-ttu-id="435fc-116">Un valor de FALSE o la ausencia de esta propiedad indica que un cliente o servidor debe no aceptar automáticamente las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="435fc-116">A value of FALSE or the absence of this property indicates that a client or server must not automatically accept meeting requests.</span></span> <span data-ttu-id="435fc-117">No es una propiedad necesaria.</span><span class="sxs-lookup"><span data-stu-id="435fc-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="435fc-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="435fc-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="435fc-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="435fc-119">Protocol specifications</span></span>

<span data-ttu-id="435fc-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="435fc-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="435fc-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="435fc-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="435fc-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="435fc-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="435fc-123">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="435fc-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="435fc-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="435fc-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="435fc-125">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="435fc-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="435fc-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="435fc-126">Header files</span></span>

<span data-ttu-id="435fc-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="435fc-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="435fc-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="435fc-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="435fc-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="435fc-129">Mapitags.h</span></span>
  
> <span data-ttu-id="435fc-130">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="435fc-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="435fc-131">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="435fc-131">See also</span></span>



[<span data-ttu-id="435fc-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="435fc-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="435fc-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="435fc-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="435fc-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="435fc-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="435fc-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="435fc-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

