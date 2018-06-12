---
title: Propiedad canónico PidLidCalendarType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCalendarType
api_type:
- COM
ms.assetid: 06e066f1-2b7d-4a6b-b88c-85a9bfa83bd3
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 8e3017d18491fde6b66c3173c43b8b9d0ee37ea8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818588"
---
# <a name="pidlidcalendartype-canonical-property"></a><span data-ttu-id="718d6-103">Propiedad canónico PidLidCalendarType</span><span class="sxs-lookup"><span data-stu-id="718d6-103">PidLidCalendarType Canonical Property</span></span>

  
  
<span data-ttu-id="718d6-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="718d6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="718d6-105">Especifica el valor del campo tipo de calendario de la propiedad **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="718d6-105">Specifies the value of the CalendarType field from the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="718d6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="718d6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="718d6-107">LID_CALENDAR_TYPE</span><span class="sxs-lookup"><span data-stu-id="718d6-107">LID_CALENDAR_TYPE</span></span>  <br/> |
|<span data-ttu-id="718d6-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="718d6-108">Property set:</span></span>  <br/> |<span data-ttu-id="718d6-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="718d6-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="718d6-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="718d6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="718d6-111">0x0000001C</span><span class="sxs-lookup"><span data-stu-id="718d6-111">0x0000001C</span></span>  <br/> |
|<span data-ttu-id="718d6-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="718d6-112">Data type:</span></span>  <br/> |<span data-ttu-id="718d6-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="718d6-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="718d6-114">Área:</span><span class="sxs-lookup"><span data-stu-id="718d6-114">Area:</span></span>  <br/> |<span data-ttu-id="718d6-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="718d6-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="718d6-116">Notas</span><span class="sxs-lookup"><span data-stu-id="718d6-116">Remarks</span></span>

<span data-ttu-id="718d6-117">Cuando la convocatoria de reunión representa una serie periódica o una excepción, este es el valor del campo tipo de calendario de la propiedad **dispidApptRecur** .</span><span class="sxs-lookup"><span data-stu-id="718d6-117">When the meeting request represents a recurring series or an exception, this is the value of the CalendarType field from the **dispidApptRecur** property.</span></span> <span data-ttu-id="718d6-118">De lo contrario, esta propiedad no es establecer y se supone que es 0.</span><span class="sxs-lookup"><span data-stu-id="718d6-118">Otherwise, this property is not set and assumed to be 0.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="718d6-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="718d6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="718d6-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="718d6-120">Protocol specifications</span></span>

<span data-ttu-id="718d6-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="718d6-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="718d6-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="718d6-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="718d6-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="718d6-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="718d6-124">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="718d6-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="718d6-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="718d6-125">Header files</span></span>

<span data-ttu-id="718d6-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="718d6-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="718d6-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="718d6-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="718d6-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="718d6-128">See also</span></span>



[<span data-ttu-id="718d6-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="718d6-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="718d6-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="718d6-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="718d6-131">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="718d6-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="718d6-132">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="718d6-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

