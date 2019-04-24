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
ms.openlocfilehash: 074bcf7c051b78bc32caf66502747e7fb1ab6b79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355289"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a><span data-ttu-id="593b0-103">Propiedad canónica PidTagRecipientTrackStatus</span><span class="sxs-lookup"><span data-stu-id="593b0-103">PidTagRecipientTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="593b0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="593b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="593b0-105">Indica el estado de respuesta devuelto por el asistente.</span><span class="sxs-lookup"><span data-stu-id="593b0-105">Indicates the response status returned by the attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="593b0-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="593b0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="593b0-107">PR_RECIPIENT_TRACKSTATUS</span><span class="sxs-lookup"><span data-stu-id="593b0-107">PR_RECIPIENT_TRACKSTATUS</span></span>  <br/> |
|<span data-ttu-id="593b0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="593b0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="593b0-109">0x5FFF</span><span class="sxs-lookup"><span data-stu-id="593b0-109">0x5FFF</span></span>  <br/> |
|<span data-ttu-id="593b0-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="593b0-110">Data type:</span></span>  <br/> |<span data-ttu-id="593b0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="593b0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="593b0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="593b0-112">Area:</span></span>  <br/> |<span data-ttu-id="593b0-113">Destinatario de transporte</span><span class="sxs-lookup"><span data-stu-id="593b0-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="593b0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="593b0-114">Remarks</span></span>

<span data-ttu-id="593b0-115">Si no se establece este valor, debe considerarse respNone.</span><span class="sxs-lookup"><span data-stu-id="593b0-115">If this value is not set, it must be assumed to be respNone.</span></span> <span data-ttu-id="593b0-116">De lo contrario, debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="593b0-116">Otherwise, it must be one of the following:</span></span>
  
|<span data-ttu-id="593b0-117">**Estado de respuesta**</span><span class="sxs-lookup"><span data-stu-id="593b0-117">**Response status**</span></span>|<span data-ttu-id="593b0-118">**Value**</span><span class="sxs-lookup"><span data-stu-id="593b0-118">**Value**</span></span>|<span data-ttu-id="593b0-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="593b0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="593b0-120">respNone</span><span class="sxs-lookup"><span data-stu-id="593b0-120">respNone</span></span>  <br/> |<span data-ttu-id="593b0-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="593b0-121">0x00000000</span></span>  <br/> |<span data-ttu-id="593b0-122">No se requiere respuesta para este objeto.</span><span class="sxs-lookup"><span data-stu-id="593b0-122">No response is required for this object.</span></span> <span data-ttu-id="593b0-123">Este es el caso de objetos de cita y objetos de respuesta a la reunión.</span><span class="sxs-lookup"><span data-stu-id="593b0-123">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="593b0-124">respTentative</span><span class="sxs-lookup"><span data-stu-id="593b0-124">respTentative</span></span>  <br/> |<span data-ttu-id="593b0-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="593b0-125">0x00000002</span></span>  <br/> |<span data-ttu-id="593b0-126">Este valor en el objeto de reunión del asistente indica que el asistente aceptó provisionalmente el objeto convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="593b0-126">This value on the attendee's meeting object indicates that the attendee has tentatively accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="593b0-127">respAccepted</span><span class="sxs-lookup"><span data-stu-id="593b0-127">respAccepted</span></span>  <br/> |<span data-ttu-id="593b0-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="593b0-128">0x00000003</span></span>  <br/> |<span data-ttu-id="593b0-129">Este valor en el objeto de reunión del asistente indica que el asistente ha aceptado el objeto convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="593b0-129">This value on the attendee's meeting object indicates that the attendee has accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="593b0-130">respDeclined</span><span class="sxs-lookup"><span data-stu-id="593b0-130">respDeclined</span></span>  <br/> |<span data-ttu-id="593b0-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="593b0-131">0x00000004</span></span>  <br/> |<span data-ttu-id="593b0-132">Este valor en el objeto de reunión del asistente indica que el asistente ha rechazado el objeto de convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="593b0-132">This value on the attendee's meeting object indicates that the attendee has declined the meeting request object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="593b0-133">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="593b0-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="593b0-134">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="593b0-134">Protocol specifications</span></span>

<span data-ttu-id="593b0-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="593b0-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="593b0-136">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="593b0-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="593b0-137">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="593b0-137">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="593b0-138">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="593b0-138">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="593b0-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="593b0-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="593b0-140">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="593b0-140">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="593b0-141">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="593b0-141">Header files</span></span>

<span data-ttu-id="593b0-142">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="593b0-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="593b0-143">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="593b0-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="593b0-144">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="593b0-144">Mapitags.h</span></span>
  
> <span data-ttu-id="593b0-145">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="593b0-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="593b0-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="593b0-146">See also</span></span>



[<span data-ttu-id="593b0-147">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="593b0-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="593b0-148">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="593b0-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="593b0-149">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="593b0-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="593b0-150">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="593b0-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

