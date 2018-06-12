---
title: Propiedad canónico PidLidAppointmentRecur
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 815b4f60adb65791cdd4c7d7d00a0cfc7d9e3fdf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818520"
---
# <a name="pidlidappointmentrecur-canonical-property"></a><span data-ttu-id="cf724-103">Propiedad canónico PidLidAppointmentRecur</span><span class="sxs-lookup"><span data-stu-id="cf724-103">PidLidAppointmentRecur Canonical Property</span></span>

  
  
<span data-ttu-id="cf724-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cf724-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cf724-105">Especifica las fechas y horas cuando se produce una serie periódica mediante uno de los patrones de periodicidad y los intervalos que se especifican en [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="cf724-105">Specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges that are specified in [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cf724-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cf724-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cf724-107">dispidApptRecur</span><span class="sxs-lookup"><span data-stu-id="cf724-107">dispidApptRecur</span></span>  <br/> |
|<span data-ttu-id="cf724-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="cf724-108">Property set:</span></span>  <br/> |<span data-ttu-id="cf724-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="cf724-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="cf724-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="cf724-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cf724-111">0x00008216</span><span class="sxs-lookup"><span data-stu-id="cf724-111">0x00008216</span></span>  <br/> |
|<span data-ttu-id="cf724-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="cf724-112">Data type:</span></span>  <br/> |<span data-ttu-id="cf724-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cf724-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cf724-114">Área:</span><span class="sxs-lookup"><span data-stu-id="cf724-114">Area:</span></span>  <br/> |<span data-ttu-id="cf724-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="cf724-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf724-116">Notas</span><span class="sxs-lookup"><span data-stu-id="cf724-116">Remarks</span></span>

<span data-ttu-id="cf724-117">Esta propiedad especifica las fechas y horas cuando una serie periódica se produce mediante uno de los patrones de periodicidad y rangos detalla en [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="cf724-117">This property specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges detailed in [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span> <span data-ttu-id="cf724-118">El valor de esta propiedad también contiene información sobre las excepciones modificadas y eliminadas; información como las fechas, asunto, ubicación y otras propiedades de excepciones.</span><span class="sxs-lookup"><span data-stu-id="cf724-118">The value of this property also contains information about both modified and deleted exceptions; information such as dates, subject, location, and several other properties of exceptions.</span></span> <span data-ttu-id="cf724-119">Los datos binarios en esta propiedad para los elementos de calendario periódicos se almacenan como la estructura de **AppointmentRecurrencePattern** .</span><span class="sxs-lookup"><span data-stu-id="cf724-119">The binary data in this property for recurring calendar items is stored as the **AppointmentRecurrencePattern** structure.</span></span> <span data-ttu-id="cf724-120">Esta propiedad no debe existir en los elementos de calendario de una sola instancia.</span><span class="sxs-lookup"><span data-stu-id="cf724-120">This property must not exist on single instance calendar items.</span></span> 
  
<span data-ttu-id="cf724-121">Existen algunas limitaciones para las repeticiones:</span><span class="sxs-lookup"><span data-stu-id="cf724-121">There are some limitations to recurrences:</span></span>
  
- <span data-ttu-id="cf724-122">No deben iniciar varias instancias en el mismo día.</span><span class="sxs-lookup"><span data-stu-id="cf724-122">Multiple instances must not start on the same day.</span></span>
    
- <span data-ttu-id="cf724-123">No deben superponerse repeticiones.</span><span class="sxs-lookup"><span data-stu-id="cf724-123">Occurrences must not overlap.</span></span> <span data-ttu-id="cf724-124">En concreto, debe producir una excepción que modifica la fecha de inicio de una instancia de la serie periódica en una fecha que se encuentra después del final de la instancia anterior y el inicio de la siguiente aparición de la serie periódica.</span><span class="sxs-lookup"><span data-stu-id="cf724-124">Specifically, an exception that modifies the start date of an instance in the recurring series must occur on a date that is after the end of the prior instance and the start of the next instance in the recurring series.</span></span> <span data-ttu-id="cf724-125">El mismo es true si las instancias anteriores o siguiente de la serie periódica son excepciones.</span><span class="sxs-lookup"><span data-stu-id="cf724-125">The same is true if the prior or next instances in the recurring series are exceptions.</span></span>
    
<span data-ttu-id="cf724-126">La programación de una serie periódica está determinada por su patrón de periodicidad y el intervalo.</span><span class="sxs-lookup"><span data-stu-id="cf724-126">The schedule of a recurring series is determined by its recurrence pattern and range.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cf724-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cf724-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cf724-128">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="cf724-128">Protocol specifications</span></span>

<span data-ttu-id="cf724-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf724-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf724-130">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="cf724-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cf724-131">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf724-131">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf724-132">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf724-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="cf724-133">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf724-133">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf724-134">Especifica las propiedades y el modelo de interacción para correo electrónico y otros avisos de objeto.</span><span class="sxs-lookup"><span data-stu-id="cf724-134">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cf724-135">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cf724-135">Header files</span></span>

<span data-ttu-id="cf724-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cf724-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="cf724-137">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cf724-137">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cf724-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="cf724-138">See also</span></span>



[<span data-ttu-id="cf724-139">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cf724-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cf724-140">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="cf724-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cf724-141">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="cf724-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cf724-142">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="cf724-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

