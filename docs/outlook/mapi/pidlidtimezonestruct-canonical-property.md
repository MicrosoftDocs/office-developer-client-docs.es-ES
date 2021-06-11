---
title: Propiedad canónica PidLidTimeZoneStruct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZoneStruct
api_type:
- COM
ms.assetid: 2acf0036-2f3e-4f90-8614-7aa667860f74
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b9c2a1bbf519379c1735c489c2dcd3fcfb395a60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346378"
---
# <a name="pidlidtimezonestruct-canonical-property"></a><span data-ttu-id="fa59d-103">Propiedad canónica PidLidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="fa59d-103">PidLidTimeZoneStruct Canonical Property</span></span>

  
  
<span data-ttu-id="fa59d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa59d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa59d-105">Contiene una secuencia que se asigna al formato persistente de una estructura [TZREG,](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) que describe la zona horaria que se usará para la hora de inicio y finalización de una cita periódica o una solicitud de reunión.</span><span class="sxs-lookup"><span data-stu-id="fa59d-105">Contains a stream that maps to the persisted format of a [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) structure, which describes the time zone to be used for the start and end time of a recurring appointment or meeting request.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fa59d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fa59d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fa59d-107">dispidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="fa59d-107">dispidTimeZoneStruct</span></span>  <br/> |
|<span data-ttu-id="fa59d-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="fa59d-108">Property set:</span></span>  <br/> |<span data-ttu-id="fa59d-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="fa59d-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="fa59d-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="fa59d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fa59d-111">0x00008233</span><span class="sxs-lookup"><span data-stu-id="fa59d-111">0x00008233</span></span>  <br/> |
|<span data-ttu-id="fa59d-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fa59d-112">Data type:</span></span>  <br/> |<span data-ttu-id="fa59d-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fa59d-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fa59d-114">Área:</span><span class="sxs-lookup"><span data-stu-id="fa59d-114">Area:</span></span>  <br/> |<span data-ttu-id="fa59d-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="fa59d-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa59d-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fa59d-116">Remarks</span></span>

<span data-ttu-id="fa59d-117">Microsoft Office Outlook 2003, versiones anteriores de Outlook y aplicaciones basadas en objetos de datos de colaboración (CDO) 1.21 cuyos usuarios no han ejecutado la herramienta de actualización de calendario proporcionada por Outlook o Exchange Server almacenan la hora de inicio y finalización de una cita periódica o una solicitud de reunión como hora relativa, y almacenan la zona horaria donde se crea la cita o la solicitud de reunión en **dispidTimeZoneStruct**.</span><span class="sxs-lookup"><span data-stu-id="fa59d-117">Microsoft Office Outlook 2003, earlier versions of Outlook, and applications that are based on Collaboration Data Objects (CDO) 1.21 whose users have not run the calendar update tool provided by Outlook or Exchange Server store the start time and end time of a recurring appointment or meeting request as relative time, and store the time zone where the appointment or meeting request is created in **dispidTimeZoneStruct**.</span></span> <span data-ttu-id="fa59d-118">Sin embargo, este esquema omite que, con el tiempo, las reglas de zona horaria pueden cambiar, lo que da como resultado algunas citas y reuniones que los usuarios programaron antes de que las reglas cambiaron y se producen en momentos incorrectos.</span><span class="sxs-lookup"><span data-stu-id="fa59d-118">However, this scheme ignores that over time, time zone rules can change, resulting in some appointments and meetings that users scheduled before the rules changed and occur at incorrect times.</span></span> <span data-ttu-id="fa59d-119">Los usuarios y administradores que no ejecutan Windows Vista o que no tienen actualizaciones automáticas activadas deben usar las herramientas de cambio de calendario proporcionadas por Outlook o Exchange Server para ajustar el tiempo de dichas citas y solicitudes de reunión.</span><span class="sxs-lookup"><span data-stu-id="fa59d-119">Users and administrators who are not running Windows Vista or who do not have automatic updates turned on should use the calendar rebasing tools that are provided by Outlook or Exchange Server to adjust the time of such appointments and meeting requests.</span></span> <span data-ttu-id="fa59d-120">Para obtener más información acerca de estas API y herramientas de rebasado de calendarios que rebasen calendarios, vea About [rebasing calendars programmatically for Daylight Saving Time](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa59d-120">For more information about these calendar rebasing tools and APIs that rebase calendars, see [About rebasing calendars programmatically for Daylight Saving Time](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span></span>
  
<span data-ttu-id="fa59d-121">Use el siguiente formato little-endian al analizar una secuencia obtenida de **dispidTimeZoneStruct** o al conservar la estructura **TZREG** en una secuencia para confirmar la propiedad binaria **dispidTimeZoneStruct.**</span><span class="sxs-lookup"><span data-stu-id="fa59d-121">Use the following little-endian format when parsing a stream obtained from **dispidTimeZoneStruct**, or when persisting the **TZREG** structure to a stream to commit to the **dispidTimeZoneStruct** binary property.</span></span> 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

<span data-ttu-id="fa59d-122">Esta propiedad se establece en una serie periódica para especificar información de zona horaria y especifica cómo convertir campos de hora entre la hora local y la hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="fa59d-122">This property is set on a recurring series to specify time-zone information, and specifies how to convert time fields between local time and Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fa59d-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa59d-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fa59d-124">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="fa59d-124">Protocol specifications</span></span>

<span data-ttu-id="fa59d-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa59d-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa59d-126">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="fa59d-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fa59d-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa59d-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa59d-128">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="fa59d-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fa59d-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fa59d-129">Header files</span></span>

<span data-ttu-id="fa59d-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fa59d-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="fa59d-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fa59d-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fa59d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa59d-132">See also</span></span>



[<span data-ttu-id="fa59d-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fa59d-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fa59d-134">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="fa59d-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fa59d-135">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fa59d-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fa59d-136">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="fa59d-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

