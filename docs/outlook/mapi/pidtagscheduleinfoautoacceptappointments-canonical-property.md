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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330096"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a><span data-ttu-id="52da1-103">Propiedad canónica PidTagScheduleInfoAutoAcceptAppointments</span><span class="sxs-lookup"><span data-stu-id="52da1-103">PidTagScheduleInfoAutoAcceptAppointments Canonical Property</span></span>

  
  
<span data-ttu-id="52da1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52da1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52da1-105">Contiene TRUE si un cliente o servidor debe responder automáticamente a todas las solicitudes de reunión para el asistente o recurso.</span><span class="sxs-lookup"><span data-stu-id="52da1-105">Contains TRUE if a client or server should automatically respond to all meeting requests for the attendee or resource.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="52da1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="52da1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="52da1-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span><span class="sxs-lookup"><span data-stu-id="52da1-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span></span>  <br/> |
|<span data-ttu-id="52da1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="52da1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="52da1-109">0x686D</span><span class="sxs-lookup"><span data-stu-id="52da1-109">0x686D</span></span>  <br/> |
|<span data-ttu-id="52da1-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="52da1-110">Data type:</span></span>  <br/> |<span data-ttu-id="52da1-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="52da1-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="52da1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="52da1-112">Area:</span></span>  <br/> |<span data-ttu-id="52da1-113">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="52da1-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52da1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52da1-114">Remarks</span></span>

<span data-ttu-id="52da1-115">Al responder, la respuesta debe ser de aceptación, a menos que se cumplen las propiedades **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) o **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="52da1-115">When responding, the response must be acceptance, unless for an additional constraint that is specified by the **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) or **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) properties is met.</span></span> <span data-ttu-id="52da1-116">Un valor FALSE o la ausencia de esta propiedad indica que un cliente o servidor no debe aceptar automáticamente las solicitudes de reunión.</span><span class="sxs-lookup"><span data-stu-id="52da1-116">A value of FALSE or the absence of this property indicates that a client or server must not automatically accept meeting requests.</span></span> <span data-ttu-id="52da1-117">Esta propiedad no es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="52da1-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="52da1-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="52da1-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="52da1-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="52da1-119">Protocol specifications</span></span>

<span data-ttu-id="52da1-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52da1-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52da1-121">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="52da1-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="52da1-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52da1-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52da1-123">Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.</span><span class="sxs-lookup"><span data-stu-id="52da1-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="52da1-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52da1-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52da1-125">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="52da1-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="52da1-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="52da1-126">Header files</span></span>

<span data-ttu-id="52da1-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="52da1-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="52da1-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="52da1-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="52da1-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="52da1-129">Mapitags.h</span></span>
  
> <span data-ttu-id="52da1-130">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="52da1-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52da1-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="52da1-131">See also</span></span>



[<span data-ttu-id="52da1-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="52da1-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="52da1-133">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="52da1-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="52da1-134">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="52da1-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="52da1-135">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="52da1-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

