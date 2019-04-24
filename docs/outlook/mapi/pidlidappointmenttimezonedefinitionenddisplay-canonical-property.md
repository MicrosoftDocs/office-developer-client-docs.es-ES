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
ms.openlocfilehash: 24ccd25a1d799f3146bd230e5156be0051104f47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345384"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a><span data-ttu-id="dcbcc-103">Propiedad canónica PidLidAppointmentTimeZoneDefinitionEndDisplay</span><span class="sxs-lookup"><span data-stu-id="dcbcc-103">PidLidAppointmentTimeZoneDefinitionEndDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="dcbcc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dcbcc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dcbcc-105">Contiene una secuencia que se asigna al formato persistente de una estructura [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , que almacena la descripción de la zona horaria que se usa cuando se selecciona la hora de finalización de una cita o convocatoria de reunión de una sola instancia.</span><span class="sxs-lookup"><span data-stu-id="dcbcc-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the end time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dcbcc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="dcbcc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dcbcc-107">dispidApptTZDefEndDisplay</span><span class="sxs-lookup"><span data-stu-id="dcbcc-107">dispidApptTZDefEndDisplay</span></span>  <br/> |
|<span data-ttu-id="dcbcc-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="dcbcc-108">Property set:</span></span>  <br/> |<span data-ttu-id="dcbcc-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="dcbcc-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="dcbcc-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="dcbcc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="dcbcc-111">0x0000825F</span><span class="sxs-lookup"><span data-stu-id="dcbcc-111">0x0000825F</span></span>  <br/> |
|<span data-ttu-id="dcbcc-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="dcbcc-112">Data type:</span></span>  <br/> |<span data-ttu-id="dcbcc-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="dcbcc-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="dcbcc-114">Área:</span><span class="sxs-lookup"><span data-stu-id="dcbcc-114">Area:</span></span>  <br/> |<span data-ttu-id="dcbcc-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="dcbcc-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dcbcc-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dcbcc-116">Remarks</span></span>

<span data-ttu-id="dcbcc-117">Microsoft Office Outlook 2003 o anterior, y soluciones basadas en Collaboration Data Objects (CDO) 1.2.1 y que no han ejecutado la herramienta de actualización de calendarios para Outlook o Microsoft Exchange Server, almacenan la hora de inicio y la hora de finalización de una sola instancia citas y convocatorias de reunión en la hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="dcbcc-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="dcbcc-118">Estos clientes no almacenan ninguna información para la zona horaria en la que se crea la cita o la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="dcbcc-118">These clients do not store any information for the time zone where the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="dcbcc-119">Las versiones de Microsoft Outlook desde Microsoft Office Outlook 2007 y las soluciones basadas en CDO 1.2.1 que ejecutaban la herramienta de actualización de calendario de Outlook o Exchange Server usan **dispidApptTZDefEndDisplay** para almacenar la zona horaria para la hora de finalización.</span><span class="sxs-lookup"><span data-stu-id="dcbcc-119">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use **dispidApptTZDefEndDisplay** to store the time zone for the end time.</span></span> <span data-ttu-id="dcbcc-120">**dispidApptTZDefEndDisplay** muestra la cita o la reunión en la zona horaria original en la que se programó y determina si la hora de finalización debe ajustarse si las reglas de la zona horaria cambian.</span><span class="sxs-lookup"><span data-stu-id="dcbcc-120">**dispidApptTZDefEndDisplay** shows the appointment or meeting in the original time zone that it was scheduled, and determines whether the end time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="dcbcc-121">Si falta esta propiedad, se utiliza la zona horaria especificada por la propiedad **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dcbcc-121">If this property is missing, the time zone specified by the **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) property is used.</span></span> <span data-ttu-id="dcbcc-122">Si **dispidApptTZDefStartDisplay** falta o no es válido, se supone que se trata de la zona horaria local actual.</span><span class="sxs-lookup"><span data-stu-id="dcbcc-122">If **dispidApptTZDefStartDisplay** is missing or invalid, the current local time zone is assumed.</span></span> <span data-ttu-id="dcbcc-123">**dispidApptTZDefEndDisplay** se usa solo con fines de presentación y no se usa en la expansión de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="dcbcc-123">**dispidApptTZDefEndDisplay** is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="dcbcc-124">Un analizador debe tener cuidado cuando lee una secuencia obtenida de **dispidApptTZDefEndDisplay**o cuando continúa **TZDEFINITION** en una secuencia para que se comprometa a una propiedad binaria como **dispidApptTZDefEndDisplay**.</span><span class="sxs-lookup"><span data-stu-id="dcbcc-124">A parser must be careful when it reads a stream obtained from **dispidApptTZDefEndDisplay**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefEndDisplay**.</span></span> <span data-ttu-id="dcbcc-125">Para obtener más información, vea [acerca de la persistencia de TZDEFINITION en una secuencia para confirmar una propiedad binaria](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="dcbcc-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="dcbcc-126">**dispidApptTZDefEndDisplay** especifica la información de zona horaria para la propiedad **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dcbcc-126">**dispidApptTZDefEndDisplay** specifies time zone information for the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="dcbcc-127">El formato, las restricciones y el cálculo de **dispidApptTZDefEndDisplay** son los mismos que los especificados en la propiedad **dispidApptTZDefStartDisplay** .</span><span class="sxs-lookup"><span data-stu-id="dcbcc-127">The format, constraints, and computation of **dispidApptTZDefEndDisplay** are the same as specified in the **dispidApptTZDefStartDisplay** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dcbcc-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dcbcc-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dcbcc-129">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="dcbcc-129">Protocol specifications</span></span>

<span data-ttu-id="dcbcc-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dcbcc-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dcbcc-131">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="dcbcc-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dcbcc-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dcbcc-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dcbcc-133">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="dcbcc-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dcbcc-134">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="dcbcc-134">Header files</span></span>

<span data-ttu-id="dcbcc-135">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="dcbcc-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="dcbcc-136">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="dcbcc-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dcbcc-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="dcbcc-137">See also</span></span>



[<span data-ttu-id="dcbcc-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dcbcc-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dcbcc-139">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="dcbcc-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dcbcc-140">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="dcbcc-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dcbcc-141">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="dcbcc-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

