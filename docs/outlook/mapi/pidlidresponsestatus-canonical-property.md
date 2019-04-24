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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345762"
---
# <a name="pidlidresponsestatus-canonical-property"></a><span data-ttu-id="8aee1-103">Propiedad canónica PidLidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="8aee1-103">PidLidResponseStatus Canonical Property</span></span>

  
  
<span data-ttu-id="8aee1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8aee1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8aee1-105">Especifica el estado de respuesta de un asistente.</span><span class="sxs-lookup"><span data-stu-id="8aee1-105">Specifies the response status of an attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8aee1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8aee1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8aee1-107">dispidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="8aee1-107">dispidResponseStatus</span></span>  <br/> |
|<span data-ttu-id="8aee1-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="8aee1-108">Property set:</span></span>  <br/> |<span data-ttu-id="8aee1-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="8aee1-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="8aee1-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="8aee1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8aee1-111">0x00008218</span><span class="sxs-lookup"><span data-stu-id="8aee1-111">0x00008218</span></span>  <br/> |
|<span data-ttu-id="8aee1-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8aee1-112">Data type:</span></span>  <br/> |<span data-ttu-id="8aee1-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8aee1-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8aee1-114">Área:</span><span class="sxs-lookup"><span data-stu-id="8aee1-114">Area:</span></span>  <br/> |<span data-ttu-id="8aee1-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="8aee1-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8aee1-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8aee1-116">Remarks</span></span>

<span data-ttu-id="8aee1-117">El estado de respuesta debe ser uno de los valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8aee1-117">The response status must be one of the values in the table below.</span></span>
  
|<span data-ttu-id="8aee1-118">**Estado de respuesta**</span><span class="sxs-lookup"><span data-stu-id="8aee1-118">**Response status**</span></span>|<span data-ttu-id="8aee1-119">**Value**</span><span class="sxs-lookup"><span data-stu-id="8aee1-119">**Value**</span></span>|<span data-ttu-id="8aee1-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8aee1-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8aee1-121">respNone</span><span class="sxs-lookup"><span data-stu-id="8aee1-121">respNone</span></span>  <br/> |<span data-ttu-id="8aee1-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8aee1-122">0x00000000</span></span>  <br/> |<span data-ttu-id="8aee1-123">No se requiere respuesta para este objeto.</span><span class="sxs-lookup"><span data-stu-id="8aee1-123">No response is required for this object.</span></span> <span data-ttu-id="8aee1-124">Este es el caso de objetos de cita y objetos de respuesta a la reunión.</span><span class="sxs-lookup"><span data-stu-id="8aee1-124">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="8aee1-125">respOrganized</span><span class="sxs-lookup"><span data-stu-id="8aee1-125">respOrganized</span></span>  <br/> |<span data-ttu-id="8aee1-126">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8aee1-126">0x00000001</span></span>  <br/> |<span data-ttu-id="8aee1-127">Esta reunión pertenece al organizador.</span><span class="sxs-lookup"><span data-stu-id="8aee1-127">This meeting belongs to the organizer.</span></span>  <br/> |
|<span data-ttu-id="8aee1-128">respTentative</span><span class="sxs-lookup"><span data-stu-id="8aee1-128">respTentative</span></span>  <br/> |<span data-ttu-id="8aee1-129">0x00000002</span><span class="sxs-lookup"><span data-stu-id="8aee1-129">0x00000002</span></span>  <br/> |<span data-ttu-id="8aee1-130">Este valor en la reunión del asistente indica que el asistente aceptó provisionalmente la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="8aee1-130">This value on the attendee's meeting indicates that the attendee has tentatively accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="8aee1-131">respAccepted</span><span class="sxs-lookup"><span data-stu-id="8aee1-131">respAccepted</span></span>  <br/> |<span data-ttu-id="8aee1-132">0x00000003</span><span class="sxs-lookup"><span data-stu-id="8aee1-132">0x00000003</span></span>  <br/> |<span data-ttu-id="8aee1-133">Este valor en la reunión del asistente t indica que el asistente ha aceptado la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="8aee1-133">This value on the attendee's meeting t indicates that the attendee has accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="8aee1-134">respDeclined</span><span class="sxs-lookup"><span data-stu-id="8aee1-134">respDeclined</span></span>  <br/> |<span data-ttu-id="8aee1-135">0x00000004</span><span class="sxs-lookup"><span data-stu-id="8aee1-135">0x00000004</span></span>  <br/> |<span data-ttu-id="8aee1-136">Este valor en la reunión del asistente indica que el asistente ha rechazado la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="8aee1-136">This value on the attendee's meeting indicates that the attendee has declined the meeting request.</span></span>  <br/> |
|<span data-ttu-id="8aee1-137">respNotResponded</span><span class="sxs-lookup"><span data-stu-id="8aee1-137">respNotResponded</span></span>  <br/> |<span data-ttu-id="8aee1-138">0x00000005</span><span class="sxs-lookup"><span data-stu-id="8aee1-138">0x00000005</span></span>  <br/> |<span data-ttu-id="8aee1-139">Este valor en la reunión del asistente indica que el asistente todavía no ha respondido.</span><span class="sxs-lookup"><span data-stu-id="8aee1-139">This value on the attendee's meeting indicates the attendee has not yet responded.</span></span> <span data-ttu-id="8aee1-140">Este valor se encuentra en la convocatoria de reunión, la actualización de la reunión y la cancelación de la reunión.</span><span class="sxs-lookup"><span data-stu-id="8aee1-140">This value is on the meeting request, meeting update, and meeting cancelation.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="8aee1-141">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8aee1-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8aee1-142">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="8aee1-142">Protocol specifications</span></span>

<span data-ttu-id="8aee1-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8aee1-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8aee1-144">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8aee1-144">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8aee1-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8aee1-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8aee1-146">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8aee1-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8aee1-147">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8aee1-147">Header files</span></span>

<span data-ttu-id="8aee1-148">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8aee1-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="8aee1-149">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8aee1-149">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8aee1-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="8aee1-150">See also</span></span>



[<span data-ttu-id="8aee1-151">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8aee1-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8aee1-152">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="8aee1-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8aee1-153">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8aee1-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8aee1-154">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="8aee1-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

