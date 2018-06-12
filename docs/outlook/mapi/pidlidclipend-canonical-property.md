---
title: Propiedad canónico PidLidClipEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidClipEnd
api_type:
- COM
ms.assetid: 17c8db96-80dd-4a7a-9a1b-ab1b37ba616c
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 1353289da2b428fb58adecc6f7830a2eea4b519a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818602"
---
# <a name="pidlidclipend-canonical-property"></a><span data-ttu-id="bef10-103">Propiedad canónico PidLidClipEnd</span><span class="sxs-lookup"><span data-stu-id="bef10-103">PidLidClipEnd Canonical Property</span></span>

  
  
<span data-ttu-id="bef10-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bef10-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bef10-105">Especifica la fecha de finalización y la hora del evento en hora Universal coordinada (UTC) para los objetos de calendario de una sola instancia.</span><span class="sxs-lookup"><span data-stu-id="bef10-105">Specifies the end date and time of the event in Coordinated Universal Time (UTC) for single instance calendar objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bef10-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="bef10-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bef10-107">dispidClipEnd</span><span class="sxs-lookup"><span data-stu-id="bef10-107">dispidClipEnd</span></span>  <br/> |
|<span data-ttu-id="bef10-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="bef10-108">Property set:</span></span>  <br/> |<span data-ttu-id="bef10-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="bef10-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="bef10-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="bef10-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bef10-111">0x00008236</span><span class="sxs-lookup"><span data-stu-id="bef10-111">0x00008236</span></span>  <br/> |
|<span data-ttu-id="bef10-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="bef10-112">Data type:</span></span>  <br/> |<span data-ttu-id="bef10-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="bef10-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="bef10-114">Área:</span><span class="sxs-lookup"><span data-stu-id="bef10-114">Area:</span></span>  <br/> |<span data-ttu-id="bef10-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="bef10-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bef10-116">Notas</span><span class="sxs-lookup"><span data-stu-id="bef10-116">Remarks</span></span>

<span data-ttu-id="bef10-117">Para los objetos de calendario de una sola instancia, especifica la fecha de finalización y la hora del evento en UTC.</span><span class="sxs-lookup"><span data-stu-id="bef10-117">For single instance calendar objects, it specifies the end date and time of the event in UTC.</span></span> <span data-ttu-id="bef10-118">Para una serie periódica, esta propiedad especifica medianoche en la fecha de la última instancia de la serie periódica en UTC, a menos que la serie periódica no tiene fin, en el que caso el valor debe ser el 31 de agosto 4500, 11:59 p.m.</span><span class="sxs-lookup"><span data-stu-id="bef10-118">For a recurring series, this property specifies midnight on the date of the last instance of the recurring series in UTC, unless the recurring series has no end, in which case the value must be 31 August 4500, 11:59 p.m.</span></span>
  
<span data-ttu-id="bef10-119">El valor de esta propiedad debe establecerse en el valor de la **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bef10-119">The value of this property must be set to the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bef10-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bef10-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bef10-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="bef10-121">Protocol specifications</span></span>

<span data-ttu-id="bef10-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bef10-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bef10-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="bef10-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bef10-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bef10-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bef10-125">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="bef10-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bef10-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="bef10-126">Header files</span></span>

<span data-ttu-id="bef10-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bef10-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="bef10-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="bef10-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bef10-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="bef10-129">See also</span></span>



[<span data-ttu-id="bef10-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bef10-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bef10-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="bef10-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bef10-132">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="bef10-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bef10-133">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="bef10-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

