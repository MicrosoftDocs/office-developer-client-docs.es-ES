---
title: Propiedad canónica PidLidClipEnd
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 71a0a50f26b26d65ed34f38c2a0c7f930e6082a8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386071"
---
# <a name="pidlidclipend-canonical-property"></a><span data-ttu-id="a42b7-103">Propiedad canónica PidLidClipEnd</span><span class="sxs-lookup"><span data-stu-id="a42b7-103">PidLidClipEnd Canonical Property</span></span>

  
  
<span data-ttu-id="a42b7-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a42b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a42b7-105">Especifica la fecha de finalización y la hora del evento en hora Universal coordinada (UTC) para los objetos de calendario de una sola instancia.</span><span class="sxs-lookup"><span data-stu-id="a42b7-105">Specifies the end date and time of the event in Coordinated Universal Time (UTC) for single instance calendar objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a42b7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a42b7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a42b7-107">dispidClipEnd</span><span class="sxs-lookup"><span data-stu-id="a42b7-107">dispidClipEnd</span></span>  <br/> |
|<span data-ttu-id="a42b7-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="a42b7-108">Property set:</span></span>  <br/> |<span data-ttu-id="a42b7-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="a42b7-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="a42b7-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="a42b7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a42b7-111">0x00008236</span><span class="sxs-lookup"><span data-stu-id="a42b7-111">0x00008236</span></span>  <br/> |
|<span data-ttu-id="a42b7-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a42b7-112">Data type:</span></span>  <br/> |<span data-ttu-id="a42b7-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="a42b7-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="a42b7-114">Área:</span><span class="sxs-lookup"><span data-stu-id="a42b7-114">Area:</span></span>  <br/> |<span data-ttu-id="a42b7-115">Calendario</span><span class="sxs-lookup"><span data-stu-id="a42b7-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a42b7-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a42b7-116">Remarks</span></span>

<span data-ttu-id="a42b7-117">Para los objetos de calendario de una sola instancia, especifica la fecha de finalización y la hora del evento en UTC.</span><span class="sxs-lookup"><span data-stu-id="a42b7-117">For single instance calendar objects, it specifies the end date and time of the event in UTC.</span></span> <span data-ttu-id="a42b7-118">Para una serie periódica, esta propiedad especifica medianoche en la fecha de la última instancia de la serie periódica en UTC, a menos que la serie periódica no tiene fin, en el que caso el valor debe ser el 31 de agosto 4500, 11:59 p.m.</span><span class="sxs-lookup"><span data-stu-id="a42b7-118">For a recurring series, this property specifies midnight on the date of the last instance of the recurring series in UTC, unless the recurring series has no end, in which case the value must be 31 August 4500, 11:59 p.m.</span></span>
  
<span data-ttu-id="a42b7-119">El valor de esta propiedad debe establecerse en el valor de la **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a42b7-119">The value of this property must be set to the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a42b7-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a42b7-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a42b7-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="a42b7-121">Protocol specifications</span></span>

<span data-ttu-id="a42b7-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a42b7-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a42b7-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a42b7-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a42b7-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a42b7-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a42b7-125">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="a42b7-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a42b7-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a42b7-126">Header files</span></span>

<span data-ttu-id="a42b7-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a42b7-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="a42b7-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a42b7-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a42b7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a42b7-129">See also</span></span>



[<span data-ttu-id="a42b7-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a42b7-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a42b7-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="a42b7-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a42b7-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a42b7-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a42b7-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="a42b7-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

