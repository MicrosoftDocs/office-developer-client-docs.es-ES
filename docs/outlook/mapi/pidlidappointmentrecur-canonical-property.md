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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393372"
---
# <a name="pidlidappointmentrecur-canonical-property"></a><span data-ttu-id="ace98-103">Propiedad canónica PidLidAppointmentRecur</span><span class="sxs-lookup"><span data-stu-id="ace98-103">PidLidAppointmentRecur Canonical Property</span></span>

  
  
<span data-ttu-id="ace98-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ace98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ace98-105">Especifica las fechas y horas cuando se produce una serie periódica mediante uno de los patrones de periodicidad y los intervalos que se especifican en [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ace98-105">Specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges that are specified in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ace98-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ace98-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ace98-107">dispidApptRecur</span><span class="sxs-lookup"><span data-stu-id="ace98-107">dispidApptRecur</span></span>  <br/> |
|<span data-ttu-id="ace98-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="ace98-108">Property set:</span></span>  <br/> |<span data-ttu-id="ace98-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="ace98-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="ace98-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="ace98-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ace98-111">0x00008216</span><span class="sxs-lookup"><span data-stu-id="ace98-111">0x00008216</span></span>  <br/> |
|<span data-ttu-id="ace98-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ace98-112">Data type:</span></span>  <br/> |<span data-ttu-id="ace98-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ace98-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ace98-114">Área:</span><span class="sxs-lookup"><span data-stu-id="ace98-114">Area:</span></span>  <br/> |<span data-ttu-id="ace98-115">Calendario</span><span class="sxs-lookup"><span data-stu-id="ace98-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ace98-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ace98-116">Remarks</span></span>

<span data-ttu-id="ace98-117">Esta propiedad especifica las fechas y horas cuando una serie periódica se produce mediante uno de los patrones de periodicidad y rangos detalla en [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ace98-117">This property specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges detailed in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span> <span data-ttu-id="ace98-118">El valor de esta propiedad también contiene información sobre las excepciones modificadas y eliminadas; información como las fechas, asunto, ubicación y otras propiedades de excepciones.</span><span class="sxs-lookup"><span data-stu-id="ace98-118">The value of this property also contains information about both modified and deleted exceptions; information such as dates, subject, location, and several other properties of exceptions.</span></span> <span data-ttu-id="ace98-119">Los datos binarios en esta propiedad para los elementos de calendario periódicos se almacenan como la estructura de **AppointmentRecurrencePattern** .</span><span class="sxs-lookup"><span data-stu-id="ace98-119">The binary data in this property for recurring calendar items is stored as the **AppointmentRecurrencePattern** structure.</span></span> <span data-ttu-id="ace98-120">Esta propiedad no debe existir en los elementos de calendario de una sola instancia.</span><span class="sxs-lookup"><span data-stu-id="ace98-120">This property must not exist on single instance calendar items.</span></span> 
  
<span data-ttu-id="ace98-121">Existen algunas limitaciones para las repeticiones:</span><span class="sxs-lookup"><span data-stu-id="ace98-121">There are some limitations to recurrences:</span></span>
  
- <span data-ttu-id="ace98-122">No deben iniciar varias instancias en el mismo día.</span><span class="sxs-lookup"><span data-stu-id="ace98-122">Multiple instances must not start on the same day.</span></span>
    
- <span data-ttu-id="ace98-123">No deben superponerse repeticiones.</span><span class="sxs-lookup"><span data-stu-id="ace98-123">Occurrences must not overlap.</span></span> <span data-ttu-id="ace98-124">En concreto, debe producir una excepción que modifica la fecha de inicio de una instancia de la serie periódica en una fecha que se encuentra después del final de la instancia anterior y el inicio de la siguiente aparición de la serie periódica.</span><span class="sxs-lookup"><span data-stu-id="ace98-124">Specifically, an exception that modifies the start date of an instance in the recurring series must occur on a date that is after the end of the prior instance and the start of the next instance in the recurring series.</span></span> <span data-ttu-id="ace98-125">El mismo es true si las instancias anteriores o siguiente de la serie periódica son excepciones.</span><span class="sxs-lookup"><span data-stu-id="ace98-125">The same is true if the prior or next instances in the recurring series are exceptions.</span></span>
    
<span data-ttu-id="ace98-126">La programación de una serie periódica está determinada por su patrón de periodicidad y el intervalo.</span><span class="sxs-lookup"><span data-stu-id="ace98-126">The schedule of a recurring series is determined by its recurrence pattern and range.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ace98-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ace98-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ace98-128">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="ace98-128">Protocol specifications</span></span>

<span data-ttu-id="ace98-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ace98-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ace98-130">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ace98-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ace98-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ace98-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ace98-132">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="ace98-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="ace98-133">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ace98-133">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ace98-134">Especifica las propiedades y el modelo de interacción para correo electrónico y otros avisos de objeto.</span><span class="sxs-lookup"><span data-stu-id="ace98-134">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ace98-135">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ace98-135">Header files</span></span>

<span data-ttu-id="ace98-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ace98-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="ace98-137">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ace98-137">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ace98-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="ace98-138">See also</span></span>



[<span data-ttu-id="ace98-139">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ace98-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ace98-140">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="ace98-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ace98-141">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ace98-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ace98-142">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="ace98-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

