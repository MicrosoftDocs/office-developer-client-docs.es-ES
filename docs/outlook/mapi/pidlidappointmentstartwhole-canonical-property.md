---
title: Propiedad canónico PidLidAppointmentStartWhole
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentStartWhole
api_type:
- COM
ms.assetid: e5e8ed98-57af-40d0-85c4-9d9832626e6b
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 6f7137e3d5712e7d7ce12800a07b860679dd099a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818583"
---
# <a name="pidlidappointmentstartwhole-canonical-property"></a><span data-ttu-id="90a48-103">Propiedad canónico PidLidAppointmentStartWhole</span><span class="sxs-lookup"><span data-stu-id="90a48-103">PidLidAppointmentStartWhole Canonical Property</span></span>

  
  
<span data-ttu-id="90a48-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="90a48-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="90a48-105">Representa la fecha y hora cuando empieza a una cita.</span><span class="sxs-lookup"><span data-stu-id="90a48-105">Represents the date and time when an appointment begins.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="90a48-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="90a48-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="90a48-107">dispidApptStartWhole</span><span class="sxs-lookup"><span data-stu-id="90a48-107">dispidApptStartWhole</span></span>  <br/> |
|<span data-ttu-id="90a48-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="90a48-108">Property set:</span></span>  <br/> |<span data-ttu-id="90a48-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="90a48-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="90a48-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="90a48-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="90a48-111">0x0000820D</span><span class="sxs-lookup"><span data-stu-id="90a48-111">0x0000820D</span></span>  <br/> |
|<span data-ttu-id="90a48-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="90a48-112">Data type:</span></span>  <br/> |<span data-ttu-id="90a48-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="90a48-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="90a48-114">Área:</span><span class="sxs-lookup"><span data-stu-id="90a48-114">Area:</span></span>  <br/> |<span data-ttu-id="90a48-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="90a48-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90a48-116">Notas</span><span class="sxs-lookup"><span data-stu-id="90a48-116">Remarks</span></span>

<span data-ttu-id="90a48-117">Esta propiedad especifica la fecha de inicio y la hora del evento.</span><span class="sxs-lookup"><span data-stu-id="90a48-117">This property specifies the start date and time of the event.</span></span> <span data-ttu-id="90a48-118">Esta propiedad debe ser en hora Universal coordinada (UTC) y debe ser menor que el valor de la propiedad **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="90a48-118">This property must be in Coordinated Universal Time (UTC) and must be less than the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="90a48-119">Para una serie periódica, esta propiedad es la fecha de inicio y la hora de la primera instancia según el patrón de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="90a48-119">For a recurring series, this property is the start date and time of the first instance according to the recurrence pattern.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="90a48-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="90a48-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="90a48-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="90a48-121">Protocol specifications</span></span>

<span data-ttu-id="90a48-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90a48-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90a48-123">Proporciona la definición del conjunto de propiedad y referencias a las especificaciones de protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="90a48-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="90a48-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90a48-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90a48-125">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="90a48-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="90a48-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="90a48-126">Header files</span></span>

<span data-ttu-id="90a48-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="90a48-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="90a48-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="90a48-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90a48-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="90a48-129">See also</span></span>



[<span data-ttu-id="90a48-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="90a48-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="90a48-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="90a48-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="90a48-132">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="90a48-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="90a48-133">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="90a48-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

