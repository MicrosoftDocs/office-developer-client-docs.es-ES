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
# <a name="pidtagrecipienttrackstatus-canonical-property"></a><span data-ttu-id="a3844-103">Propiedad canónica PidTagRecipientTrackStatus</span><span class="sxs-lookup"><span data-stu-id="a3844-103">PidTagRecipientTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="a3844-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3844-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3844-105">Indica el estado de respuesta devuelto por el asistente.</span><span class="sxs-lookup"><span data-stu-id="a3844-105">Indicates the response status returned by the attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a3844-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a3844-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a3844-107">PR_RECIPIENT_TRACKSTATUS</span><span class="sxs-lookup"><span data-stu-id="a3844-107">PR_RECIPIENT_TRACKSTATUS</span></span>  <br/> |
|<span data-ttu-id="a3844-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a3844-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a3844-109">0x5FFF</span><span class="sxs-lookup"><span data-stu-id="a3844-109">0x5FFF</span></span>  <br/> |
|<span data-ttu-id="a3844-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a3844-110">Data type:</span></span>  <br/> |<span data-ttu-id="a3844-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a3844-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a3844-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a3844-112">Area:</span></span>  <br/> |<span data-ttu-id="a3844-113">Destinatario de transporte</span><span class="sxs-lookup"><span data-stu-id="a3844-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3844-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a3844-114">Remarks</span></span>

<span data-ttu-id="a3844-115">Si no se establece este valor, se debe asumir que es respNone.</span><span class="sxs-lookup"><span data-stu-id="a3844-115">If this value is not set, it must be assumed to be respNone.</span></span> <span data-ttu-id="a3844-116">De lo contrario, debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a3844-116">Otherwise, it must be one of the following:</span></span>
  
|<span data-ttu-id="a3844-117">**Estado de respuesta**</span><span class="sxs-lookup"><span data-stu-id="a3844-117">**Response status**</span></span>|<span data-ttu-id="a3844-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a3844-118">**Value**</span></span>|<span data-ttu-id="a3844-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a3844-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a3844-120">respNone</span><span class="sxs-lookup"><span data-stu-id="a3844-120">respNone</span></span>  <br/> |<span data-ttu-id="a3844-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3844-121">0x00000000</span></span>  <br/> |<span data-ttu-id="a3844-122">No se requiere ninguna respuesta para este objeto.</span><span class="sxs-lookup"><span data-stu-id="a3844-122">No response is required for this object.</span></span> <span data-ttu-id="a3844-123">Este es el caso de objetos de cita y objetos de respuesta de reunión.</span><span class="sxs-lookup"><span data-stu-id="a3844-123">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="a3844-124">respTentative</span><span class="sxs-lookup"><span data-stu-id="a3844-124">respTentative</span></span>  <br/> |<span data-ttu-id="a3844-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a3844-125">0x00000002</span></span>  <br/> |<span data-ttu-id="a3844-126">Este valor en el objeto de reunión del asistente indica que el asistente ha aceptado provisionalmente el objeto de solicitud de reunión.</span><span class="sxs-lookup"><span data-stu-id="a3844-126">This value on the attendee's meeting object indicates that the attendee has tentatively accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="a3844-127">respAccepted</span><span class="sxs-lookup"><span data-stu-id="a3844-127">respAccepted</span></span>  <br/> |<span data-ttu-id="a3844-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="a3844-128">0x00000003</span></span>  <br/> |<span data-ttu-id="a3844-129">Este valor en el objeto de reunión del asistente indica que el asistente ha aceptado el objeto de solicitud de reunión.</span><span class="sxs-lookup"><span data-stu-id="a3844-129">This value on the attendee's meeting object indicates that the attendee has accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="a3844-130">respDeclined</span><span class="sxs-lookup"><span data-stu-id="a3844-130">respDeclined</span></span>  <br/> |<span data-ttu-id="a3844-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="a3844-131">0x00000004</span></span>  <br/> |<span data-ttu-id="a3844-132">Este valor en el objeto de reunión del asistente indica que el asistente ha rechazado el objeto de solicitud de reunión.</span><span class="sxs-lookup"><span data-stu-id="a3844-132">This value on the attendee's meeting object indicates that the attendee has declined the meeting request object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a3844-133">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3844-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a3844-134">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="a3844-134">Protocol specifications</span></span>

<span data-ttu-id="a3844-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3844-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3844-136">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="a3844-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a3844-137">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3844-137">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3844-138">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="a3844-138">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="a3844-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3844-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3844-140">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a3844-140">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a3844-141">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a3844-141">Header files</span></span>

<span data-ttu-id="a3844-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a3844-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="a3844-143">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a3844-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="a3844-144">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a3844-144">Mapitags.h</span></span>
  
> <span data-ttu-id="a3844-145">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="a3844-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a3844-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3844-146">See also</span></span>



[<span data-ttu-id="a3844-147">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a3844-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a3844-148">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a3844-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a3844-149">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a3844-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a3844-150">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="a3844-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

