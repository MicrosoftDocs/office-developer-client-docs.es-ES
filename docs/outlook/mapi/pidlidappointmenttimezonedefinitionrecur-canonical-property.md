---
title: Propiedad canónica PidLidAppointmentTimeZoneDefinitionRecur
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e5e9b06178a1517fc1c8652b0d667faf1afc77cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345356"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a><span data-ttu-id="8f1dd-103">Propiedad canónica PidLidAppointmentTimeZoneDefinitionRecur</span><span class="sxs-lookup"><span data-stu-id="8f1dd-103">PidLidAppointmentTimeZoneDefinitionRecur Canonical Property</span></span>

  
  
<span data-ttu-id="8f1dd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f1dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f1dd-105">Contiene una secuencia que se asigna al formato persistente de una estructura [TZDEFINITION,](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) que almacena la descripción de la zona horaria que se usa cuando se crea una cita periódica o una solicitud de reunión.</span><span class="sxs-lookup"><span data-stu-id="8f1dd-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when a recurring appointment or meeting request is created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8f1dd-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8f1dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8f1dd-107">dispidApptTZDefRecur</span><span class="sxs-lookup"><span data-stu-id="8f1dd-107">dispidApptTZDefRecur</span></span>  <br/> |
|<span data-ttu-id="8f1dd-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="8f1dd-108">Property set:</span></span>  <br/> |<span data-ttu-id="8f1dd-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="8f1dd-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="8f1dd-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="8f1dd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8f1dd-111">0x00008260</span><span class="sxs-lookup"><span data-stu-id="8f1dd-111">0x00008260</span></span>  <br/> |
|<span data-ttu-id="8f1dd-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8f1dd-112">Data type:</span></span>  <br/> |<span data-ttu-id="8f1dd-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8f1dd-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8f1dd-114">Área:</span><span class="sxs-lookup"><span data-stu-id="8f1dd-114">Area:</span></span>  <br/> |<span data-ttu-id="8f1dd-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="8f1dd-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f1dd-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8f1dd-116">Remarks</span></span>

<span data-ttu-id="8f1dd-117">Las versiones de Microsoft Outlook desde Microsoft Office Outlook 2007 y las soluciones basadas en Collaboration Data Objects (CDO) 1.2.1 que ejecutan la herramienta de actualización de calendario de Outlook o Exchange Server usan las propiedades **dispidApptTZDefRecur** y **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) para determinar si se debe ajustar la reunión periódica si cambian las reglas de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="8f1dd-117">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on Collaboration Data Objects (CDO) 1.2.1 that have run the Outlook or Exchange Server calendar update tool use the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) properties to determine whether the recurring meeting should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="8f1dd-118">Estas propiedades deben sincronizarse, ya que los clientes más antiguos aún pueden manipular la **propiedad dispidTimeZoneStruct.**</span><span class="sxs-lookup"><span data-stu-id="8f1dd-118">These properties must be synchronized, because older clients may still manipulate the **dispidTimeZoneStruct** property.</span></span> <span data-ttu-id="8f1dd-119">Para detectar si las dos propiedades están sincronizadas, el miembro **wFlags** de la regla que coincide con **dispidTimeZoneStruct** debe tener el TZRULE_FLAG_RECUR_CURRENT_TZREG marca establecida.</span><span class="sxs-lookup"><span data-stu-id="8f1dd-119">To detect whether the two properties are synchronized, the **wFlags** member for the rule that matches **dispidTimeZoneStruct** should have the TZRULE_FLAG_RECUR_CURRENT_TZREG flag set.</span></span> <span data-ttu-id="8f1dd-120">Si no se establece esta marca o se establece y la regla de la propiedad **dispidTimeZoneStruct** no coincide con la regla marcada, se debe descartar la propiedad **dispidApptTZDefRecur** y, en su lugar, debe **usarse dispidTimeZoneStruct.**</span><span class="sxs-lookup"><span data-stu-id="8f1dd-120">If this flag is not set, or it is set and the rule in the **dispidTimeZoneStruct** property does not match the marked rule, the **dispidApptTZDefRecur** property should be discarded and **dispidTimeZoneStruct** should be used instead.</span></span> 
  
<span data-ttu-id="8f1dd-121">Al escribir las propiedades **dispidApptTZDefRecur** y **dispidTimeZoneStruct** en una nueva reunión periódica, o cuando se realiza una elección arbitraria para usar la propiedad **dispidTimeZoneStruct,** se debe usar la definición actual de la zona horaria (según el Registro de Windows).</span><span class="sxs-lookup"><span data-stu-id="8f1dd-121">When you write both the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** properties to a new recurring meeting, or, when you make an arbitrary choice to use the **dispidTimeZoneStruct** property, the current definition for the time zone (according to the Windows registry) should be used.</span></span> 
  
<span data-ttu-id="8f1dd-122">Un analizador debe tener cuidado cuando lee una secuencia que se obtiene de **dispidApptTZDefRecur**, o cuando conserva **TZDEFINITION** en una secuencia para el compromiso con una propiedad binaria como **dispidApptTZDefRecur**.</span><span class="sxs-lookup"><span data-stu-id="8f1dd-122">A parser must be careful when it reads a stream that is obtained from **dispidApptTZDefRecur**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="8f1dd-123">Para obtener más información, vea [Acerca de la persistencia de TZDEFINITION en una secuencia para confirmar una propiedad binaria.](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f1dd-123">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="8f1dd-124">**dispidApptTZDefRecur** especifica información de zona horaria que describe cómo convertir la fecha y la hora de la reunión en una serie periódica a y desde la hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="8f1dd-124">**dispidApptTZDefRecur** specifies time zone information that describes how to convert the meeting date and time on a recurring series to and from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="8f1dd-125">Si se establece esta propiedad pero tiene datos que son incoherentes con los datos representados por **dispidTimeZoneStruct**, el cliente debe usar **dispidTimeZoneStruct** en lugar de **dispidApptTZDefRecur**.</span><span class="sxs-lookup"><span data-stu-id="8f1dd-125">If this property is set but it has data that is inconsistent with the data represented by **dispidTimeZoneStruct**, the client must use **dispidTimeZoneStruct** instead of **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="8f1dd-126">Si **no se establece dispidApptTZDefRecur,** se usará la propiedad **PidLidTimeZoneStruct** en su lugar.</span><span class="sxs-lookup"><span data-stu-id="8f1dd-126">If **dispidApptTZDefRecur** is not set, the **PidLidTimeZoneStruct** property will be used instead.</span></span> <span data-ttu-id="8f1dd-127">Los campos de este BLOB se codifican en orden de bytes little-endian.</span><span class="sxs-lookup"><span data-stu-id="8f1dd-127">The fields in this BLOB are encoded in little-endian byte order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8f1dd-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8f1dd-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8f1dd-129">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="8f1dd-129">Protocol specifications</span></span>

<span data-ttu-id="8f1dd-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f1dd-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f1dd-131">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="8f1dd-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8f1dd-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f1dd-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f1dd-133">Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f1dd-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8f1dd-134">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8f1dd-134">Header files</span></span>

<span data-ttu-id="8f1dd-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8f1dd-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="8f1dd-136">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8f1dd-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8f1dd-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8f1dd-137">See also</span></span>



[<span data-ttu-id="8f1dd-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8f1dd-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8f1dd-139">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="8f1dd-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8f1dd-140">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8f1dd-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8f1dd-141">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="8f1dd-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

