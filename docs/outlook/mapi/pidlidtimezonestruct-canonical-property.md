---
title: Propiedad canónico PidLidTimeZoneStruct
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: a1a96cdb3aed03b9621097f1ef858a09391c0693
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819000"
---
# <a name="pidlidtimezonestruct-canonical-property"></a><span data-ttu-id="7af81-103">Propiedad canónico PidLidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="7af81-103">PidLidTimeZoneStruct Canonical Property</span></span>

  
  
<span data-ttu-id="7af81-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7af81-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7af81-105">Contiene una secuencia que se asigna al formato persistente de una estructura [TZREG](http://msdn.microsoft.com/es-es/library/bb820983%28v=office.12%29.aspx) , que se describe la zona horaria que se usará para la hora de inicio y finalización de una cita periódica o convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="7af81-105">Contains a stream that maps to the persisted format of a [TZREG](http://msdn.microsoft.com/es-es/library/bb820983%28v=office.12%29.aspx) structure, which describes the time zone to be used for the start and end time of a recurring appointment or meeting request.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7af81-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7af81-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7af81-107">dispidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="7af81-107">dispidTimeZoneStruct</span></span>  <br/> |
|<span data-ttu-id="7af81-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="7af81-108">Property set:</span></span>  <br/> |<span data-ttu-id="7af81-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="7af81-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="7af81-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="7af81-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7af81-111">0x00008233</span><span class="sxs-lookup"><span data-stu-id="7af81-111">0x00008233</span></span>  <br/> |
|<span data-ttu-id="7af81-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7af81-112">Data type:</span></span>  <br/> |<span data-ttu-id="7af81-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7af81-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7af81-114">Área:</span><span class="sxs-lookup"><span data-stu-id="7af81-114">Area:</span></span>  <br/> |<span data-ttu-id="7af81-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="7af81-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7af81-116">Notas</span><span class="sxs-lookup"><span data-stu-id="7af81-116">Remarks</span></span>

<span data-ttu-id="7af81-117">Microsoft Office Outlook 2003, las versiones anteriores de Outlook y las aplicaciones que se basan en Collaboration Data Objects (CDO) 1.21 cuyos usuarios no se ejecuta la herramienta de actualización de calendario proporcionada por Outlook o Exchange Server almacenan la hora de inicio y hora de finalización de un periódica una cita o convocatoria de reunión como tiempo relativo y almacenar la zona horaria donde se crea la solicitud de reunión o cita en **dispidTimeZoneStruct**.</span><span class="sxs-lookup"><span data-stu-id="7af81-117">Microsoft Office Outlook 2003, earlier versions of Outlook, and applications that are based on Collaboration Data Objects (CDO) 1.21 whose users have not run the calendar update tool provided by Outlook or Exchange Server store the start time and end time of a recurring appointment or meeting request as relative time, and store the time zone where the appointment or meeting request is created in **dispidTimeZoneStruct**.</span></span> <span data-ttu-id="7af81-118">Sin embargo, este esquema omite que con el tiempo, las reglas de zona horaria pueden cambiar, resultante en algunas citas y reuniones que los usuarios programado antes de que las reglas ha cambiado y se produzcan en momentos incorrectas.</span><span class="sxs-lookup"><span data-stu-id="7af81-118">However, this scheme ignores that over time, time zone rules can change, resulting in some appointments and meetings that users scheduled before the rules changed and occur at incorrect times.</span></span> <span data-ttu-id="7af81-119">Los usuarios y administradores que no ejecutan Windows Vista o que no tienen actualizaciones automáticas está activada deben usar el calendario reorganización de las herramientas proporcionadas por Outlook o Exchange Server para ajustar el tiempo de dichas citas y convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="7af81-119">Users and administrators who are not running Windows Vista or who do not have automatic updates turned on should use the calendar rebasing tools that are provided by Outlook or Exchange Server to adjust the time of such appointments and meeting requests.</span></span> <span data-ttu-id="7af81-120">Para obtener más información acerca de estas herramientas de reajuste de calendario y las API que reorganización de calendarios, vea [acerca de los calendarios reajuste mediante programación del horario de verano](http://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7af81-120">For more information about these calendar rebasing tools and APIs that rebase calendars, see [About rebasing calendars programmatically for Daylight Saving Time](http://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span></span>
  
<span data-ttu-id="7af81-121">Use el siguiente formato "little-endian" al analizar una secuencia obtenida desde **dispidTimeZoneStruct**, o cuando se almacena la estructura **TZREG** a una secuencia para confirmar a la propiedad binarios **dispidTimeZoneStruct** .</span><span class="sxs-lookup"><span data-stu-id="7af81-121">Use the following little-endian format when parsing a stream obtained from **dispidTimeZoneStruct**, or when persisting the **TZREG** structure to a stream to commit to the **dispidTimeZoneStruct** binary property.</span></span> 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

<span data-ttu-id="7af81-122">Esta propiedad se establece en una serie periódica para especificar la información de zona horaria y especifica cómo se convierten los campos de tiempo entre la hora local y la hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="7af81-122">This property is set on a recurring series to specify time-zone information, and specifies how to convert time fields between local time and Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7af81-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7af81-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7af81-124">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="7af81-124">Protocol specifications</span></span>

<span data-ttu-id="7af81-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7af81-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7af81-126">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7af81-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7af81-127">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7af81-127">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7af81-128">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="7af81-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7af81-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7af81-129">Header files</span></span>

<span data-ttu-id="7af81-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7af81-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="7af81-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7af81-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7af81-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="7af81-132">See also</span></span>



[<span data-ttu-id="7af81-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7af81-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7af81-134">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="7af81-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7af81-135">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="7af81-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7af81-136">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="7af81-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

