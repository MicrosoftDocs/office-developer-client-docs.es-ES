---
title: Propiedad canónico PidTagScheduleInfoDisallowOverlappingAppts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowOverlappingAppts
api_type:
- COM
ms.assetid: 27978a09-daf7-4a50-927a-96d9c4a97d02
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 3719c0d86b0f14324e65b963d2a81a27f6cd52ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820211"
---
# <a name="pidtagscheduleinfodisallowoverlappingappts-canonical-property"></a><span data-ttu-id="e9785-103">Propiedad canónico PidTagScheduleInfoDisallowOverlappingAppts</span><span class="sxs-lookup"><span data-stu-id="e9785-103">PidTagScheduleInfoDisallowOverlappingAppts Canonical Property</span></span>

  
  
<span data-ttu-id="e9785-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9785-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9785-105">Contiene TRUE si no se permiten citas superpuestas.</span><span class="sxs-lookup"><span data-stu-id="e9785-105">Contains TRUE if overlapping appointments are disallowed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e9785-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e9785-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9785-107">PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS</span><span class="sxs-lookup"><span data-stu-id="e9785-107">PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS</span></span>  <br/> |
|<span data-ttu-id="e9785-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e9785-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e9785-109">0x686F</span><span class="sxs-lookup"><span data-stu-id="e9785-109">0x686F</span></span>  <br/> |
|<span data-ttu-id="e9785-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e9785-110">Data type:</span></span>  <br/> |<span data-ttu-id="e9785-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e9785-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e9785-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e9785-112">Area:</span></span>  <br/> |<span data-ttu-id="e9785-113">Libre/ocupado</span><span class="sxs-lookup"><span data-stu-id="e9785-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9785-114">Notas</span><span class="sxs-lookup"><span data-stu-id="e9785-114">Remarks</span></span>

<span data-ttu-id="e9785-115">Esta propiedad sólo es significativa cuando el valor de la propiedad **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) es TRUE.</span><span class="sxs-lookup"><span data-stu-id="e9785-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="e9785-116">Un valor de TRUE indica que cuando se responde automáticamente a las convocatorias de reunión, un cliente o servidor debe rechazar instancias que se superponen eventos previamente programados.</span><span class="sxs-lookup"><span data-stu-id="e9785-116">A value of TRUE indicates that when automatically responding to meeting requests, a client or server must decline instances that overlap previously scheduled events.</span></span> <span data-ttu-id="e9785-117">Un valor de FALSE o la ausencia de esta propiedad indica que se deben aceptar superpuestas instancias.</span><span class="sxs-lookup"><span data-stu-id="e9785-117">A value of FALSE or the absence of this property indicates that overlapping instances must be accepted.</span></span> <span data-ttu-id="e9785-118">No es una propiedad necesaria.</span><span class="sxs-lookup"><span data-stu-id="e9785-118">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e9785-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e9785-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e9785-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e9785-120">Protocol specifications</span></span>

<span data-ttu-id="e9785-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9785-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9785-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e9785-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e9785-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9785-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9785-124">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9785-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="e9785-125">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9785-125">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9785-126">Publica la disponibilidad de un usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="e9785-126">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e9785-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e9785-127">Header files</span></span>

<span data-ttu-id="e9785-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9785-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9785-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e9785-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="e9785-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e9785-130">Mapitags.h</span></span>
  
> <span data-ttu-id="e9785-131">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="e9785-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9785-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="e9785-132">See also</span></span>



[<span data-ttu-id="e9785-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e9785-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9785-134">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e9785-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9785-135">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="e9785-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9785-136">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e9785-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

