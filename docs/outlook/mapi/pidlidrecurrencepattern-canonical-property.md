---
title: Propiedad canónica PidLidRecurrencePattern
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurrencePattern
api_type:
- COM
ms.assetid: ac21ba98-f16b-4365-9134-bca7748189ee
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d94ac430df54fc03d96ac761c53ca20201d899c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315935"
---
# <a name="pidlidrecurrencepattern-canonical-property"></a><span data-ttu-id="8c0c5-103">Propiedad canónica PidLidRecurrencePattern</span><span class="sxs-lookup"><span data-stu-id="8c0c5-103">PidLidRecurrencePattern Canonical Property</span></span>

  
  
<span data-ttu-id="8c0c5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c0c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c0c5-105">Especifica una descripción del patrón de periodicidad del objeto calendar.</span><span class="sxs-lookup"><span data-stu-id="8c0c5-105">Specifies a description of the recurrence pattern of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8c0c5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8c0c5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8c0c5-107">dispidRecurPattern</span><span class="sxs-lookup"><span data-stu-id="8c0c5-107">dispidRecurPattern</span></span>  <br/> |
|<span data-ttu-id="8c0c5-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="8c0c5-108">Property set:</span></span>  <br/> |<span data-ttu-id="8c0c5-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="8c0c5-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="8c0c5-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="8c0c5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8c0c5-111">0x00008232</span><span class="sxs-lookup"><span data-stu-id="8c0c5-111">0x00008232</span></span>  <br/> |
|<span data-ttu-id="8c0c5-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8c0c5-112">Data type:</span></span>  <br/> |<span data-ttu-id="8c0c5-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8c0c5-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8c0c5-114">Área:</span><span class="sxs-lookup"><span data-stu-id="8c0c5-114">Area:</span></span>  <br/> |<span data-ttu-id="8c0c5-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="8c0c5-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c0c5-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8c0c5-116">Remarks</span></span>

<span data-ttu-id="8c0c5-117">Si se establece esta propiedad, debe establecerse en una descripción de la periodicidad especificada por la **propiedad dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8c0c5-117">If this property is set, it must be set to a description of the recurrence that is specified by the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8c0c5-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8c0c5-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8c0c5-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="8c0c5-119">Protocol specifications</span></span>

<span data-ttu-id="8c0c5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c0c5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c0c5-121">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="8c0c5-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8c0c5-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c0c5-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c0c5-123">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="8c0c5-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8c0c5-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8c0c5-124">Header files</span></span>

<span data-ttu-id="8c0c5-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8c0c5-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8c0c5-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8c0c5-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8c0c5-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c0c5-127">See also</span></span>



[<span data-ttu-id="8c0c5-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8c0c5-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8c0c5-129">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="8c0c5-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8c0c5-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8c0c5-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8c0c5-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="8c0c5-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

