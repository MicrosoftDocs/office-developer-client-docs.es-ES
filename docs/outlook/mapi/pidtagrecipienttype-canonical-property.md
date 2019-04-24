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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355261"
---
# <a name="pidtagrecipienttype-canonical-property"></a><span data-ttu-id="23170-103">Propiedad canónica PidTagRecipientType</span><span class="sxs-lookup"><span data-stu-id="23170-103">PidTagRecipientType Canonical Property</span></span>

  
  
<span data-ttu-id="23170-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23170-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23170-105">Contiene el tipo de destinatario de un destinatario del mensaje.</span><span class="sxs-lookup"><span data-stu-id="23170-105">Contains the recipient type for a message recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="23170-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="23170-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="23170-107">PR_RECIPIENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="23170-107">PR_RECIPIENT_TYPE</span></span>  <br/> |
|<span data-ttu-id="23170-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="23170-108">Identifier:</span></span>  <br/> |<span data-ttu-id="23170-109">0x0C15</span><span class="sxs-lookup"><span data-stu-id="23170-109">0x0C15</span></span>  <br/> |
|<span data-ttu-id="23170-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="23170-110">Data type:</span></span>  <br/> |<span data-ttu-id="23170-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="23170-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="23170-112">Área:</span><span class="sxs-lookup"><span data-stu-id="23170-112">Area:</span></span>  <br/> |<span data-ttu-id="23170-113">Destinatario MAPI</span><span class="sxs-lookup"><span data-stu-id="23170-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23170-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="23170-114">Remarks</span></span>

<span data-ttu-id="23170-115">El tipo de destinatario contenido en esta propiedad consta de un valor obligatorio y de una marca opcional.</span><span class="sxs-lookup"><span data-stu-id="23170-115">The recipient type contained in this property consists of one required value and one optional flag.</span></span>
  
<span data-ttu-id="23170-116">Esta propiedad debe contener exactamente uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="23170-116">This property must contain exactly one of the following values:</span></span>
  
<span data-ttu-id="23170-117">MAPI_TO</span><span class="sxs-lookup"><span data-stu-id="23170-117">MAPI_TO</span></span> 
  
> <span data-ttu-id="23170-118">El destinatario es un destinatario principal (para).</span><span class="sxs-lookup"><span data-stu-id="23170-118">The recipient is a primary (To) recipient.</span></span> <span data-ttu-id="23170-119">Los clientes deben administrar los destinatarios principales.</span><span class="sxs-lookup"><span data-stu-id="23170-119">Clients are required to handle primary recipients.</span></span> <span data-ttu-id="23170-120">Todos los dem�s tipos son opcionales.</span><span class="sxs-lookup"><span data-stu-id="23170-120">All other types are optional.</span></span>
    
<span data-ttu-id="23170-121">MAPI_CC</span><span class="sxs-lookup"><span data-stu-id="23170-121">MAPI_CC</span></span> 
  
> <span data-ttu-id="23170-122">El destinatario es un destinatario con copia (CC), un destinatario que recibe un mensaje además de los destinatarios principales.</span><span class="sxs-lookup"><span data-stu-id="23170-122">The recipient is a carbon copy (CC) recipient, a recipient that receives a message in addition to the primary recipients.</span></span>
    
<span data-ttu-id="23170-123">MAPI_BCC</span><span class="sxs-lookup"><span data-stu-id="23170-123">MAPI_BCC</span></span> 
  
> <span data-ttu-id="23170-124">El destinatario es un destinatario con copia oculta (CCO).</span><span class="sxs-lookup"><span data-stu-id="23170-124">The recipient is a blind carbon copy (BCC) recipient.</span></span> <span data-ttu-id="23170-125">Los destinatarios principales y de copia carbón no son conscientes de la existencia de destinatarios de CCO.</span><span class="sxs-lookup"><span data-stu-id="23170-125">Primary and carbon copy recipients are unaware of the existence of BCC recipients.</span></span> 
    
<span data-ttu-id="23170-126">MAPI_P1</span><span class="sxs-lookup"><span data-stu-id="23170-126">MAPI_P1</span></span> 
  
> <span data-ttu-id="23170-127">El destinatario no recibió correctamente el mensaje en el intento anterior.</span><span class="sxs-lookup"><span data-stu-id="23170-127">The recipient did not successfully receive the message on the previous attempt.</span></span> <span data-ttu-id="23170-128">Se trata de un reenvío de una transmisión anterior.</span><span class="sxs-lookup"><span data-stu-id="23170-128">This is a resend of an earlier transmission.</span></span>
    
<span data-ttu-id="23170-129">Además, se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="23170-129">In addition, the following flag can be set:</span></span>
  
<span data-ttu-id="23170-130">MAPI_SUBMITTED</span><span class="sxs-lookup"><span data-stu-id="23170-130">MAPI_SUBMITTED</span></span> 
  
> <span data-ttu-id="23170-131">El destinatario ya ha recibido el mensaje y no necesita recibirlo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="23170-131">The recipient has already received the message and does not need to receive it again.</span></span> <span data-ttu-id="23170-132">Se trata de un reenvío de una transmisión anterior.</span><span class="sxs-lookup"><span data-stu-id="23170-132">This is a resend of an earlier transmission.</span></span> <span data-ttu-id="23170-133">Esta marca se establece junto con los valores de **MAPI_TO**, **MAPI_CC**y **MAPI_BCC** .</span><span class="sxs-lookup"><span data-stu-id="23170-133">This flag is set in conjunction with the **MAPI_TO**, **MAPI_CC**, and **MAPI_BCC** values.</span></span> 
    
<span data-ttu-id="23170-134">El valor MAPI_P1 y la marca **MAPI_SUBMITTED** se usan cuando se retransmite un mensaje debido a la no entrega a uno o más de los destinatarios previstos.</span><span class="sxs-lookup"><span data-stu-id="23170-134">The MAPI_P1 value and the **MAPI_SUBMITTED** flag are used when a message is being retransmitted due to nondelivery to one or more of the intended recipients.</span></span> <span data-ttu-id="23170-135">Para esta retransmisión, el cliente establece **MAPI_SUBMITTED** en todos los destinatarios que no necesitan el mensaje de nuevo, sino que deben mostrarse en la lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="23170-135">For this retransmission, the client sets **MAPI_SUBMITTED** on every recipient that does not need the message again but should be displayed in the recipient list.</span></span> <span data-ttu-id="23170-136">Por cada destinatario que no recibió el mensaje anteriormente, el cliente conserva el destinatario original con su valor **PR_RECIPIENT_TYPE** sin modificar, pero además envía una copia del destinatario con MAPI_P1 en lugar del valor original.</span><span class="sxs-lookup"><span data-stu-id="23170-136">For every recipient that did not receive the message previously, the client retains the original recipient with its **PR_RECIPIENT_TYPE** value unchanged, but additionally submits a copy of the recipient with MAPI_P1 in place of the original value.</span></span> <span data-ttu-id="23170-137">Esta copia, que se descarta antes de la entrega real, fuerza al destinatario en el sobre P1 y garantiza una retransmisión física a ese destinatario.</span><span class="sxs-lookup"><span data-stu-id="23170-137">This copy, which is discarded before actual delivery, forces the recipient into the P1 envelope and guarantees physical retransmission to that recipient.</span></span> <span data-ttu-id="23170-138">La propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) se establece en false para los destinatarios de MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="23170-138">The **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property is set to FALSE for MAPI_P1 recipients.</span></span>
  
<span data-ttu-id="23170-139">Cuando un cliente muestra un formulario de reenvío, solo están visibles los destinatarios de MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="23170-139">When a client displays a resend form, only the MAPI_P1 recipients are visible.</span></span> <span data-ttu-id="23170-140">A menos que el usuario escriba destinatarios adicionales, cuando se entregue el mensaje, la lista de destinatarios aparecerá exactamente como lo hacía cuando se envió el mensaje por primera vez.</span><span class="sxs-lookup"><span data-stu-id="23170-140">Unless the user enters additional recipients, when the message is delivered, the recipient list appears exactly as it did when the message was sent for the first time.</span></span> 
  
<span data-ttu-id="23170-141">Las propiedades **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) **, PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) y **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) están relacionadas con el tipo de destinatario.</span><span class="sxs-lookup"><span data-stu-id="23170-141">The **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) and **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) properties are related to recipient type.</span></span> <span data-ttu-id="23170-142">Cuando un cliente llama a **IMAPIProp:: SaveChanges** y existe al menos un destinatario en la lista de destinatarios, el proveedor de almacenamiento de mensajes establece estas propiedades de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="23170-142">When a client calls a message's **IMAPIProp::SaveChanges** and there is at least one recipient in the recipient list, the message store provider sets these properties as follows:</span></span> 
  
|<span data-ttu-id="23170-143">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="23170-143">**Property**</span></span>|<span data-ttu-id="23170-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="23170-144">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="23170-145">PR_DISPLAY_TO</span><span class="sxs-lookup"><span data-stu-id="23170-145">PR_DISPLAY_TO</span></span>  <br/> |<span data-ttu-id="23170-146">Se establece en TRUE si uno o varios de los destinatarios son destinatarios **MAPI_TO** .</span><span class="sxs-lookup"><span data-stu-id="23170-146">Set to TRUE if one or more of the recipients are **MAPI_TO** recipients.</span></span>  <br/> |
|<span data-ttu-id="23170-147">PR_DISPLAY_CC</span><span class="sxs-lookup"><span data-stu-id="23170-147">PR_DISPLAY_CC</span></span>  <br/> |<span data-ttu-id="23170-148">Se establece en TRUE si uno o varios de los destinatarios son destinatarios **MAPI_CC** .</span><span class="sxs-lookup"><span data-stu-id="23170-148">Set to TRUE if one or more of the recipients are **MAPI_CC** recipients.</span></span>  <br/> |
| <span data-ttu-id="23170-149">PR_DISPLAY_BCC</span><span class="sxs-lookup"><span data-stu-id="23170-149">PR_DISPLAY_BCC</span></span>  <br/> |<span data-ttu-id="23170-150">Se establece en TRUE si uno o varios de los destinatarios son destinatarios **MAPI_BCC** .</span><span class="sxs-lookup"><span data-stu-id="23170-150">Set to TRUE if one or more of the recipients are **MAPI_BCC** recipients.</span></span>  <br/> |
   
<span data-ttu-id="23170-151">En X. 400, el sobre P1 o de entrega es la información necesaria para entregar un mensaje, incluidas las propiedades de la dirección del destinatario y los indicadores de opciones que controlan la entrega y las respuestas.</span><span class="sxs-lookup"><span data-stu-id="23170-151">In X.400, the P1 or delivery envelope is the information needed to deliver a message, including the recipient's address properties and any option flags controlling delivery and replies.</span></span> <span data-ttu-id="23170-152">La P2 o el sobre de visualización es la información que se muestra normalmente a todos los destinatarios que no sean el propio texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="23170-152">The P2 or display envelope is the information usually displayed to each recipient other than the message text itself.</span></span> <span data-ttu-id="23170-153">Normalmente, incluye el asunto, la importancia, la prioridad, la confidencialidad y el tiempo de envío, así como los nombres de los destinatarios principales y copiados.</span><span class="sxs-lookup"><span data-stu-id="23170-153">It typically includes the subject, importance, priority, sensitivity, and submission time, as well as the primary and copied recipient names.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="23170-154">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="23170-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="23170-155">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="23170-155">Protocol specifications</span></span>

<span data-ttu-id="23170-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23170-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23170-157">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="23170-157">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="23170-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23170-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23170-159">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="23170-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="23170-160">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23170-160">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23170-161">Especifica las propiedades y operaciones que se admiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="23170-161">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="23170-162">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23170-162">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23170-163">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="23170-163">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="23170-164">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="23170-164">Header files</span></span>

<span data-ttu-id="23170-165">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="23170-165">Mapidefs.h</span></span>
  
> <span data-ttu-id="23170-166">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="23170-166">Provides data type definitions.</span></span>
    
<span data-ttu-id="23170-167">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="23170-167">Mapitags.h</span></span>
  
> <span data-ttu-id="23170-168">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="23170-168">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23170-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="23170-169">See also</span></span>



[<span data-ttu-id="23170-170">Propiedad canónica PidTagRecipientStatus</span><span class="sxs-lookup"><span data-stu-id="23170-170">PidTagRecipientStatus Canonical Property</span></span>](pidtagrecipientstatus-canonical-property.md)
  
[<span data-ttu-id="23170-171">Propiedad canónica PidTagDisplayTo</span><span class="sxs-lookup"><span data-stu-id="23170-171">PidTagDisplayTo Canonical Property</span></span>](pidtagdisplayto-canonical-property.md)
  
[<span data-ttu-id="23170-172">Propiedad canónica PidTagDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="23170-172">PidTagDisplayBcc Canonical Property</span></span>](pidtagdisplaybcc-canonical-property.md)
  
[<span data-ttu-id="23170-173">Propiedad canónica PidTagDisplayCc</span><span class="sxs-lookup"><span data-stu-id="23170-173">PidTagDisplayCc Canonical Property</span></span>](pidtagdisplaycc-canonical-property.md)


[<span data-ttu-id="23170-174">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="23170-174">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="23170-175">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="23170-175">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="23170-176">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="23170-176">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="23170-177">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="23170-177">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

