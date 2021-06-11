---
title: Propiedad canónica PidLidAppointmentSubType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentSubType
api_type:
- COM
ms.assetid: e2e00af3-1fb3-4314-936a-f480674d3d83
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 921d7d8defbdae66bc48072d757f4f58b7d656f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345419"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a><span data-ttu-id="0cb47-103">Propiedad canónica PidLidAppointmentSubType</span><span class="sxs-lookup"><span data-stu-id="0cb47-103">PidLidAppointmentSubType Canonical Property</span></span>

  
  
<span data-ttu-id="0cb47-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0cb47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0cb47-105">Especifica si el evento es todo el día.</span><span class="sxs-lookup"><span data-stu-id="0cb47-105">Specifies whether or not the event is all day.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0cb47-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0cb47-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0cb47-107">dispidApptSubType</span><span class="sxs-lookup"><span data-stu-id="0cb47-107">dispidApptSubType</span></span>  <br/> |
|<span data-ttu-id="0cb47-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="0cb47-108">Property set:</span></span>  <br/> |<span data-ttu-id="0cb47-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="0cb47-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="0cb47-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="0cb47-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0cb47-111">0x00008215</span><span class="sxs-lookup"><span data-stu-id="0cb47-111">0x00008215</span></span>  <br/> |
|<span data-ttu-id="0cb47-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0cb47-112">Data type:</span></span>  <br/> |<span data-ttu-id="0cb47-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0cb47-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0cb47-114">Área:</span><span class="sxs-lookup"><span data-stu-id="0cb47-114">Area:</span></span>  <br/> |<span data-ttu-id="0cb47-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="0cb47-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0cb47-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0cb47-116">Remarks</span></span>

<span data-ttu-id="0cb47-117">Esta propiedad especifica si el evento es un evento de todo el día, según lo especificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="0cb47-117">This property specifies whether or not the event is an all-day event, as specified by the user.</span></span> <span data-ttu-id="0cb47-118">Un valor de TRUE indica que el evento es un evento de todo el día, en cuyo caso la hora de inicio y la hora de finalización deben ser medianoche, de modo que la duración sea de un múltiplo de 24 horas y de al menos 24 horas.</span><span class="sxs-lookup"><span data-stu-id="0cb47-118">A value of TRUE indicates that the event is an all-day event, in which case the start time and end time must be midnight so that the duration is a multiple of 24 hours and is at least 24 hours.</span></span> <span data-ttu-id="0cb47-119">Un valor de FALSE o la ausencia de esta propiedad indica que el evento no es un evento de todo el día.</span><span class="sxs-lookup"><span data-stu-id="0cb47-119">A value of FALSE or the absence of this property indicates the event is not an all-day event.</span></span> <span data-ttu-id="0cb47-120">El cliente o el servidor no deben inferir el valor como TRUE cuando un usuario crea un evento de 24 horas, incluso si el evento se inicia y finaliza a medianoche.</span><span class="sxs-lookup"><span data-stu-id="0cb47-120">The client or server must not infer the value as TRUE when a user happens to create an event that is 24 hours, even if the event starts and ends at midnight.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0cb47-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0cb47-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0cb47-122">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="0cb47-122">Protocol specifications</span></span>

<span data-ttu-id="0cb47-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0cb47-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0cb47-124">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="0cb47-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0cb47-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0cb47-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0cb47-126">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="0cb47-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0cb47-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0cb47-127">Header files</span></span>

<span data-ttu-id="0cb47-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0cb47-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="0cb47-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0cb47-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0cb47-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cb47-130">See also</span></span>



[<span data-ttu-id="0cb47-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0cb47-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0cb47-132">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="0cb47-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0cb47-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0cb47-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0cb47-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="0cb47-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

