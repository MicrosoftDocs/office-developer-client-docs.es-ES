---
title: Propiedad canónico PidLidAppointmentEndWhole
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentEndWhole
api_type:
- COM
ms.assetid: f6fd33d6-04fb-4801-a004-fb80a14ca79d
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 155300d3c3043713ce2197d3b70843c589d777e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818481"
---
# <a name="pidlidappointmentendwhole-canonical-property"></a><span data-ttu-id="8e9c5-103">Propiedad canónico PidLidAppointmentEndWhole</span><span class="sxs-lookup"><span data-stu-id="8e9c5-103">PidLidAppointmentEndWhole Canonical Property</span></span>

  
  
<span data-ttu-id="8e9c5-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e9c5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8e9c5-105">Representa la fecha y hora en que finaliza una cita.</span><span class="sxs-lookup"><span data-stu-id="8e9c5-105">Represents the date and time that an appointment ends.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e9c5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8e9c5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e9c5-107">dispidApptEndWhole</span><span class="sxs-lookup"><span data-stu-id="8e9c5-107">dispidApptEndWhole</span></span>  <br/> |
|<span data-ttu-id="8e9c5-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="8e9c5-108">Property set:</span></span>  <br/> |<span data-ttu-id="8e9c5-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="8e9c5-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="8e9c5-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="8e9c5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8e9c5-111">0x0000820E</span><span class="sxs-lookup"><span data-stu-id="8e9c5-111">0x0000820E</span></span>  <br/> |
|<span data-ttu-id="8e9c5-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8e9c5-112">Data type:</span></span>  <br/> |<span data-ttu-id="8e9c5-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="8e9c5-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="8e9c5-114">Área:</span><span class="sxs-lookup"><span data-stu-id="8e9c5-114">Area:</span></span>  <br/> |<span data-ttu-id="8e9c5-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="8e9c5-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e9c5-116">Notas</span><span class="sxs-lookup"><span data-stu-id="8e9c5-116">Remarks</span></span>

<span data-ttu-id="8e9c5-117">Esta propiedad corresponde a la propiedad **dispidApptEndWhole** de la cita en el modelo de objetos de Microsoft Office Outlook.</span><span class="sxs-lookup"><span data-stu-id="8e9c5-117">This property corresponds to the **dispidApptEndWhole** property of the appointment in the Microsoft Office Outlook object model.</span></span> 
  
<span data-ttu-id="8e9c5-118">Especifica la fecha de finalización y la hora para el evento; debe ser en hora Universal coordinada (UTC) y debe ser mayor que el valor de la propiedad **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8e9c5-118">This specifies the end date and time for the event; it must be in Coordinated Universal Time (UTC) and must be greater than the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="8e9c5-119">Para una serie periódica, la propiedad **dispidApptEndWhole** es la fecha de finalización y la hora de la primera instancia según el patrón de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="8e9c5-119">For a recurring series, the **dispidApptEndWhole** property is the end date and time of the first instance according to the recurrence pattern.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8e9c5-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e9c5-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8e9c5-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="8e9c5-121">Protocol specifications</span></span>

<span data-ttu-id="8e9c5-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e9c5-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e9c5-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8e9c5-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8e9c5-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e9c5-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e9c5-125">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8e9c5-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8e9c5-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8e9c5-126">Header files</span></span>

<span data-ttu-id="8e9c5-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e9c5-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e9c5-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8e9c5-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e9c5-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="8e9c5-129">See also</span></span>



[<span data-ttu-id="8e9c5-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8e9c5-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e9c5-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="8e9c5-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e9c5-132">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="8e9c5-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e9c5-133">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="8e9c5-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

