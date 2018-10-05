---
title: Propiedad canónica PidLidResponseStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidResponseStatus
api_type:
- COM
ms.assetid: e56142fd-204b-497e-83b9-59f9acda6cb4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8c8e284752c6fd47eb7a8f227e2dbfeceebea596
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385014"
---
# <a name="pidlidresponsestatus-canonical-property"></a><span data-ttu-id="8c493-103">Propiedad canónica PidLidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="8c493-103">PidLidResponseStatus Canonical Property</span></span>

  
  
<span data-ttu-id="8c493-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c493-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c493-105">Especifica el estado de respuesta de un asistente.</span><span class="sxs-lookup"><span data-stu-id="8c493-105">Specifies the response status of an attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8c493-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8c493-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8c493-107">dispidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="8c493-107">dispidResponseStatus</span></span>  <br/> |
|<span data-ttu-id="8c493-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="8c493-108">Property set:</span></span>  <br/> |<span data-ttu-id="8c493-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="8c493-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="8c493-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="8c493-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8c493-111">0x00008218</span><span class="sxs-lookup"><span data-stu-id="8c493-111">0x00008218</span></span>  <br/> |
|<span data-ttu-id="8c493-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8c493-112">Data type:</span></span>  <br/> |<span data-ttu-id="8c493-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8c493-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8c493-114">Área:</span><span class="sxs-lookup"><span data-stu-id="8c493-114">Area:</span></span>  <br/> |<span data-ttu-id="8c493-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="8c493-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c493-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8c493-116">Remarks</span></span>

<span data-ttu-id="8c493-117">El estado de la respuesta debe ser uno de los valores en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8c493-117">The response status must be one of the values in the table below.</span></span>
  
|<span data-ttu-id="8c493-118">**Estado de la respuesta**</span><span class="sxs-lookup"><span data-stu-id="8c493-118">**Response status**</span></span>|<span data-ttu-id="8c493-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8c493-119">**Value**</span></span>|<span data-ttu-id="8c493-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8c493-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8c493-121">respNone</span><span class="sxs-lookup"><span data-stu-id="8c493-121">respNone</span></span>  <br/> |<span data-ttu-id="8c493-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c493-122">0x00000000</span></span>  <br/> |<span data-ttu-id="8c493-123">No hay respuesta es necesaria para este objeto.</span><span class="sxs-lookup"><span data-stu-id="8c493-123">No response is required for this object.</span></span> <span data-ttu-id="8c493-124">Este es el caso de objetos de citas y objetos de respuesta de la reunión.</span><span class="sxs-lookup"><span data-stu-id="8c493-124">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="8c493-125">respOrganized</span><span class="sxs-lookup"><span data-stu-id="8c493-125">respOrganized</span></span>  <br/> |<span data-ttu-id="8c493-126">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8c493-126">0x00000001</span></span>  <br/> |<span data-ttu-id="8c493-127">Al que pertenece el organizador de esta reunión.</span><span class="sxs-lookup"><span data-stu-id="8c493-127">This meeting belongs to the organizer.</span></span>  <br/> |
|<span data-ttu-id="8c493-128">respTentative</span><span class="sxs-lookup"><span data-stu-id="8c493-128">respTentative</span></span>  <br/> |<span data-ttu-id="8c493-129">0x00000002</span><span class="sxs-lookup"><span data-stu-id="8c493-129">0x00000002</span></span>  <br/> |<span data-ttu-id="8c493-130">Este valor en la reunión del asistente indica que el asistente ha aceptado provisionalmente la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="8c493-130">This value on the attendee's meeting indicates that the attendee has tentatively accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="8c493-131">respAccepted</span><span class="sxs-lookup"><span data-stu-id="8c493-131">respAccepted</span></span>  <br/> |<span data-ttu-id="8c493-132">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="8c493-132">0x00000003</span></span>  <br/> |<span data-ttu-id="8c493-133">Este valor en t de reunión del asistente indica que el asistente ha aceptado la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="8c493-133">This value on the attendee's meeting t indicates that the attendee has accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="8c493-134">respDeclined</span><span class="sxs-lookup"><span data-stu-id="8c493-134">respDeclined</span></span>  <br/> |<span data-ttu-id="8c493-135">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="8c493-135">0x00000004</span></span>  <br/> |<span data-ttu-id="8c493-136">Este valor en la reunión del asistente indica que el asistente ha rechazado la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="8c493-136">This value on the attendee's meeting indicates that the attendee has declined the meeting request.</span></span>  <br/> |
|<span data-ttu-id="8c493-137">respNotResponded</span><span class="sxs-lookup"><span data-stu-id="8c493-137">respNotResponded</span></span>  <br/> |<span data-ttu-id="8c493-138">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="8c493-138">0x00000005</span></span>  <br/> |<span data-ttu-id="8c493-139">Este valor en la reunión del asistente indica que el asistente no ha respondido.</span><span class="sxs-lookup"><span data-stu-id="8c493-139">This value on the attendee's meeting indicates the attendee has not yet responded.</span></span> <span data-ttu-id="8c493-140">Este valor se encuentra en la convocatoria de reunión, la actualización de la reunión y la cancelación de la reunión.</span><span class="sxs-lookup"><span data-stu-id="8c493-140">This value is on the meeting request, meeting update, and meeting cancelation.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="8c493-141">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8c493-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8c493-142">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="8c493-142">Protocol specifications</span></span>

<span data-ttu-id="8c493-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c493-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c493-144">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8c493-144">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8c493-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c493-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c493-146">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8c493-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8c493-147">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8c493-147">Header files</span></span>

<span data-ttu-id="8c493-148">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8c493-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="8c493-149">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8c493-149">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8c493-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c493-150">See also</span></span>



[<span data-ttu-id="8c493-151">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8c493-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8c493-152">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="8c493-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8c493-153">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8c493-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8c493-154">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="8c493-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

