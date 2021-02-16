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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345020"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a><span data-ttu-id="80c67-103">Propiedad canónica PidLidAppointmentTimeZoneDefinitionStartDisplay</span><span class="sxs-lookup"><span data-stu-id="80c67-103">PidLidAppointmentTimeZoneDefinitionStartDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="80c67-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80c67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80c67-105">Contiene una secuencia que se asigna al formato persistente de una estructura [TZDEFINITION,](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) que almacena la descripción de la zona horaria que se usa cuando se selecciona la hora de inicio de una cita de instancia única o una solicitud de reunión.</span><span class="sxs-lookup"><span data-stu-id="80c67-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the start time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="80c67-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="80c67-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="80c67-107">dispidApptTZDefStartDisplay</span><span class="sxs-lookup"><span data-stu-id="80c67-107">dispidApptTZDefStartDisplay</span></span>  <br/> |
|<span data-ttu-id="80c67-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="80c67-108">Property set:</span></span>  <br/> |<span data-ttu-id="80c67-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="80c67-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="80c67-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="80c67-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="80c67-111">0x0000825E</span><span class="sxs-lookup"><span data-stu-id="80c67-111">0x0000825E</span></span>  <br/> |
|<span data-ttu-id="80c67-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="80c67-112">Data type:</span></span>  <br/> |<span data-ttu-id="80c67-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="80c67-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="80c67-114">Área:</span><span class="sxs-lookup"><span data-stu-id="80c67-114">Area:</span></span>  <br/> |<span data-ttu-id="80c67-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="80c67-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80c67-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="80c67-116">Remarks</span></span>

<span data-ttu-id="80c67-117">Microsoft Office Outlook 2003 o versiones anteriores, y soluciones basadas en Collaboration Data Objects (CDO) 1.2.1 y que no han ejecutado la herramienta de actualización de calendario para Outlook o Microsoft Exchange Server, almacene la hora de inicio y la hora de finalización de las citas de instancia única y las solicitudes de reunión en hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="80c67-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="80c67-118">Estos clientes no almacenan información sobre la zona horaria en la que se crea la cita o la solicitud de reunión.</span><span class="sxs-lookup"><span data-stu-id="80c67-118">These clients do not store any information for the time zone in which the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="80c67-119">Las versiones de Outlook desde Microsoft Office Outlook 2007 y las soluciones basadas en CDO 1.2.1 que han ejecutado la herramienta de actualización de calendario de Outlook o Exchange Server usan esta propiedad para almacenar la zona horaria de la hora de inicio.</span><span class="sxs-lookup"><span data-stu-id="80c67-119">Versions of Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use this property to store the time zone for the start time.</span></span> <span data-ttu-id="80c67-120">La **propiedad dispidApptTZDefStartDisplay** muestra la cita o reunión en la zona horaria original que se programó.</span><span class="sxs-lookup"><span data-stu-id="80c67-120">The **dispidApptTZDefStartDisplay** property shows the appointment or meeting in the original time zone that it was scheduled.</span></span> <span data-ttu-id="80c67-121">Determina si se debe ajustar la hora de inicio si cambian las reglas de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="80c67-121">It determines whether the start time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="80c67-122">Si falta esta propiedad, se asume la zona horaria local actual.</span><span class="sxs-lookup"><span data-stu-id="80c67-122">If this property is missing, the current local time zone is assumed.</span></span> <span data-ttu-id="80c67-123">Esta propiedad se usa únicamente con fines de presentación y no se usa en la expansión de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="80c67-123">This property is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="80c67-124">Un analizador debe tener cuidado cuando lee una secuencia obtenida de esta propiedad o cuando conserva **TZDEFINITION** en una secuencia para el compromiso con una propiedad binaria como **dispidApptTZDefStartDisplay**.</span><span class="sxs-lookup"><span data-stu-id="80c67-124">A parser must be careful when it reads a stream obtained from this property, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefStartDisplay**.</span></span> <span data-ttu-id="80c67-125">Para obtener más información, vea [Acerca de la persistencia de TZDEFINITION en una secuencia para confirmar una propiedad binaria.](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80c67-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="80c67-126">Esta propiedad especifica información de zona horaria para la propiedad **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="80c67-126">This property specifies time zone information for the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="80c67-127">El valor de **dispidApptTZDefStartDisplay** se usa para convertir la fecha y hora de inicio de UTC a la zona horaria local con fines de presentación.</span><span class="sxs-lookup"><span data-stu-id="80c67-127">The value of **dispidApptTZDefStartDisplay** is used to convert the start date and time from UTC to the local time zone for display purposes.</span></span> <span data-ttu-id="80c67-128">Para cada **TZRULE** especificado por esta propiedad, no se debe establecer TZRULE_FLAG_RECUR_CURRENT_TZREG marca.</span><span class="sxs-lookup"><span data-stu-id="80c67-128">For each **TZRULE** specified by this property, the TZRULE_FLAG_RECUR_CURRENT_TZREG flag must not be set.</span></span> <span data-ttu-id="80c67-129">Por ejemplo, si **TZRULE** es la regla efectiva, el valor del campo, **TZRULE** debe ser "0x0002"; de lo contrario, debe ser "0x0000".</span><span class="sxs-lookup"><span data-stu-id="80c67-129">For example, if the **TZRULE** is the effective rule, the value of the field, **TZRULE** must be "0x0002"; otherwise, it must be "0x0000".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="80c67-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="80c67-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="80c67-131">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="80c67-131">Protocol specifications</span></span>

<span data-ttu-id="80c67-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80c67-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80c67-133">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="80c67-133">Provides property set definitions and references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="80c67-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80c67-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80c67-135">Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.</span><span class="sxs-lookup"><span data-stu-id="80c67-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="80c67-136">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="80c67-136">Header files</span></span>

<span data-ttu-id="80c67-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="80c67-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="80c67-138">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="80c67-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="80c67-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="80c67-139">See also</span></span>



[<span data-ttu-id="80c67-140">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="80c67-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="80c67-141">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="80c67-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="80c67-142">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="80c67-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="80c67-143">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="80c67-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

