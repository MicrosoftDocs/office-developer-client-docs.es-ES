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
ms.openlocfilehash: 78749a61bcbac64ded2c4791d9e239a12c38ce81
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579049"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a><span data-ttu-id="19e41-103">Propiedad canónica PidLidAppointmentSubType</span><span class="sxs-lookup"><span data-stu-id="19e41-103">PidLidAppointmentSubType Canonical Property</span></span>

  
  
<span data-ttu-id="19e41-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19e41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19e41-105">Especifica si está o no el evento todo el día.</span><span class="sxs-lookup"><span data-stu-id="19e41-105">Specifies whether or not the event is all day.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="19e41-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="19e41-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="19e41-107">dispidApptSubType</span><span class="sxs-lookup"><span data-stu-id="19e41-107">dispidApptSubType</span></span>  <br/> |
|<span data-ttu-id="19e41-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="19e41-108">Property set:</span></span>  <br/> |<span data-ttu-id="19e41-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="19e41-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="19e41-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="19e41-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="19e41-111">0x00008215</span><span class="sxs-lookup"><span data-stu-id="19e41-111">0x00008215</span></span>  <br/> |
|<span data-ttu-id="19e41-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="19e41-112">Data type:</span></span>  <br/> |<span data-ttu-id="19e41-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="19e41-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="19e41-114">Área:</span><span class="sxs-lookup"><span data-stu-id="19e41-114">Area:</span></span>  <br/> |<span data-ttu-id="19e41-115">Calendario</span><span class="sxs-lookup"><span data-stu-id="19e41-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19e41-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="19e41-116">Remarks</span></span>

<span data-ttu-id="19e41-117">Esta propiedad especifica si el evento es un evento de día completo, tal como se especifica por el usuario.</span><span class="sxs-lookup"><span data-stu-id="19e41-117">This property specifies whether or not the event is an all-day event, as specified by the user.</span></span> <span data-ttu-id="19e41-118">Un valor de TRUE indica que el evento es un evento de día completo, en cuyo caso la hora de inicio y hora de finalización deben ser medianoche para que la duración es un múltiplo de 24 horas y es de al menos 24 horas.</span><span class="sxs-lookup"><span data-stu-id="19e41-118">A value of TRUE indicates that the event is an all-day event, in which case the start time and end time must be midnight so that the duration is a multiple of 24 hours and is at least 24 hours.</span></span> <span data-ttu-id="19e41-119">Un valor de FALSE o la ausencia de esta propiedad indica que el evento no es un evento de día completo.</span><span class="sxs-lookup"><span data-stu-id="19e41-119">A value of FALSE or the absence of this property indicates the event is not an all-day event.</span></span> <span data-ttu-id="19e41-120">El cliente o el servidor no debe inferir el valor como TRUE cuando ocurre un usuario crear un evento que es de 24 horas, incluso si el evento se inicia y termina en la medianoche.</span><span class="sxs-lookup"><span data-stu-id="19e41-120">The client or server must not infer the value as TRUE when a user happens to create an event that is 24 hours, even if the event starts and ends at midnight.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="19e41-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="19e41-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="19e41-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="19e41-122">Protocol specifications</span></span>

<span data-ttu-id="19e41-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19e41-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19e41-124">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="19e41-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="19e41-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19e41-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19e41-126">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="19e41-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="19e41-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="19e41-127">Header files</span></span>

<span data-ttu-id="19e41-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="19e41-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="19e41-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="19e41-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19e41-130">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="19e41-130">See also</span></span>



[<span data-ttu-id="19e41-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="19e41-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="19e41-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="19e41-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="19e41-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="19e41-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="19e41-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="19e41-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

