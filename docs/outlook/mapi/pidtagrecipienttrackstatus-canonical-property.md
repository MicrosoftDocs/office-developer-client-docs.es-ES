---
title: Propiedad canónico PidTagRecipientTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientTrackStatus
api_type:
- COM
ms.assetid: d619b5e7-2867-44fc-9b42-123bb1bf7bde
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: cbc934eec5331a0302ba222108ee92a0dc696b1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820061"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a><span data-ttu-id="a5ac2-103">Propiedad canónico PidTagRecipientTrackStatus</span><span class="sxs-lookup"><span data-stu-id="a5ac2-103">PidTagRecipientTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="a5ac2-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a5ac2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a5ac2-105">Indica el estado de respuesta devuelto por el asistente.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-105">Indicates the response status returned by the attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5ac2-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a5ac2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5ac2-107">PR_RECIPIENT_TRACKSTATUS</span><span class="sxs-lookup"><span data-stu-id="a5ac2-107">PR_RECIPIENT_TRACKSTATUS</span></span>  <br/> |
|<span data-ttu-id="a5ac2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a5ac2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a5ac2-109">0x5FFF</span><span class="sxs-lookup"><span data-stu-id="a5ac2-109">0x5FFF</span></span>  <br/> |
|<span data-ttu-id="a5ac2-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a5ac2-110">Data type:</span></span>  <br/> |<span data-ttu-id="a5ac2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a5ac2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a5ac2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a5ac2-112">Area:</span></span>  <br/> |<span data-ttu-id="a5ac2-113">Destinatario del transporte</span><span class="sxs-lookup"><span data-stu-id="a5ac2-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5ac2-114">Notas</span><span class="sxs-lookup"><span data-stu-id="a5ac2-114">Remarks</span></span>

<span data-ttu-id="a5ac2-115">Si no se establece este valor, debe ser supone que ésta respNone.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-115">If this value is not set, it must be assumed to be respNone.</span></span> <span data-ttu-id="a5ac2-116">De lo contrario, debe ser uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="a5ac2-116">Otherwise, it must be one of the following:</span></span>
  
|<span data-ttu-id="a5ac2-117">**Estado de la respuesta**</span><span class="sxs-lookup"><span data-stu-id="a5ac2-117">**Response status**</span></span>|<span data-ttu-id="a5ac2-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a5ac2-118">**Value**</span></span>|<span data-ttu-id="a5ac2-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a5ac2-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a5ac2-120">respNone</span><span class="sxs-lookup"><span data-stu-id="a5ac2-120">respNone</span></span>  <br/> |<span data-ttu-id="a5ac2-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5ac2-121">0x00000000</span></span>  <br/> |<span data-ttu-id="a5ac2-122">No hay respuesta es necesaria para este objeto.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-122">No response is required for this object.</span></span> <span data-ttu-id="a5ac2-123">Este es el caso de objetos de citas y objetos de respuesta de la reunión.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-123">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="a5ac2-124">respTentative</span><span class="sxs-lookup"><span data-stu-id="a5ac2-124">respTentative</span></span>  <br/> |<span data-ttu-id="a5ac2-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a5ac2-125">0x00000002</span></span>  <br/> |<span data-ttu-id="a5ac2-126">Este valor en el objeto de reunión del asistente indica que el asistente ha aceptado provisionalmente la reunión objeto de solicitud.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-126">This value on the attendee's meeting object indicates that the attendee has tentatively accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="a5ac2-127">respAccepted</span><span class="sxs-lookup"><span data-stu-id="a5ac2-127">respAccepted</span></span>  <br/> |<span data-ttu-id="a5ac2-128">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="a5ac2-128">0x00000003</span></span>  <br/> |<span data-ttu-id="a5ac2-129">Este valor en el objeto de reunión del asistente indica que el asistente ha aceptado la reunión objeto de solicitud.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-129">This value on the attendee's meeting object indicates that the attendee has accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="a5ac2-130">respDeclined</span><span class="sxs-lookup"><span data-stu-id="a5ac2-130">respDeclined</span></span>  <br/> |<span data-ttu-id="a5ac2-131">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="a5ac2-131">0x00000004</span></span>  <br/> |<span data-ttu-id="a5ac2-132">Este valor en el objeto de reunión del asistente indica que el asistente ha rechazado la reunión objeto de solicitud.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-132">This value on the attendee's meeting object indicates that the attendee has declined the meeting request object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a5ac2-133">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a5ac2-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a5ac2-134">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="a5ac2-134">Protocol specifications</span></span>

<span data-ttu-id="a5ac2-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5ac2-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5ac2-136">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a5ac2-137">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5ac2-137">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5ac2-138">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-138">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="a5ac2-139">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5ac2-139">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5ac2-140">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-140">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a5ac2-141">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a5ac2-141">Header files</span></span>

<span data-ttu-id="a5ac2-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5ac2-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="a5ac2-143">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="a5ac2-144">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a5ac2-144">Mapitags.h</span></span>
  
> <span data-ttu-id="a5ac2-145">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5ac2-146">Ver también</span><span class="sxs-lookup"><span data-stu-id="a5ac2-146">See also</span></span>



[<span data-ttu-id="a5ac2-147">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a5ac2-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5ac2-148">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="a5ac2-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5ac2-149">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="a5ac2-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5ac2-150">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a5ac2-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

