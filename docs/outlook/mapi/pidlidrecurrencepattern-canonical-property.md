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
ms.openlocfilehash: 94656a1444149efeb6e2e9cd3a239ff14fa46937
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818849"
---
# <a name="pidlidrecurrencepattern-canonical-property"></a><span data-ttu-id="53933-103">Propiedad canónica PidLidRecurrencePattern</span><span class="sxs-lookup"><span data-stu-id="53933-103">PidLidRecurrencePattern Canonical Property</span></span>

  
  
<span data-ttu-id="53933-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="53933-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="53933-105">Especifica una descripción del patrón de frecuencia del objeto de calendario.</span><span class="sxs-lookup"><span data-stu-id="53933-105">Specifies a description of the recurrence pattern of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="53933-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="53933-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="53933-107">dispidRecurPattern</span><span class="sxs-lookup"><span data-stu-id="53933-107">dispidRecurPattern</span></span>  <br/> |
|<span data-ttu-id="53933-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="53933-108">Property set:</span></span>  <br/> |<span data-ttu-id="53933-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="53933-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="53933-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="53933-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="53933-111">0x00008232</span><span class="sxs-lookup"><span data-stu-id="53933-111">0x00008232</span></span>  <br/> |
|<span data-ttu-id="53933-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="53933-112">Data type:</span></span>  <br/> |<span data-ttu-id="53933-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="53933-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="53933-114">Área:</span><span class="sxs-lookup"><span data-stu-id="53933-114">Area:</span></span>  <br/> |<span data-ttu-id="53933-115">Calendario</span><span class="sxs-lookup"><span data-stu-id="53933-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53933-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="53933-116">Remarks</span></span>

<span data-ttu-id="53933-117">Si se establece esta propiedad, se debe establecer para una descripción de la repetición que se especifica mediante la propiedad **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="53933-117">If this property is set, it must be set to a description of the recurrence that is specified by the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="53933-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="53933-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="53933-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="53933-119">Protocol specifications</span></span>

<span data-ttu-id="53933-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53933-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53933-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="53933-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="53933-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53933-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53933-123">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="53933-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="53933-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="53933-124">Header files</span></span>

<span data-ttu-id="53933-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53933-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="53933-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="53933-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53933-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="53933-127">See also</span></span>



[<span data-ttu-id="53933-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="53933-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="53933-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="53933-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="53933-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="53933-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="53933-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="53933-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

