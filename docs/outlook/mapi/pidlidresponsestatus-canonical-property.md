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
# <a name="pidlidresponsestatus-canonical-property"></a><span data-ttu-id="4446e-103">Propiedad canónica PidLidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="4446e-103">PidLidResponseStatus Canonical Property</span></span>

  
  
<span data-ttu-id="4446e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4446e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4446e-105">Especifica el estado de respuesta de un asistente.</span><span class="sxs-lookup"><span data-stu-id="4446e-105">Specifies the response status of an attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4446e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4446e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4446e-107">dispidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="4446e-107">dispidResponseStatus</span></span>  <br/> |
|<span data-ttu-id="4446e-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="4446e-108">Property set:</span></span>  <br/> |<span data-ttu-id="4446e-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="4446e-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="4446e-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="4446e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4446e-111">0x00008218</span><span class="sxs-lookup"><span data-stu-id="4446e-111">0x00008218</span></span>  <br/> |
|<span data-ttu-id="4446e-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4446e-112">Data type:</span></span>  <br/> |<span data-ttu-id="4446e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4446e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4446e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="4446e-114">Area:</span></span>  <br/> |<span data-ttu-id="4446e-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="4446e-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4446e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4446e-116">Remarks</span></span>

<span data-ttu-id="4446e-117">El estado de la respuesta debe ser uno de los valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="4446e-117">The response status must be one of the values in the table below.</span></span>
  
|<span data-ttu-id="4446e-118">**Estado de respuesta**</span><span class="sxs-lookup"><span data-stu-id="4446e-118">**Response status**</span></span>|<span data-ttu-id="4446e-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4446e-119">**Value**</span></span>|<span data-ttu-id="4446e-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4446e-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4446e-121">respNone</span><span class="sxs-lookup"><span data-stu-id="4446e-121">respNone</span></span>  <br/> |<span data-ttu-id="4446e-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4446e-122">0x00000000</span></span>  <br/> |<span data-ttu-id="4446e-123">No se requiere ninguna respuesta para este objeto.</span><span class="sxs-lookup"><span data-stu-id="4446e-123">No response is required for this object.</span></span> <span data-ttu-id="4446e-124">Este es el caso de objetos de cita y objetos de respuesta de reunión.</span><span class="sxs-lookup"><span data-stu-id="4446e-124">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="4446e-125">respOrganized</span><span class="sxs-lookup"><span data-stu-id="4446e-125">respOrganized</span></span>  <br/> |<span data-ttu-id="4446e-126">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4446e-126">0x00000001</span></span>  <br/> |<span data-ttu-id="4446e-127">Esta reunión pertenece al organizador.</span><span class="sxs-lookup"><span data-stu-id="4446e-127">This meeting belongs to the organizer.</span></span>  <br/> |
|<span data-ttu-id="4446e-128">respTentative</span><span class="sxs-lookup"><span data-stu-id="4446e-128">respTentative</span></span>  <br/> |<span data-ttu-id="4446e-129">0x00000002</span><span class="sxs-lookup"><span data-stu-id="4446e-129">0x00000002</span></span>  <br/> |<span data-ttu-id="4446e-130">Este valor en la reunión del asistente indica que el asistente ha aceptado provisionalmente la solicitud de reunión.</span><span class="sxs-lookup"><span data-stu-id="4446e-130">This value on the attendee's meeting indicates that the attendee has tentatively accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="4446e-131">respAccepted</span><span class="sxs-lookup"><span data-stu-id="4446e-131">respAccepted</span></span>  <br/> |<span data-ttu-id="4446e-132">0x00000003</span><span class="sxs-lookup"><span data-stu-id="4446e-132">0x00000003</span></span>  <br/> |<span data-ttu-id="4446e-133">Este valor en la reunión del asistente t indica que el asistente ha aceptado la solicitud de reunión.</span><span class="sxs-lookup"><span data-stu-id="4446e-133">This value on the attendee's meeting t indicates that the attendee has accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="4446e-134">respDeclined</span><span class="sxs-lookup"><span data-stu-id="4446e-134">respDeclined</span></span>  <br/> |<span data-ttu-id="4446e-135">0x00000004</span><span class="sxs-lookup"><span data-stu-id="4446e-135">0x00000004</span></span>  <br/> |<span data-ttu-id="4446e-136">Este valor en la reunión del asistente indica que el asistente ha rechazado la solicitud de reunión.</span><span class="sxs-lookup"><span data-stu-id="4446e-136">This value on the attendee's meeting indicates that the attendee has declined the meeting request.</span></span>  <br/> |
|<span data-ttu-id="4446e-137">respNotResponded</span><span class="sxs-lookup"><span data-stu-id="4446e-137">respNotResponded</span></span>  <br/> |<span data-ttu-id="4446e-138">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4446e-138">0x00000005</span></span>  <br/> |<span data-ttu-id="4446e-139">Este valor en la reunión del asistente indica que el asistente aún no ha respondido.</span><span class="sxs-lookup"><span data-stu-id="4446e-139">This value on the attendee's meeting indicates the attendee has not yet responded.</span></span> <span data-ttu-id="4446e-140">Este valor se encuentra en la solicitud de reunión, la actualización de la reunión y la cancelación de la reunión.</span><span class="sxs-lookup"><span data-stu-id="4446e-140">This value is on the meeting request, meeting update, and meeting cancelation.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4446e-141">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4446e-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4446e-142">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="4446e-142">Protocol specifications</span></span>

<span data-ttu-id="4446e-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4446e-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4446e-144">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="4446e-144">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4446e-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4446e-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4446e-146">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="4446e-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4446e-147">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4446e-147">Header files</span></span>

<span data-ttu-id="4446e-148">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4446e-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="4446e-149">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4446e-149">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4446e-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="4446e-150">See also</span></span>



[<span data-ttu-id="4446e-151">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4446e-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4446e-152">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="4446e-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4446e-153">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4446e-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4446e-154">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="4446e-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

