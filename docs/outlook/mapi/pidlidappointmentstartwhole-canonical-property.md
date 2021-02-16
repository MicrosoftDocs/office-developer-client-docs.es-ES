---
title: Propiedad canónica PidLidAppointmentStartWhole
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6f9fb9c3f02e66fd01e89742edcfba7391c36e3e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345377"
---
# <a name="pidlidappointmentstartwhole-canonical-property"></a><span data-ttu-id="f4ad3-103">Propiedad canónica PidLidAppointmentStartWhole</span><span class="sxs-lookup"><span data-stu-id="f4ad3-103">PidLidAppointmentStartWhole Canonical Property</span></span>

  
  
<span data-ttu-id="f4ad3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4ad3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4ad3-105">Representa la fecha y la hora en que comienza una cita.</span><span class="sxs-lookup"><span data-stu-id="f4ad3-105">Represents the date and time when an appointment begins.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f4ad3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f4ad3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4ad3-107">dispidApptStartWhole</span><span class="sxs-lookup"><span data-stu-id="f4ad3-107">dispidApptStartWhole</span></span>  <br/> |
|<span data-ttu-id="f4ad3-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="f4ad3-108">Property set:</span></span>  <br/> |<span data-ttu-id="f4ad3-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="f4ad3-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="f4ad3-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="f4ad3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f4ad3-111">0x0000820D</span><span class="sxs-lookup"><span data-stu-id="f4ad3-111">0x0000820D</span></span>  <br/> |
|<span data-ttu-id="f4ad3-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f4ad3-112">Data type:</span></span>  <br/> |<span data-ttu-id="f4ad3-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="f4ad3-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="f4ad3-114">Área:</span><span class="sxs-lookup"><span data-stu-id="f4ad3-114">Area:</span></span>  <br/> |<span data-ttu-id="f4ad3-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="f4ad3-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4ad3-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f4ad3-116">Remarks</span></span>

<span data-ttu-id="f4ad3-117">Esta propiedad especifica la fecha y hora de inicio del evento.</span><span class="sxs-lookup"><span data-stu-id="f4ad3-117">This property specifies the start date and time of the event.</span></span> <span data-ttu-id="f4ad3-118">Esta propiedad debe estar en hora universal coordinada (UTC) y debe ser menor que el valor de la propiedad **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f4ad3-118">This property must be in Coordinated Universal Time (UTC) and must be less than the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="f4ad3-119">Para una serie periódica, esta propiedad es la fecha y hora de inicio de la primera instancia según el patrón de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="f4ad3-119">For a recurring series, this property is the start date and time of the first instance according to the recurrence pattern.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f4ad3-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f4ad3-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f4ad3-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="f4ad3-121">Protocol specifications</span></span>

<span data-ttu-id="f4ad3-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4ad3-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4ad3-123">Proporciona la definición del conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="f4ad3-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f4ad3-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4ad3-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4ad3-125">Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.</span><span class="sxs-lookup"><span data-stu-id="f4ad3-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f4ad3-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f4ad3-126">Header files</span></span>

<span data-ttu-id="f4ad3-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4ad3-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4ad3-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f4ad3-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4ad3-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f4ad3-129">See also</span></span>



[<span data-ttu-id="f4ad3-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f4ad3-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4ad3-131">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="f4ad3-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4ad3-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f4ad3-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4ad3-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="f4ad3-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

