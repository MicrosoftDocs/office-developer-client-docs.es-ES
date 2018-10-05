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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386302"
---
# <a name="pidlidrecurrencepattern-canonical-property"></a><span data-ttu-id="37c75-103">Propiedad canónica PidLidRecurrencePattern</span><span class="sxs-lookup"><span data-stu-id="37c75-103">PidLidRecurrencePattern Canonical Property</span></span>

  
  
<span data-ttu-id="37c75-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37c75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37c75-105">Especifica una descripción del patrón de frecuencia del objeto de calendario.</span><span class="sxs-lookup"><span data-stu-id="37c75-105">Specifies a description of the recurrence pattern of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="37c75-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="37c75-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="37c75-107">dispidRecurPattern</span><span class="sxs-lookup"><span data-stu-id="37c75-107">dispidRecurPattern</span></span>  <br/> |
|<span data-ttu-id="37c75-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="37c75-108">Property set:</span></span>  <br/> |<span data-ttu-id="37c75-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="37c75-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="37c75-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="37c75-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="37c75-111">0x00008232</span><span class="sxs-lookup"><span data-stu-id="37c75-111">0x00008232</span></span>  <br/> |
|<span data-ttu-id="37c75-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="37c75-112">Data type:</span></span>  <br/> |<span data-ttu-id="37c75-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="37c75-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="37c75-114">Área:</span><span class="sxs-lookup"><span data-stu-id="37c75-114">Area:</span></span>  <br/> |<span data-ttu-id="37c75-115">Calendario</span><span class="sxs-lookup"><span data-stu-id="37c75-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37c75-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="37c75-116">Remarks</span></span>

<span data-ttu-id="37c75-117">Si se establece esta propiedad, se debe establecer para una descripción de la repetición que se especifica mediante la propiedad **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="37c75-117">If this property is set, it must be set to a description of the recurrence that is specified by the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="37c75-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="37c75-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="37c75-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="37c75-119">Protocol specifications</span></span>

<span data-ttu-id="37c75-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37c75-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37c75-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="37c75-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="37c75-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37c75-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37c75-123">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="37c75-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="37c75-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="37c75-124">Header files</span></span>

<span data-ttu-id="37c75-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="37c75-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="37c75-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="37c75-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="37c75-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="37c75-127">See also</span></span>



[<span data-ttu-id="37c75-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="37c75-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="37c75-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="37c75-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="37c75-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="37c75-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="37c75-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="37c75-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

