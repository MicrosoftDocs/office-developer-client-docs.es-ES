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
ms.openlocfilehash: 6fe724d70ac86b1c51e72f243ef9255dd452be9c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386890"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a><span data-ttu-id="f7ec3-103">Propiedad canónica PidTagScheduleInfoAutoAcceptAppointments</span><span class="sxs-lookup"><span data-stu-id="f7ec3-103">PidTagScheduleInfoAutoAcceptAppointments Canonical Property</span></span>

  
  
<span data-ttu-id="f7ec3-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7ec3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7ec3-105">Contiene TRUE si un cliente o servidor debe responder automáticamente a todas las solicitudes de reunión para el asistente o un recurso.</span><span class="sxs-lookup"><span data-stu-id="f7ec3-105">Contains TRUE if a client or server should automatically respond to all meeting requests for the attendee or resource.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f7ec3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f7ec3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f7ec3-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span><span class="sxs-lookup"><span data-stu-id="f7ec3-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span></span>  <br/> |
|<span data-ttu-id="f7ec3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f7ec3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f7ec3-109">0x686D</span><span class="sxs-lookup"><span data-stu-id="f7ec3-109">0x686D</span></span>  <br/> |
|<span data-ttu-id="f7ec3-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f7ec3-110">Data type:</span></span>  <br/> |<span data-ttu-id="f7ec3-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f7ec3-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f7ec3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f7ec3-112">Area:</span></span>  <br/> |<span data-ttu-id="f7ec3-113">Libre/ocupado</span><span class="sxs-lookup"><span data-stu-id="f7ec3-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7ec3-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f7ec3-114">Remarks</span></span>

<span data-ttu-id="f7ec3-115">Al responder, la respuesta debe ser la aceptación, a menos que para una restricción adicional se especifica mediante la **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) o **PR_SCHDINFO_DISALLOW_ OVERLAPPING_APPTS** se cumple las propiedades ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f7ec3-115">When responding, the response must be acceptance, unless for an additional constraint that is specified by the **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) or **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) properties is met.</span></span> <span data-ttu-id="f7ec3-116">Un valor de FALSE o la ausencia de esta propiedad indica que un cliente o servidor debe no aceptar automáticamente las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="f7ec3-116">A value of FALSE or the absence of this property indicates that a client or server must not automatically accept meeting requests.</span></span> <span data-ttu-id="f7ec3-117">No es una propiedad necesaria.</span><span class="sxs-lookup"><span data-stu-id="f7ec3-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f7ec3-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7ec3-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f7ec3-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f7ec3-119">Protocol specifications</span></span>

<span data-ttu-id="f7ec3-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7ec3-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7ec3-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f7ec3-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f7ec3-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7ec3-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7ec3-123">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="f7ec3-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="f7ec3-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7ec3-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7ec3-125">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="f7ec3-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f7ec3-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f7ec3-126">Header files</span></span>

<span data-ttu-id="f7ec3-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7ec3-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="f7ec3-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f7ec3-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="f7ec3-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f7ec3-129">Mapitags.h</span></span>
  
> <span data-ttu-id="f7ec3-130">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f7ec3-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7ec3-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7ec3-131">See also</span></span>



[<span data-ttu-id="f7ec3-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f7ec3-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f7ec3-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f7ec3-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f7ec3-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f7ec3-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f7ec3-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f7ec3-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

