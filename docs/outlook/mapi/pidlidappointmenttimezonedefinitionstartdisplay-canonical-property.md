---
title: Propiedad canónica PidLidAppointmentTimeZoneDefinitionStartDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionStartDispl
api_type:
- COM
ms.assetid: 08239670-3211-420c-99d7-0056ed967cb8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 504dc4b1cecb9798590e4a15968acc3aa98fe4a6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399903"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a><span data-ttu-id="87849-103">Propiedad canónica PidLidAppointmentTimeZoneDefinitionStartDisplay</span><span class="sxs-lookup"><span data-stu-id="87849-103">PidLidAppointmentTimeZoneDefinitionStartDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="87849-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87849-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87849-105">Contiene una secuencia que se asigna al formato persistente de una estructura [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , que almacena la descripción de la zona horaria que se usa cuando se selecciona la hora de inicio de una instancia única cita o convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="87849-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the start time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87849-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="87849-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="87849-107">dispidApptTZDefStartDisplay</span><span class="sxs-lookup"><span data-stu-id="87849-107">dispidApptTZDefStartDisplay</span></span>  <br/> |
|<span data-ttu-id="87849-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="87849-108">Property set:</span></span>  <br/> |<span data-ttu-id="87849-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="87849-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="87849-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="87849-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="87849-111">0x0000825E</span><span class="sxs-lookup"><span data-stu-id="87849-111">0x0000825E</span></span>  <br/> |
|<span data-ttu-id="87849-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="87849-112">Data type:</span></span>  <br/> |<span data-ttu-id="87849-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="87849-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="87849-114">Área:</span><span class="sxs-lookup"><span data-stu-id="87849-114">Area:</span></span>  <br/> |<span data-ttu-id="87849-115">Calendario</span><span class="sxs-lookup"><span data-stu-id="87849-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87849-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="87849-116">Remarks</span></span>

<span data-ttu-id="87849-117">Microsoft Office Outlook 2003 o anterior y las soluciones que se basan en Collaboration Data Objects (CDO) 1.2.1 y que no se ejecuta la herramienta de actualización de calendario de Outlook o Microsoft Exchange Server, almacenan la hora de inicio y hora de finalización de instancia única las citas y las convocatorias de reunión en hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="87849-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="87849-118">Estos clientes no almacene ninguna información para la zona horaria en la que se creó la convocatoria de reunión o cita.</span><span class="sxs-lookup"><span data-stu-id="87849-118">These clients do not store any information for the time zone in which the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="87849-119">Las versiones de Outlook con respecto a Microsoft Office Outlook 2007 y soluciones basadas en CDO 1.2.1 que han ejecutado la herramienta de actualización de calendario de Outlook o Exchange Server usan esta propiedad para almacenar la zona horaria de la hora de inicio.</span><span class="sxs-lookup"><span data-stu-id="87849-119">Versions of Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use this property to store the time zone for the start time.</span></span> <span data-ttu-id="87849-120">La propiedad **dispidApptTZDefStartDisplay** muestra la cita o reunión en la zona horaria original que se encontraba programado.</span><span class="sxs-lookup"><span data-stu-id="87849-120">The **dispidApptTZDefStartDisplay** property shows the appointment or meeting in the original time zone that it was scheduled.</span></span> <span data-ttu-id="87849-121">Determina si se debe ajustar la hora de inicio si cambian las reglas de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="87849-121">It determines whether the start time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="87849-122">Si falta esta propiedad, se supone la zona horaria local actual.</span><span class="sxs-lookup"><span data-stu-id="87849-122">If this property is missing, the current local time zone is assumed.</span></span> <span data-ttu-id="87849-123">Esta propiedad se utiliza únicamente con fines de presentación y no se usa en la expansión de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="87849-123">This property is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="87849-124">Un analizador de debe tener cuidado cuando lee una secuencia obtenida de esta propiedad, o cuando conserva **TZDEFINITION** a una secuencia de compromiso a una propiedad binaria, como **dispidApptTZDefStartDisplay**.</span><span class="sxs-lookup"><span data-stu-id="87849-124">A parser must be careful when it reads a stream obtained from this property, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefStartDisplay**.</span></span> <span data-ttu-id="87849-125">Para obtener más información, vea [acerca de la conservación de datos TZDEFINITION a una secuencia de confirmación en una propiedad binaria](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="87849-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="87849-126">Esta propiedad especifica la información de zona horaria de la propiedad **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="87849-126">This property specifies time zone information for the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="87849-127">El valor de **dispidApptTZDefStartDisplay** se usa para convertir la fecha de inicio y la hora de la hora UTC a la zona horaria local para fines de presentación.</span><span class="sxs-lookup"><span data-stu-id="87849-127">The value of **dispidApptTZDefStartDisplay** is used to convert the start date and time from UTC to the local time zone for display purposes.</span></span> <span data-ttu-id="87849-128">Para cada **TZRULE** especificado por esta propiedad, no se debe establecer la marca TZRULE_FLAG_RECUR_CURRENT_TZREG.</span><span class="sxs-lookup"><span data-stu-id="87849-128">For each **TZRULE** specified by this property, the TZRULE_FLAG_RECUR_CURRENT_TZREG flag must not be set.</span></span> <span data-ttu-id="87849-129">Por ejemplo, si la **TZRULE** es la regla eficaz, el valor del campo, **TZRULE** debe ser "0 x 0002"; de lo contrario, debe ser "0 x 0000".</span><span class="sxs-lookup"><span data-stu-id="87849-129">For example, if the **TZRULE** is the effective rule, the value of the field, **TZRULE** must be "0x0002"; otherwise, it must be "0x0000".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="87849-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="87849-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="87849-131">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="87849-131">Protocol specifications</span></span>

<span data-ttu-id="87849-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87849-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87849-133">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones de protocolo relacionadas de Exchange Server..</span><span class="sxs-lookup"><span data-stu-id="87849-133">Provides property set definitions and references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="87849-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87849-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87849-135">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="87849-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="87849-136">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="87849-136">Header files</span></span>

<span data-ttu-id="87849-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="87849-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="87849-138">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="87849-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87849-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="87849-139">See also</span></span>



[<span data-ttu-id="87849-140">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="87849-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="87849-141">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="87849-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="87849-142">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="87849-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="87849-143">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="87849-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

