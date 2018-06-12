---
title: Propiedad canónico PidTagScheduleInfoAutoAcceptAppointments
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 4f2cab31d6eed19a262bd0e667166bc79f428877
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820202"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a><span data-ttu-id="05737-103">Propiedad canónico PidTagScheduleInfoAutoAcceptAppointments</span><span class="sxs-lookup"><span data-stu-id="05737-103">PidTagScheduleInfoAutoAcceptAppointments Canonical Property</span></span>

  
  
<span data-ttu-id="05737-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="05737-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="05737-105">Contiene TRUE si un cliente o servidor debe responder automáticamente a todas las solicitudes de reunión para el asistente o un recurso.</span><span class="sxs-lookup"><span data-stu-id="05737-105">Contains TRUE if a client or server should automatically respond to all meeting requests for the attendee or resource.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="05737-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="05737-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="05737-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span><span class="sxs-lookup"><span data-stu-id="05737-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span></span>  <br/> |
|<span data-ttu-id="05737-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="05737-108">Identifier:</span></span>  <br/> |<span data-ttu-id="05737-109">0x686D</span><span class="sxs-lookup"><span data-stu-id="05737-109">0x686D</span></span>  <br/> |
|<span data-ttu-id="05737-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="05737-110">Data type:</span></span>  <br/> |<span data-ttu-id="05737-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="05737-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="05737-112">Área:</span><span class="sxs-lookup"><span data-stu-id="05737-112">Area:</span></span>  <br/> |<span data-ttu-id="05737-113">Libre/ocupado</span><span class="sxs-lookup"><span data-stu-id="05737-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05737-114">Notas</span><span class="sxs-lookup"><span data-stu-id="05737-114">Remarks</span></span>

<span data-ttu-id="05737-115">Al responder, la respuesta debe ser la aceptación, a menos que para una restricción adicional se especifica mediante la **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) o **PR_SCHDINFO_DISALLOW_ OVERLAPPING_APPTS** se cumple las propiedades ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="05737-115">When responding, the response must be acceptance, unless for an additional constraint that is specified by the **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) or **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) properties is met.</span></span> <span data-ttu-id="05737-116">Un valor de FALSE o la ausencia de esta propiedad indica que un cliente o servidor debe no aceptar automáticamente las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="05737-116">A value of FALSE or the absence of this property indicates that a client or server must not automatically accept meeting requests.</span></span> <span data-ttu-id="05737-117">No es una propiedad necesaria.</span><span class="sxs-lookup"><span data-stu-id="05737-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="05737-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="05737-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="05737-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="05737-119">Protocol specifications</span></span>

<span data-ttu-id="05737-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05737-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05737-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="05737-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="05737-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05737-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05737-123">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="05737-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="05737-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05737-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05737-125">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="05737-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="05737-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="05737-126">Header files</span></span>

<span data-ttu-id="05737-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05737-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="05737-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="05737-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="05737-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="05737-129">Mapitags.h</span></span>
  
> <span data-ttu-id="05737-130">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="05737-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="05737-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="05737-131">See also</span></span>



[<span data-ttu-id="05737-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="05737-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="05737-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="05737-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="05737-134">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="05737-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="05737-135">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="05737-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

