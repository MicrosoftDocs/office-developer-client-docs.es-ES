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
ms.openlocfilehash: 815b4f60adb65791cdd4c7d7d00a0cfc7d9e3fdf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818520"
---
# <a name="pidlidappointmentrecur-canonical-property"></a><span data-ttu-id="b0230-103">Propiedad canónica PidLidAppointmentRecur</span><span class="sxs-lookup"><span data-stu-id="b0230-103">PidLidAppointmentRecur Canonical Property</span></span>

  
  
<span data-ttu-id="b0230-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b0230-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b0230-105">Especifica las fechas y horas cuando se produce una serie periódica mediante uno de los patrones de periodicidad y los intervalos que se especifican en [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b0230-105">Specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges that are specified in [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b0230-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b0230-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b0230-107">dispidApptRecur</span><span class="sxs-lookup"><span data-stu-id="b0230-107">dispidApptRecur</span></span>  <br/> |
|<span data-ttu-id="b0230-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="b0230-108">Property set:</span></span>  <br/> |<span data-ttu-id="b0230-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="b0230-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="b0230-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="b0230-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b0230-111">0x00008216</span><span class="sxs-lookup"><span data-stu-id="b0230-111">0x00008216</span></span>  <br/> |
|<span data-ttu-id="b0230-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b0230-112">Data type:</span></span>  <br/> |<span data-ttu-id="b0230-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b0230-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b0230-114">Área:</span><span class="sxs-lookup"><span data-stu-id="b0230-114">Area:</span></span>  <br/> |<span data-ttu-id="b0230-115">Calendario</span><span class="sxs-lookup"><span data-stu-id="b0230-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0230-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b0230-116">Remarks</span></span>

<span data-ttu-id="b0230-117">Esta propiedad especifica las fechas y horas cuando una serie periódica se produce mediante uno de los patrones de periodicidad y rangos detalla en [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b0230-117">This property specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges detailed in [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span> <span data-ttu-id="b0230-118">El valor de esta propiedad también contiene información sobre las excepciones modificadas y eliminadas; información como las fechas, asunto, ubicación y otras propiedades de excepciones.</span><span class="sxs-lookup"><span data-stu-id="b0230-118">The value of this property also contains information about both modified and deleted exceptions; information such as dates, subject, location, and several other properties of exceptions.</span></span> <span data-ttu-id="b0230-119">Los datos binarios en esta propiedad para los elementos de calendario periódicos se almacenan como la estructura de **AppointmentRecurrencePattern** .</span><span class="sxs-lookup"><span data-stu-id="b0230-119">The binary data in this property for recurring calendar items is stored as the **AppointmentRecurrencePattern** structure.</span></span> <span data-ttu-id="b0230-120">Esta propiedad no debe existir en los elementos de calendario de una sola instancia.</span><span class="sxs-lookup"><span data-stu-id="b0230-120">This property must not exist on single instance calendar items.</span></span> 
  
<span data-ttu-id="b0230-121">Existen algunas limitaciones para las repeticiones:</span><span class="sxs-lookup"><span data-stu-id="b0230-121">There are some limitations to recurrences:</span></span>
  
- <span data-ttu-id="b0230-122">No deben iniciar varias instancias en el mismo día.</span><span class="sxs-lookup"><span data-stu-id="b0230-122">Multiple instances must not start on the same day.</span></span>
    
- <span data-ttu-id="b0230-123">No deben superponerse repeticiones.</span><span class="sxs-lookup"><span data-stu-id="b0230-123">Occurrences must not overlap.</span></span> <span data-ttu-id="b0230-124">En concreto, debe producir una excepción que modifica la fecha de inicio de una instancia de la serie periódica en una fecha que se encuentra después del final de la instancia anterior y el inicio de la siguiente aparición de la serie periódica.</span><span class="sxs-lookup"><span data-stu-id="b0230-124">Specifically, an exception that modifies the start date of an instance in the recurring series must occur on a date that is after the end of the prior instance and the start of the next instance in the recurring series.</span></span> <span data-ttu-id="b0230-125">El mismo es true si las instancias anteriores o siguiente de la serie periódica son excepciones.</span><span class="sxs-lookup"><span data-stu-id="b0230-125">The same is true if the prior or next instances in the recurring series are exceptions.</span></span>
    
<span data-ttu-id="b0230-126">La programación de una serie periódica está determinada por su patrón de periodicidad y el intervalo.</span><span class="sxs-lookup"><span data-stu-id="b0230-126">The schedule of a recurring series is determined by its recurrence pattern and range.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b0230-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b0230-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b0230-128">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="b0230-128">Protocol specifications</span></span>

<span data-ttu-id="b0230-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0230-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0230-130">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="b0230-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b0230-131">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0230-131">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0230-132">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="b0230-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="b0230-133">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0230-133">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0230-134">Especifica las propiedades y el modelo de interacción para correo electrónico y otros avisos de objeto.</span><span class="sxs-lookup"><span data-stu-id="b0230-134">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b0230-135">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b0230-135">Header files</span></span>

<span data-ttu-id="b0230-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b0230-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="b0230-137">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b0230-137">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0230-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0230-138">See also</span></span>



[<span data-ttu-id="b0230-139">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b0230-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b0230-140">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="b0230-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b0230-141">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b0230-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b0230-142">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="b0230-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

