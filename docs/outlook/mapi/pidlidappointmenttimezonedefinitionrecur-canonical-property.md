---
title: Propiedad canónico PidLidAppointmentTimeZoneDefinitionRecur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionRecur
api_type:
- COM
ms.assetid: 52fd57a0-9e34-4452-9ecd-2acb454446c9
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 5cff6ec7b39c26eec098d250688d98bf1e4799ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818591"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a><span data-ttu-id="d3334-103">Propiedad canónico PidLidAppointmentTimeZoneDefinitionRecur</span><span class="sxs-lookup"><span data-stu-id="d3334-103">PidLidAppointmentTimeZoneDefinitionRecur Canonical Property</span></span>

  
  
<span data-ttu-id="d3334-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d3334-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d3334-105">Contiene una secuencia que se asigna al formato persistente de una estructura [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , que almacena la descripción de la zona horaria que se usa cuando se crea una cita periódica o una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="d3334-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when a recurring appointment or meeting request is created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3334-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d3334-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d3334-107">dispidApptTZDefRecur</span><span class="sxs-lookup"><span data-stu-id="d3334-107">dispidApptTZDefRecur</span></span>  <br/> |
|<span data-ttu-id="d3334-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="d3334-108">Property set:</span></span>  <br/> |<span data-ttu-id="d3334-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="d3334-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="d3334-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="d3334-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d3334-111">0x00008260</span><span class="sxs-lookup"><span data-stu-id="d3334-111">0x00008260</span></span>  <br/> |
|<span data-ttu-id="d3334-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d3334-112">Data type:</span></span>  <br/> |<span data-ttu-id="d3334-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d3334-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d3334-114">Área:</span><span class="sxs-lookup"><span data-stu-id="d3334-114">Area:</span></span>  <br/> |<span data-ttu-id="d3334-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="d3334-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3334-116">Notas</span><span class="sxs-lookup"><span data-stu-id="d3334-116">Remarks</span></span>

<span data-ttu-id="d3334-117">Versiones de Microsoft Outlook desde Microsoft Office Outlook 2007 y soluciones basadas en Collaboration Data Objects (CDO) 1.2.1 que se han ejecutado el calendario de Outlook o Exchange Server actualización de uso de la herramienta el **dispidApptTZDefRecur** y ** dispidTimeZoneStruct** propiedades ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) para determinar si se debe ajustar la reunión periódica si cambian las reglas de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="d3334-117">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on Collaboration Data Objects (CDO) 1.2.1 that have run the Outlook or Exchange Server calendar update tool use the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) properties to determine whether the recurring meeting should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="d3334-118">Estas propiedades se deben sincronizarse, debido a que los clientes más antiguos aún pueden manipular la propiedad **dispidTimeZoneStruct** .</span><span class="sxs-lookup"><span data-stu-id="d3334-118">These properties must be synchronized, because older clients may still manipulate the **dispidTimeZoneStruct** property.</span></span> <span data-ttu-id="d3334-119">Para detectar si se sincronizan las dos propiedades, el miembro **wFlags** para la regla que coincide con **dispidTimeZoneStruct** debe tener el indicador TZRULE_FLAG_RECUR_CURRENT_TZREG establecido.</span><span class="sxs-lookup"><span data-stu-id="d3334-119">To detect whether the two properties are synchronized, the **wFlags** member for the rule that matches **dispidTimeZoneStruct** should have the TZRULE_FLAG_RECUR_CURRENT_TZREG flag set.</span></span> <span data-ttu-id="d3334-120">Si no se establece este marcador, o se establece y la regla en la propiedad **dispidTimeZoneStruct** no coincide con la regla de marcado, la propiedad **dispidApptTZDefRecur** debe descartarse y **dispidTimeZoneStruct** debe usarse en su lugar.</span><span class="sxs-lookup"><span data-stu-id="d3334-120">If this flag is not set, or it is set and the rule in the **dispidTimeZoneStruct** property does not match the marked rule, the **dispidApptTZDefRecur** property should be discarded and **dispidTimeZoneStruct** should be used instead.</span></span> 
  
<span data-ttu-id="d3334-121">Al escribir las propiedades de la **dispidApptTZDefRecur** y la **dispidTimeZoneStruct** a una nueva reunión periódica o, cuando se realiza una opción para usar la propiedad **dispidTimeZoneStruct** , la definición actual para la zona horaria (arbitraria debe usarse según el registro de Windows).</span><span class="sxs-lookup"><span data-stu-id="d3334-121">When you write both the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** properties to a new recurring meeting, or, when you make an arbitrary choice to use the **dispidTimeZoneStruct** property, the current definition for the time zone (according to the Windows registry) should be used.</span></span> 
  
<span data-ttu-id="d3334-122">Un analizador de debe tener cuidado cuando lee una secuencia que se obtiene de **dispidApptTZDefRecur**, o cuando conserva **TZDEFINITION** a una secuencia de compromiso a una propiedad binaria, como **dispidApptTZDefRecur**.</span><span class="sxs-lookup"><span data-stu-id="d3334-122">A parser must be careful when it reads a stream that is obtained from **dispidApptTZDefRecur**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="d3334-123">Para obtener más información, vea [acerca de la conservación de datos TZDEFINITION a una secuencia de confirmación en una propiedad binaria](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d3334-123">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="d3334-124">**dispidApptTZDefRecur** especifica la información de zona horaria que se describe el procedimiento para convertir la fecha de la reunión y la hora en una serie periódica y de la hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="d3334-124">**dispidApptTZDefRecur** specifies time zone information that describes how to convert the meeting date and time on a recurring series to and from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="d3334-125">Si se establece esta propiedad, pero tiene datos que no es coherentes con los datos representados por **dispidTimeZoneStruct**, el cliente debe utilizar **dispidTimeZoneStruct** en lugar de **dispidApptTZDefRecur**.</span><span class="sxs-lookup"><span data-stu-id="d3334-125">If this property is set but it has data that is inconsistent with the data represented by **dispidTimeZoneStruct**, the client must use **dispidTimeZoneStruct** instead of **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="d3334-126">Si **dispidApptTZDefRecur** no está establecida, la propiedad **PidLidTimeZoneStruct** se usará en su lugar.</span><span class="sxs-lookup"><span data-stu-id="d3334-126">If **dispidApptTZDefRecur** is not set, the **PidLidTimeZoneStruct** property will be used instead.</span></span> <span data-ttu-id="d3334-127">Los campos de este BLOB se codifican en orden de bytes little-endian.</span><span class="sxs-lookup"><span data-stu-id="d3334-127">The fields in this BLOB are encoded in little-endian byte order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d3334-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d3334-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d3334-129">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d3334-129">Protocol specifications</span></span>

<span data-ttu-id="d3334-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3334-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3334-131">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d3334-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d3334-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3334-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3334-133">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="d3334-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d3334-134">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d3334-134">Header files</span></span>

<span data-ttu-id="d3334-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d3334-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="d3334-136">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d3334-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d3334-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="d3334-137">See also</span></span>



[<span data-ttu-id="d3334-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d3334-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d3334-139">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d3334-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d3334-140">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="d3334-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d3334-141">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d3334-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

