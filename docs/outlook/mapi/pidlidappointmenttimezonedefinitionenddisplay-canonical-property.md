---
title: Propiedad canónica PidLidAppointmentTimeZoneDefinitionEndDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionEndDisplay
api_type:
- COM
ms.assetid: 7b6193cb-612b-408e-b9bc-285df313e2cc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: facbcb9eed18db304cac334be845c0b3869ba508
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574807"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a><span data-ttu-id="2f3a7-103">Propiedad canónica PidLidAppointmentTimeZoneDefinitionEndDisplay</span><span class="sxs-lookup"><span data-stu-id="2f3a7-103">PidLidAppointmentTimeZoneDefinitionEndDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="2f3a7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f3a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f3a7-105">Contiene una secuencia que se asigna al formato persistente de una estructura [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , que almacena la descripción de la zona horaria que se usa cuando se selecciona la hora de finalización de una instancia única cita o convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="2f3a7-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the end time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f3a7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2f3a7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2f3a7-107">dispidApptTZDefEndDisplay</span><span class="sxs-lookup"><span data-stu-id="2f3a7-107">dispidApptTZDefEndDisplay</span></span>  <br/> |
|<span data-ttu-id="2f3a7-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="2f3a7-108">Property set:</span></span>  <br/> |<span data-ttu-id="2f3a7-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="2f3a7-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="2f3a7-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="2f3a7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2f3a7-111">0x0000825F</span><span class="sxs-lookup"><span data-stu-id="2f3a7-111">0x0000825F</span></span>  <br/> |
|<span data-ttu-id="2f3a7-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2f3a7-112">Data type:</span></span>  <br/> |<span data-ttu-id="2f3a7-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2f3a7-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2f3a7-114">Área:</span><span class="sxs-lookup"><span data-stu-id="2f3a7-114">Area:</span></span>  <br/> |<span data-ttu-id="2f3a7-115">Calendario</span><span class="sxs-lookup"><span data-stu-id="2f3a7-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f3a7-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2f3a7-116">Remarks</span></span>

<span data-ttu-id="2f3a7-117">Microsoft Office Outlook 2003 o anterior y las soluciones que se basan en Collaboration Data Objects (CDO) 1.2.1 y que no se ejecuta la herramienta de actualización de calendario de Outlook o Microsoft Exchange Server, almacenan la hora de inicio y hora de finalización de instancia única las citas y las convocatorias de reunión en hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="2f3a7-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="2f3a7-118">Estos clientes no almacene ninguna información para la zona horaria donde se crea la solicitud de reunión o cita.</span><span class="sxs-lookup"><span data-stu-id="2f3a7-118">These clients do not store any information for the time zone where the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="2f3a7-119">Versiones de Microsoft Outlook desde Microsoft Office Outlook 2007 y soluciones basadas en CDO 1.2.1 que se han ejecutado el calendario de Outlook o Exchange Server la actualización de uso de herramienta **dispidApptTZDefEndDisplay** para almacenar la zona horaria para la hora de finalización.</span><span class="sxs-lookup"><span data-stu-id="2f3a7-119">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use **dispidApptTZDefEndDisplay** to store the time zone for the end time.</span></span> <span data-ttu-id="2f3a7-120">**dispidApptTZDefEndDisplay** muestra la cita o reunión en la zona horaria original que se ha programado y que determina si se debe ajustar la hora de finalización si cambian las reglas de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="2f3a7-120">**dispidApptTZDefEndDisplay** shows the appointment or meeting in the original time zone that it was scheduled, and determines whether the end time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="2f3a7-121">Si falta esta propiedad, se usa la zona horaria especificada por la propiedad **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2f3a7-121">If this property is missing, the time zone specified by the **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) property is used.</span></span> <span data-ttu-id="2f3a7-122">Si **dispidApptTZDefStartDisplay** es falta o no es válida, se supone la zona horaria local actual.</span><span class="sxs-lookup"><span data-stu-id="2f3a7-122">If **dispidApptTZDefStartDisplay** is missing or invalid, the current local time zone is assumed.</span></span> <span data-ttu-id="2f3a7-123">**dispidApptTZDefEndDisplay** se utiliza únicamente con fines de presentación y no se usa en la expansión de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="2f3a7-123">**dispidApptTZDefEndDisplay** is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="2f3a7-124">Un analizador de debe tener cuidado cuando lee una secuencia obtenida de **dispidApptTZDefEndDisplay**, o cuando conserva **TZDEFINITION** a una secuencia de compromiso a una propiedad binaria, como **dispidApptTZDefEndDisplay**.</span><span class="sxs-lookup"><span data-stu-id="2f3a7-124">A parser must be careful when it reads a stream obtained from **dispidApptTZDefEndDisplay**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefEndDisplay**.</span></span> <span data-ttu-id="2f3a7-125">Para obtener más información, vea [acerca de la conservación de datos TZDEFINITION a una secuencia de confirmación en una propiedad binaria](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2f3a7-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="2f3a7-126">**dispidApptTZDefEndDisplay** especifica la información de zona horaria de la propiedad **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2f3a7-126">**dispidApptTZDefEndDisplay** specifies time zone information for the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="2f3a7-127">El formato y las restricciones de cálculo de **dispidApptTZDefEndDisplay** son los mismos tal como se especifica en la propiedad **dispidApptTZDefStartDisplay** .</span><span class="sxs-lookup"><span data-stu-id="2f3a7-127">The format, constraints, and computation of **dispidApptTZDefEndDisplay** are the same as specified in the **dispidApptTZDefStartDisplay** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2f3a7-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2f3a7-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2f3a7-129">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="2f3a7-129">Protocol specifications</span></span>

<span data-ttu-id="2f3a7-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f3a7-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f3a7-131">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="2f3a7-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2f3a7-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f3a7-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f3a7-133">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="2f3a7-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2f3a7-134">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2f3a7-134">Header files</span></span>

<span data-ttu-id="2f3a7-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2f3a7-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="2f3a7-136">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2f3a7-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2f3a7-137">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="2f3a7-137">See also</span></span>



[<span data-ttu-id="2f3a7-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2f3a7-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2f3a7-139">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="2f3a7-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2f3a7-140">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2f3a7-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2f3a7-141">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="2f3a7-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

