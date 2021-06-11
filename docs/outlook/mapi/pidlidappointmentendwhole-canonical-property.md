---
title: Propiedad canónica PidLidAppointmentEndWhole
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: eaff90de919c1bdc04983bce32a2aa808ae56013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358901"
---
# <a name="pidlidappointmentendwhole-canonical-property"></a><span data-ttu-id="e81a4-103">Propiedad canónica PidLidAppointmentEndWhole</span><span class="sxs-lookup"><span data-stu-id="e81a4-103">PidLidAppointmentEndWhole Canonical Property</span></span>

  
  
<span data-ttu-id="e81a4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e81a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e81a4-105">Representa la fecha y hora en que finaliza una cita.</span><span class="sxs-lookup"><span data-stu-id="e81a4-105">Represents the date and time that an appointment ends.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e81a4-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e81a4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e81a4-107">dispidApptEndWhole</span><span class="sxs-lookup"><span data-stu-id="e81a4-107">dispidApptEndWhole</span></span>  <br/> |
|<span data-ttu-id="e81a4-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="e81a4-108">Property set:</span></span>  <br/> |<span data-ttu-id="e81a4-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="e81a4-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="e81a4-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="e81a4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e81a4-111">0x0000820E</span><span class="sxs-lookup"><span data-stu-id="e81a4-111">0x0000820E</span></span>  <br/> |
|<span data-ttu-id="e81a4-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e81a4-112">Data type:</span></span>  <br/> |<span data-ttu-id="e81a4-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e81a4-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e81a4-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e81a4-114">Area:</span></span>  <br/> |<span data-ttu-id="e81a4-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="e81a4-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e81a4-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e81a4-116">Remarks</span></span>

<span data-ttu-id="e81a4-117">Esta propiedad corresponde a la **propiedad dispidApptEndWhole** de la cita en el Microsoft Office Outlook de objetos.</span><span class="sxs-lookup"><span data-stu-id="e81a4-117">This property corresponds to the **dispidApptEndWhole** property of the appointment in the Microsoft Office Outlook object model.</span></span> 
  
<span data-ttu-id="e81a4-118">Especifica la fecha y hora de finalización del evento; debe estar en hora universal coordinada (UTC) y debe ser mayor que el valor de la propiedad **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e81a4-118">This specifies the end date and time for the event; it must be in Coordinated Universal Time (UTC) and must be greater than the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="e81a4-119">Para una serie periódica, la propiedad **dispidApptEndWhole** es la fecha y hora de finalización de la primera instancia según el patrón de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="e81a4-119">For a recurring series, the **dispidApptEndWhole** property is the end date and time of the first instance according to the recurrence pattern.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e81a4-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e81a4-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e81a4-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="e81a4-121">Protocol specifications</span></span>

<span data-ttu-id="e81a4-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e81a4-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e81a4-123">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="e81a4-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e81a4-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e81a4-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e81a4-125">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="e81a4-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e81a4-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e81a4-126">Header files</span></span>

<span data-ttu-id="e81a4-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e81a4-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="e81a4-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e81a4-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e81a4-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e81a4-129">See also</span></span>



[<span data-ttu-id="e81a4-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e81a4-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e81a4-131">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e81a4-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e81a4-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e81a4-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e81a4-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="e81a4-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

