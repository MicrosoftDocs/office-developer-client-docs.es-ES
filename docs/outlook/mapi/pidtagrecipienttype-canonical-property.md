---
title: Propiedad canónica PidTagRecipientType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientType
api_type:
- COM
ms.assetid: 67e31027-6bc2-4a40-9b00-d61baef4ab0f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9d74fdb3acb6db94078d6090f0def050fb564cd9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385847"
---
# <a name="pidtagrecipienttype-canonical-property"></a><span data-ttu-id="55434-103">Propiedad canónica PidTagRecipientType</span><span class="sxs-lookup"><span data-stu-id="55434-103">PidTagRecipientType Canonical Property</span></span>

  
  
<span data-ttu-id="55434-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55434-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55434-105">Contiene el tipo de destinatario para un destinatario del mensaje.</span><span class="sxs-lookup"><span data-stu-id="55434-105">Contains the recipient type for a message recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55434-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="55434-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="55434-107">PR_RECIPIENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="55434-107">PR_RECIPIENT_TYPE</span></span>  <br/> |
|<span data-ttu-id="55434-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="55434-108">Identifier:</span></span>  <br/> |<span data-ttu-id="55434-109">0x0C15</span><span class="sxs-lookup"><span data-stu-id="55434-109">0x0C15</span></span>  <br/> |
|<span data-ttu-id="55434-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="55434-110">Data type:</span></span>  <br/> |<span data-ttu-id="55434-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="55434-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="55434-112">Área:</span><span class="sxs-lookup"><span data-stu-id="55434-112">Area:</span></span>  <br/> |<span data-ttu-id="55434-113">Destinatario MAPI</span><span class="sxs-lookup"><span data-stu-id="55434-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55434-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="55434-114">Remarks</span></span>

<span data-ttu-id="55434-115">El tipo de destinatario contenido en esta propiedad consta de un valor requerido y un indicador opcional.</span><span class="sxs-lookup"><span data-stu-id="55434-115">The recipient type contained in this property consists of one required value and one optional flag.</span></span>
  
<span data-ttu-id="55434-116">Esta propiedad debe contener exactamente uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="55434-116">This property must contain exactly one of the following values:</span></span>
  
<span data-ttu-id="55434-117">MAPI_TO</span><span class="sxs-lookup"><span data-stu-id="55434-117">MAPI_TO</span></span> 
  
> <span data-ttu-id="55434-118">El destinatario es un servidor principal (a) del destinatario.</span><span class="sxs-lookup"><span data-stu-id="55434-118">The recipient is a primary (To) recipient.</span></span> <span data-ttu-id="55434-119">Los clientes son necesarios para administrar a destinatarios principales.</span><span class="sxs-lookup"><span data-stu-id="55434-119">Clients are required to handle primary recipients.</span></span> <span data-ttu-id="55434-120">Todos los dem�s tipos son opcionales.</span><span class="sxs-lookup"><span data-stu-id="55434-120">All other types are optional.</span></span>
    
<span data-ttu-id="55434-121">MAPI_CC</span><span class="sxs-lookup"><span data-stu-id="55434-121">MAPI_CC</span></span> 
  
> <span data-ttu-id="55434-122">El destinatario es un destinatario de copia (CC), un destinatario que recibe un mensaje además de los destinatarios principales.</span><span class="sxs-lookup"><span data-stu-id="55434-122">The recipient is a carbon copy (CC) recipient, a recipient that receives a message in addition to the primary recipients.</span></span>
    
<span data-ttu-id="55434-123">MAPI_BCC</span><span class="sxs-lookup"><span data-stu-id="55434-123">MAPI_BCC</span></span> 
  
> <span data-ttu-id="55434-124">El destinatario es un destinatario de copia oculta (CCO).</span><span class="sxs-lookup"><span data-stu-id="55434-124">The recipient is a blind carbon copy (BCC) recipient.</span></span> <span data-ttu-id="55434-125">Destinatarios principales y de copia oculta son conscientes de la existencia de destinatarios CCO.</span><span class="sxs-lookup"><span data-stu-id="55434-125">Primary and carbon copy recipients are unaware of the existence of BCC recipients.</span></span> 
    
<span data-ttu-id="55434-126">MAPI_P1</span><span class="sxs-lookup"><span data-stu-id="55434-126">MAPI_P1</span></span> 
  
> <span data-ttu-id="55434-127">El destinatario no recibió correctamente el mensaje en el intento anterior.</span><span class="sxs-lookup"><span data-stu-id="55434-127">The recipient did not successfully receive the message on the previous attempt.</span></span> <span data-ttu-id="55434-128">Se trata de un nuevo envío de una transmisión anterior.</span><span class="sxs-lookup"><span data-stu-id="55434-128">This is a resend of an earlier transmission.</span></span>
    
<span data-ttu-id="55434-129">Además, se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="55434-129">In addition, the following flag can be set:</span></span>
  
<span data-ttu-id="55434-130">MAPI_SUBMITTED</span><span class="sxs-lookup"><span data-stu-id="55434-130">MAPI_SUBMITTED</span></span> 
  
> <span data-ttu-id="55434-131">El destinatario ya ha recibido el mensaje y no es necesario que volverá a aparecer.</span><span class="sxs-lookup"><span data-stu-id="55434-131">The recipient has already received the message and does not need to receive it again.</span></span> <span data-ttu-id="55434-132">Se trata de un nuevo envío de una transmisión anterior.</span><span class="sxs-lookup"><span data-stu-id="55434-132">This is a resend of an earlier transmission.</span></span> <span data-ttu-id="55434-133">Este indicador se establece en junto con los valores **MAPI_TO**, **MAPI_CC**y **MAPI_BCC** .</span><span class="sxs-lookup"><span data-stu-id="55434-133">This flag is set in conjunction with the **MAPI_TO**, **MAPI_CC**, and **MAPI_BCC** values.</span></span> 
    
<span data-ttu-id="55434-134">El valor de MAPI_P1 y el indicador **MAPI_SUBMITTED** se usa cuando un mensaje es que se retransmite debido a no entrega a uno o varios de los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="55434-134">The MAPI_P1 value and the **MAPI_SUBMITTED** flag are used when a message is being retransmitted due to nondelivery to one or more of the intended recipients.</span></span> <span data-ttu-id="55434-135">Para esta retransmisión, el cliente establece **MAPI_SUBMITTED** en todos los destinatarios que no es necesario volver al mensaje pero que deben mostrarse en la lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="55434-135">For this retransmission, the client sets **MAPI_SUBMITTED** on every recipient that does not need the message again but should be displayed in the recipient list.</span></span> <span data-ttu-id="55434-136">Para cada destinatario que no ha recibido el mensaje anteriormente, el cliente conserva el destinatario original con su valor **PR_RECIPIENT_TYPE** sin cambios, pero además envía una copia del destinatario con MAPI_P1 en lugar del valor original.</span><span class="sxs-lookup"><span data-stu-id="55434-136">For every recipient that did not receive the message previously, the client retains the original recipient with its **PR_RECIPIENT_TYPE** value unchanged, but additionally submits a copy of the recipient with MAPI_P1 in place of the original value.</span></span> <span data-ttu-id="55434-137">Esta copia, que se descarta antes de la entrega real, fuerza al destinatario en el sobre P1 y garantiza la retransmisión físico a ese destinatario.</span><span class="sxs-lookup"><span data-stu-id="55434-137">This copy, which is discarded before actual delivery, forces the recipient into the P1 envelope and guarantees physical retransmission to that recipient.</span></span> <span data-ttu-id="55434-138">La propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) se establece en FALSE para los destinatarios MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="55434-138">The **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property is set to FALSE for MAPI_P1 recipients.</span></span>
  
<span data-ttu-id="55434-139">Cuando un cliente, muestra un formulario de volver a enviar, sólo a los destinatarios MAPI_P1 están visibles.</span><span class="sxs-lookup"><span data-stu-id="55434-139">When a client displays a resend form, only the MAPI_P1 recipients are visible.</span></span> <span data-ttu-id="55434-140">A menos que el usuario escribe a los destinatarios adicionales, cuando el mensaje se entrega, la lista de destinatarios aparece exactamente igual que cuando se envió el mensaje por primera vez.</span><span class="sxs-lookup"><span data-stu-id="55434-140">Unless the user enters additional recipients, when the message is delivered, the recipient list appears exactly as it did when the message was sent for the first time.</span></span> 
  
<span data-ttu-id="55434-141">El **PR_DISPLAY_TO de MAPI** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) y las propiedades de **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) están relacionados con tipo de destinatario.</span><span class="sxs-lookup"><span data-stu-id="55434-141">The **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) and **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) properties are related to recipient type.</span></span> <span data-ttu-id="55434-142">Cuando un cliente llama a **IMAPIProp::SaveChanges un mensaje** y hay al menos un destinatario en la lista de destinatarios, el proveedor de almacén de mensajes establece estas propiedades como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="55434-142">When a client calls a message's **IMAPIProp::SaveChanges** and there is at least one recipient in the recipient list, the message store provider sets these properties as follows:</span></span> 
  
|<span data-ttu-id="55434-143">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="55434-143">**Property**</span></span>|<span data-ttu-id="55434-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="55434-144">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="55434-145">PR_DISPLAY_TO DE MAPI</span><span class="sxs-lookup"><span data-stu-id="55434-145">PR_DISPLAY_TO</span></span>  <br/> |<span data-ttu-id="55434-146">Se establece en TRUE si uno o varios de los destinatarios son **MAPI_TO** destinatarios.</span><span class="sxs-lookup"><span data-stu-id="55434-146">Set to TRUE if one or more of the recipients are **MAPI_TO** recipients.</span></span>  <br/> |
|<span data-ttu-id="55434-147">PR_DISPLAY_CC</span><span class="sxs-lookup"><span data-stu-id="55434-147">PR_DISPLAY_CC</span></span>  <br/> |<span data-ttu-id="55434-148">Se establece en TRUE si uno o varios de los destinatarios son **MAPI_CC** destinatarios.</span><span class="sxs-lookup"><span data-stu-id="55434-148">Set to TRUE if one or more of the recipients are **MAPI_CC** recipients.</span></span>  <br/> |
| <span data-ttu-id="55434-149">PR_DISPLAY_BCC</span><span class="sxs-lookup"><span data-stu-id="55434-149">PR_DISPLAY_BCC</span></span>  <br/> |<span data-ttu-id="55434-150">Se establece en TRUE si uno o varios de los destinatarios son destinatarios **MAPI_BCC** .</span><span class="sxs-lookup"><span data-stu-id="55434-150">Set to TRUE if one or more of the recipients are **MAPI_BCC** recipients.</span></span>  <br/> |
   
<span data-ttu-id="55434-151">En X.400, el contenedor de entrega o P1 es la información necesaria para enviar un mensaje, incluidas las propiedades de la dirección del destinatario y los indicadores de opciones de control de entrega y respuestas.</span><span class="sxs-lookup"><span data-stu-id="55434-151">In X.400, the P1 or delivery envelope is the information needed to deliver a message, including the recipient's address properties and any option flags controlling delivery and replies.</span></span> <span data-ttu-id="55434-152">El contenedor de P2 o para mostrar es la información suele mostrarse para cada destinatario que no sea el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="55434-152">The P2 or display envelope is the information usually displayed to each recipient other than the message text itself.</span></span> <span data-ttu-id="55434-153">Normalmente incluye el asunto, importancia, prioridad, confidencialidad y el tiempo de envío, así como los nombres de los destinatarios principales y copiados.</span><span class="sxs-lookup"><span data-stu-id="55434-153">It typically includes the subject, importance, priority, sensitivity, and submission time, as well as the primary and copied recipient names.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="55434-154">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="55434-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="55434-155">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="55434-155">Protocol specifications</span></span>

<span data-ttu-id="55434-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55434-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55434-157">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="55434-157">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="55434-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55434-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55434-159">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="55434-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="55434-160">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55434-160">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55434-161">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="55434-161">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="55434-162">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55434-162">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55434-163">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="55434-163">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="55434-164">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="55434-164">Header files</span></span>

<span data-ttu-id="55434-165">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55434-165">Mapidefs.h</span></span>
  
> <span data-ttu-id="55434-166">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="55434-166">Provides data type definitions.</span></span>
    
<span data-ttu-id="55434-167">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="55434-167">Mapitags.h</span></span>
  
> <span data-ttu-id="55434-168">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="55434-168">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55434-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="55434-169">See also</span></span>



[<span data-ttu-id="55434-170">Propiedad canónico PidTagRecipientStatus</span><span class="sxs-lookup"><span data-stu-id="55434-170">PidTagRecipientStatus Canonical Property</span></span>](pidtagrecipientstatus-canonical-property.md)
  
[<span data-ttu-id="55434-171">Propiedad canónico PidTagDisplayTo</span><span class="sxs-lookup"><span data-stu-id="55434-171">PidTagDisplayTo Canonical Property</span></span>](pidtagdisplayto-canonical-property.md)
  
[<span data-ttu-id="55434-172">Propiedad canónico PidTagDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="55434-172">PidTagDisplayBcc Canonical Property</span></span>](pidtagdisplaybcc-canonical-property.md)
  
[<span data-ttu-id="55434-173">Propiedad canónico PidTagDisplayCc</span><span class="sxs-lookup"><span data-stu-id="55434-173">PidTagDisplayCc Canonical Property</span></span>](pidtagdisplaycc-canonical-property.md)


[<span data-ttu-id="55434-174">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="55434-174">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="55434-175">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="55434-175">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="55434-176">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="55434-176">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="55434-177">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="55434-177">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

