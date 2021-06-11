---
title: Propiedad canónica PidLidAppointmentRecur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentRecur
api_type:
- COM
ms.assetid: 56d6240f-d07b-48d1-aef0-bf57078ea6c3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: de50616664048af6b931a09df7c65461e9ee3399
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331783"
---
# <a name="pidlidappointmentrecur-canonical-property"></a><span data-ttu-id="029ce-103">Propiedad canónica PidLidAppointmentRecur</span><span class="sxs-lookup"><span data-stu-id="029ce-103">PidLidAppointmentRecur Canonical Property</span></span>

  
  
<span data-ttu-id="029ce-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="029ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="029ce-105">Especifica las fechas y las horas en las que se produce una serie periódica mediante uno de los patrones e intervalos de periodicidad especificados en [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="029ce-105">Specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges that are specified in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="029ce-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="029ce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="029ce-107">dispidApptRecur</span><span class="sxs-lookup"><span data-stu-id="029ce-107">dispidApptRecur</span></span>  <br/> |
|<span data-ttu-id="029ce-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="029ce-108">Property set:</span></span>  <br/> |<span data-ttu-id="029ce-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="029ce-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="029ce-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="029ce-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="029ce-111">0x00008216</span><span class="sxs-lookup"><span data-stu-id="029ce-111">0x00008216</span></span>  <br/> |
|<span data-ttu-id="029ce-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="029ce-112">Data type:</span></span>  <br/> |<span data-ttu-id="029ce-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="029ce-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="029ce-114">Área:</span><span class="sxs-lookup"><span data-stu-id="029ce-114">Area:</span></span>  <br/> |<span data-ttu-id="029ce-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="029ce-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="029ce-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="029ce-116">Remarks</span></span>

<span data-ttu-id="029ce-117">Esta propiedad especifica las fechas y horas en las que se produce una serie periódica mediante uno de los patrones y intervalos de periodicidad detallados en [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="029ce-117">This property specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges detailed in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span> <span data-ttu-id="029ce-118">El valor de esta propiedad también contiene información sobre las excepciones modificadas y eliminadas; información como fechas, asunto, ubicación y varias otras propiedades de excepciones.</span><span class="sxs-lookup"><span data-stu-id="029ce-118">The value of this property also contains information about both modified and deleted exceptions; information such as dates, subject, location, and several other properties of exceptions.</span></span> <span data-ttu-id="029ce-119">Los datos binarios de esta propiedad para elementos de calendario periódicos se almacenan como **la estructura AppointmentRecurrencePattern.**</span><span class="sxs-lookup"><span data-stu-id="029ce-119">The binary data in this property for recurring calendar items is stored as the **AppointmentRecurrencePattern** structure.</span></span> <span data-ttu-id="029ce-120">Esta propiedad no debe existir en elementos de calendario de una sola instancia.</span><span class="sxs-lookup"><span data-stu-id="029ce-120">This property must not exist on single instance calendar items.</span></span> 
  
<span data-ttu-id="029ce-121">Hay algunas limitaciones a las periodicidades:</span><span class="sxs-lookup"><span data-stu-id="029ce-121">There are some limitations to recurrences:</span></span>
  
- <span data-ttu-id="029ce-122">Varias instancias no deben iniciarse el mismo día.</span><span class="sxs-lookup"><span data-stu-id="029ce-122">Multiple instances must not start on the same day.</span></span>
    
- <span data-ttu-id="029ce-123">Las repeticiones no deben superponerse.</span><span class="sxs-lookup"><span data-stu-id="029ce-123">Occurrences must not overlap.</span></span> <span data-ttu-id="029ce-124">En concreto, una excepción que modifica la fecha de inicio de una instancia de la serie periódica debe producirse en una fecha posterior al final de la instancia anterior y al inicio de la siguiente instancia de la serie periódica.</span><span class="sxs-lookup"><span data-stu-id="029ce-124">Specifically, an exception that modifies the start date of an instance in the recurring series must occur on a date that is after the end of the prior instance and the start of the next instance in the recurring series.</span></span> <span data-ttu-id="029ce-125">Lo mismo sucede si las instancias anteriores o siguientes de la serie periódica son excepciones.</span><span class="sxs-lookup"><span data-stu-id="029ce-125">The same is true if the prior or next instances in the recurring series are exceptions.</span></span>
    
<span data-ttu-id="029ce-126">La programación de una serie periódica viene determinada por su patrón de periodicidad y su intervalo.</span><span class="sxs-lookup"><span data-stu-id="029ce-126">The schedule of a recurring series is determined by its recurrence pattern and range.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="029ce-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="029ce-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="029ce-128">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="029ce-128">Protocol specifications</span></span>

<span data-ttu-id="029ce-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="029ce-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="029ce-130">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="029ce-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="029ce-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="029ce-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="029ce-132">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="029ce-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="029ce-133">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="029ce-133">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="029ce-134">Especifica las propiedades y el modelo de interacción para el correo electrónico y otros avisos de objetos.</span><span class="sxs-lookup"><span data-stu-id="029ce-134">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="029ce-135">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="029ce-135">Header files</span></span>

<span data-ttu-id="029ce-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="029ce-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="029ce-137">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="029ce-137">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="029ce-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="029ce-138">See also</span></span>



[<span data-ttu-id="029ce-139">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="029ce-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="029ce-140">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="029ce-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="029ce-141">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="029ce-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="029ce-142">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="029ce-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

