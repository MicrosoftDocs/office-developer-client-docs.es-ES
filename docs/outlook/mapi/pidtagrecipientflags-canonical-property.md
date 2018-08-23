---
title: Propiedad canónica PidTagRecipientFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientFlags
api_type:
- COM
ms.assetid: 9fbe537f-b5fe-48a2-803c-653c50c82efd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0e84f1361e9ca3d95b4297c01801e649a9f86ced
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569235"
---
# <a name="pidtagrecipientflags-canonical-property"></a><span data-ttu-id="8291e-103">Propiedad canónica PidTagRecipientFlags</span><span class="sxs-lookup"><span data-stu-id="8291e-103">PidTagRecipientFlags Canonical Property</span></span>

  
  
<span data-ttu-id="8291e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8291e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8291e-105">Especifica un campo de bits que describe el estado del destinatario.</span><span class="sxs-lookup"><span data-stu-id="8291e-105">Specifies a bit field that describes the recipient status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8291e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8291e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8291e-107">PR_RECIPIENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="8291e-107">PR_RECIPIENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="8291e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8291e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8291e-109">0x5FFD</span><span class="sxs-lookup"><span data-stu-id="8291e-109">0x5FFD</span></span>  <br/> |
|<span data-ttu-id="8291e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8291e-110">Data type:</span></span>  <br/> |<span data-ttu-id="8291e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8291e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8291e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8291e-112">Area:</span></span>  <br/> |<span data-ttu-id="8291e-113">Destinatario del transporte</span><span class="sxs-lookup"><span data-stu-id="8291e-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8291e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8291e-114">Remarks</span></span>

<span data-ttu-id="8291e-115">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="8291e-115">This property is not required.</span></span> <span data-ttu-id="8291e-116">Los siguientes son los indicadores individuales que se pueden establecer.</span><span class="sxs-lookup"><span data-stu-id="8291e-116">The following are the individual flags that can be set.</span></span>
  
|<span data-ttu-id="8291e-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8291e-117">**Value**</span></span>|<span data-ttu-id="8291e-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8291e-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8291e-119">S (recipSendable, 0 x 00000001)</span><span class="sxs-lookup"><span data-stu-id="8291e-119">S (recipSendable, 0x00000001)</span></span>  <br/> |<span data-ttu-id="8291e-120">El destinatario es un asistente de **Sendable** .</span><span class="sxs-lookup"><span data-stu-id="8291e-120">The recipient is a **Sendable** Attendee.</span></span> <span data-ttu-id="8291e-121">Esta marca sólo se utiliza en la propiedad **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8291e-121">This flag is only used in the **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) property.</span></span>  <br/> |
|<span data-ttu-id="8291e-122">O (recipOrganizer, 0x0000002)</span><span class="sxs-lookup"><span data-stu-id="8291e-122">O (recipOrganizer, 0x0000002)</span></span>  <br/> |<span data-ttu-id="8291e-123">El **RecipientRow** en el que se ha configurado esta marca representa el organizador de la reunión.</span><span class="sxs-lookup"><span data-stu-id="8291e-123">The **RecipientRow** on which this flag is set represents the meeting Organizer.</span></span>  <br/> |
|<span data-ttu-id="8291e-124">Recuperación de emergencia (recipExceptionalResponse, 0 x 00000010)</span><span class="sxs-lookup"><span data-stu-id="8291e-124">ER (recipExceptionalResponse, 0x00000010)</span></span>  <br/> |<span data-ttu-id="8291e-125">Indica que el asistente le dio una respuesta para la excepción en el que reside este **RecipientRow** .</span><span class="sxs-lookup"><span data-stu-id="8291e-125">Indicates that the attendee gave a response for the exception on which this **RecipientRow** resides.</span></span> <span data-ttu-id="8291e-126">Esta marca sólo se utiliza en un **RecipientRow** de un objeto de incrustación de mensajes de excepción del objeto del organizador de la reunión.</span><span class="sxs-lookup"><span data-stu-id="8291e-126">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="8291e-127">ED (recipExceptionalDeleted, 0 x 00000020)</span><span class="sxs-lookup"><span data-stu-id="8291e-127">ED (recipExceptionalDeleted, 0x00000020)</span></span>  <br/> |<span data-ttu-id="8291e-128">Indica que aunque la **RecipientRow** existe, debe tratarse como si no lo hace el destinatario correspondiente.</span><span class="sxs-lookup"><span data-stu-id="8291e-128">Indicates that although the **RecipientRow** exists, it should be treated as if the corresponding recipient does not.</span></span> <span data-ttu-id="8291e-129">Esta marca sólo se utiliza en un **RecipientRow** de un objeto de incrustación de mensajes de excepción del objeto del organizador de la reunión.</span><span class="sxs-lookup"><span data-stu-id="8291e-129">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="8291e-130">X (reservada, 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="8291e-130">X (reserved, 0x00000040)</span></span>  <br/> |<span data-ttu-id="8291e-131">No se debe establecer.</span><span class="sxs-lookup"><span data-stu-id="8291e-131">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="8291e-132">X (reservada, 0x00000080)</span><span class="sxs-lookup"><span data-stu-id="8291e-132">X (reserved, 0x00000080)</span></span>  <br/> |<span data-ttu-id="8291e-133">No se debe establecer.</span><span class="sxs-lookup"><span data-stu-id="8291e-133">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="8291e-134">G (recipOriginal, 0 x 00000100)</span><span class="sxs-lookup"><span data-stu-id="8291e-134">G (recipOriginal, 0x00000100)</span></span>  <br/> |<span data-ttu-id="8291e-135">Indica que el destinatario es un asistente original.</span><span class="sxs-lookup"><span data-stu-id="8291e-135">Indicates the recipient is an original attendee.</span></span> <span data-ttu-id="8291e-136">Esta marca sólo se utiliza en la propiedad **dispidApptUnsendableRecips** .</span><span class="sxs-lookup"><span data-stu-id="8291e-136">This flag is only used in the **dispidApptUnsendableRecips** property.</span></span>  <br/> |
|<span data-ttu-id="8291e-137">X (reservada, 0 x 00000200)</span><span class="sxs-lookup"><span data-stu-id="8291e-137">X (reserved, 0x00000200)</span></span>  <br/> |<span data-ttu-id="8291e-138">Reservado.</span><span class="sxs-lookup"><span data-stu-id="8291e-138">Reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="8291e-139">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8291e-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8291e-140">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="8291e-140">Protocol specifications</span></span>

<span data-ttu-id="8291e-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8291e-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8291e-142">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8291e-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8291e-143">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8291e-143">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8291e-144">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8291e-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8291e-145">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8291e-145">Header files</span></span>

<span data-ttu-id="8291e-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8291e-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="8291e-147">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8291e-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="8291e-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8291e-148">Mapitags.h</span></span>
  
> <span data-ttu-id="8291e-149">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="8291e-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8291e-150">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="8291e-150">See also</span></span>



[<span data-ttu-id="8291e-151">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8291e-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8291e-152">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="8291e-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8291e-153">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8291e-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8291e-154">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="8291e-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

