---
title: Propiedad canónica PidTagRecipientTrackStatus
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cbc934eec5331a0302ba222108ee92a0dc696b1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820061"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a><span data-ttu-id="74da5-103">Propiedad canónica PidTagRecipientTrackStatus</span><span class="sxs-lookup"><span data-stu-id="74da5-103">PidTagRecipientTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="74da5-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="74da5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="74da5-105">Indica el estado de respuesta devuelto por el asistente.</span><span class="sxs-lookup"><span data-stu-id="74da5-105">Indicates the response status returned by the attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74da5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="74da5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="74da5-107">PR_RECIPIENT_TRACKSTATUS</span><span class="sxs-lookup"><span data-stu-id="74da5-107">PR_RECIPIENT_TRACKSTATUS</span></span>  <br/> |
|<span data-ttu-id="74da5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="74da5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="74da5-109">0x5FFF</span><span class="sxs-lookup"><span data-stu-id="74da5-109">0x5FFF</span></span>  <br/> |
|<span data-ttu-id="74da5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="74da5-110">Data type:</span></span>  <br/> |<span data-ttu-id="74da5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="74da5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="74da5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="74da5-112">Area:</span></span>  <br/> |<span data-ttu-id="74da5-113">Destinatario del transporte</span><span class="sxs-lookup"><span data-stu-id="74da5-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74da5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="74da5-114">Remarks</span></span>

<span data-ttu-id="74da5-115">Si no se establece este valor, debe ser supone que ésta respNone.</span><span class="sxs-lookup"><span data-stu-id="74da5-115">If this value is not set, it must be assumed to be respNone.</span></span> <span data-ttu-id="74da5-116">De lo contrario, debe ser uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="74da5-116">Otherwise, it must be one of the following:</span></span>
  
|<span data-ttu-id="74da5-117">**Estado de la respuesta**</span><span class="sxs-lookup"><span data-stu-id="74da5-117">**Response status**</span></span>|<span data-ttu-id="74da5-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="74da5-118">**Value**</span></span>|<span data-ttu-id="74da5-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="74da5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="74da5-120">respNone</span><span class="sxs-lookup"><span data-stu-id="74da5-120">respNone</span></span>  <br/> |<span data-ttu-id="74da5-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74da5-121">0x00000000</span></span>  <br/> |<span data-ttu-id="74da5-122">No hay respuesta es necesaria para este objeto.</span><span class="sxs-lookup"><span data-stu-id="74da5-122">No response is required for this object.</span></span> <span data-ttu-id="74da5-123">Este es el caso de objetos de citas y objetos de respuesta de la reunión.</span><span class="sxs-lookup"><span data-stu-id="74da5-123">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="74da5-124">respTentative</span><span class="sxs-lookup"><span data-stu-id="74da5-124">respTentative</span></span>  <br/> |<span data-ttu-id="74da5-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="74da5-125">0x00000002</span></span>  <br/> |<span data-ttu-id="74da5-126">Este valor en el objeto de reunión del asistente indica que el asistente ha aceptado provisionalmente la reunión objeto de solicitud.</span><span class="sxs-lookup"><span data-stu-id="74da5-126">This value on the attendee's meeting object indicates that the attendee has tentatively accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="74da5-127">respAccepted</span><span class="sxs-lookup"><span data-stu-id="74da5-127">respAccepted</span></span>  <br/> |<span data-ttu-id="74da5-128">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="74da5-128">0x00000003</span></span>  <br/> |<span data-ttu-id="74da5-129">Este valor en el objeto de reunión del asistente indica que el asistente ha aceptado la reunión objeto de solicitud.</span><span class="sxs-lookup"><span data-stu-id="74da5-129">This value on the attendee's meeting object indicates that the attendee has accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="74da5-130">respDeclined</span><span class="sxs-lookup"><span data-stu-id="74da5-130">respDeclined</span></span>  <br/> |<span data-ttu-id="74da5-131">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="74da5-131">0x00000004</span></span>  <br/> |<span data-ttu-id="74da5-132">Este valor en el objeto de reunión del asistente indica que el asistente ha rechazado la reunión objeto de solicitud.</span><span class="sxs-lookup"><span data-stu-id="74da5-132">This value on the attendee's meeting object indicates that the attendee has declined the meeting request object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="74da5-133">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="74da5-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="74da5-134">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="74da5-134">Protocol specifications</span></span>

<span data-ttu-id="74da5-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74da5-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74da5-136">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="74da5-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="74da5-137">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74da5-137">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74da5-138">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="74da5-138">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="74da5-139">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74da5-139">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74da5-140">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="74da5-140">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="74da5-141">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="74da5-141">Header files</span></span>

<span data-ttu-id="74da5-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74da5-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="74da5-143">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="74da5-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="74da5-144">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="74da5-144">Mapitags.h</span></span>
  
> <span data-ttu-id="74da5-145">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="74da5-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74da5-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="74da5-146">See also</span></span>



[<span data-ttu-id="74da5-147">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="74da5-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="74da5-148">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="74da5-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="74da5-149">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="74da5-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="74da5-150">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="74da5-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

