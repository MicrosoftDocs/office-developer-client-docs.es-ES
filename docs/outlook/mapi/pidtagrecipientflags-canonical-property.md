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
ms.openlocfilehash: 7b791d75c2a76ea1a504c0d8862dd20f5365b475
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356703"
---
# <a name="pidtagrecipientflags-canonical-property"></a><span data-ttu-id="f07c1-103">Propiedad canónica PidTagRecipientFlags</span><span class="sxs-lookup"><span data-stu-id="f07c1-103">PidTagRecipientFlags Canonical Property</span></span>

  
  
<span data-ttu-id="f07c1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f07c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f07c1-105">Especifica un campo de bits que describe el estado del destinatario.</span><span class="sxs-lookup"><span data-stu-id="f07c1-105">Specifies a bit field that describes the recipient status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f07c1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f07c1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f07c1-107">PR_RECIPIENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="f07c1-107">PR_RECIPIENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="f07c1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f07c1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f07c1-109">0x5FFD</span><span class="sxs-lookup"><span data-stu-id="f07c1-109">0x5FFD</span></span>  <br/> |
|<span data-ttu-id="f07c1-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f07c1-110">Data type:</span></span>  <br/> |<span data-ttu-id="f07c1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f07c1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f07c1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f07c1-112">Area:</span></span>  <br/> |<span data-ttu-id="f07c1-113">Destinatario de transporte</span><span class="sxs-lookup"><span data-stu-id="f07c1-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f07c1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f07c1-114">Remarks</span></span>

<span data-ttu-id="f07c1-115">Esta propiedad no es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="f07c1-115">This property is not required.</span></span> <span data-ttu-id="f07c1-116">A continuación se enumeran las marcas individuales que se pueden establecer.</span><span class="sxs-lookup"><span data-stu-id="f07c1-116">The following are the individual flags that can be set.</span></span>
  
|<span data-ttu-id="f07c1-117">**Value**</span><span class="sxs-lookup"><span data-stu-id="f07c1-117">**Value**</span></span>|<span data-ttu-id="f07c1-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f07c1-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f07c1-119">S (recipSendable, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="f07c1-119">S (recipSendable, 0x00000001)</span></span>  <br/> |<span data-ttu-id="f07c1-120">El destinatario es un asistente que se **envía** .</span><span class="sxs-lookup"><span data-stu-id="f07c1-120">The recipient is a **Sendable** Attendee.</span></span> <span data-ttu-id="f07c1-121">Esta marca solo se usa en la propiedad **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f07c1-121">This flag is only used in the **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) property.</span></span>  <br/> |
|<span data-ttu-id="f07c1-122">O (recipOrganizer, 0x0000002)</span><span class="sxs-lookup"><span data-stu-id="f07c1-122">O (recipOrganizer, 0x0000002)</span></span>  <br/> |<span data-ttu-id="f07c1-123">El **RecipientRow** en el que se establece esta marca representa el organizador de la reunión.</span><span class="sxs-lookup"><span data-stu-id="f07c1-123">The **RecipientRow** on which this flag is set represents the meeting Organizer.</span></span>  <br/> |
|<span data-ttu-id="f07c1-124">ER (recipExceptionalResponse, 0x00000010)</span><span class="sxs-lookup"><span data-stu-id="f07c1-124">ER (recipExceptionalResponse, 0x00000010)</span></span>  <br/> |<span data-ttu-id="f07c1-125">Indica que el asistente dio una respuesta para la excepción en la que reside esta **RecipientRow** .</span><span class="sxs-lookup"><span data-stu-id="f07c1-125">Indicates that the attendee gave a response for the exception on which this **RecipientRow** resides.</span></span> <span data-ttu-id="f07c1-126">Esta marca solo se usa en un **RecipientRow** de un objeto de mensaje incrustado de excepción del objeto de reunión del organizador.</span><span class="sxs-lookup"><span data-stu-id="f07c1-126">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="f07c1-127">ED (recipExceptionalDeleted, 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="f07c1-127">ED (recipExceptionalDeleted, 0x00000020)</span></span>  <br/> |<span data-ttu-id="f07c1-128">Indica que, aunque exista la **RecipientRow** , debe tratarse como si el destinatario correspondiente no lo hubiera.</span><span class="sxs-lookup"><span data-stu-id="f07c1-128">Indicates that although the **RecipientRow** exists, it should be treated as if the corresponding recipient does not.</span></span> <span data-ttu-id="f07c1-129">Esta marca solo se usa en un **RecipientRow** de un objeto de mensaje incrustado de excepción del objeto de reunión del organizador.</span><span class="sxs-lookup"><span data-stu-id="f07c1-129">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="f07c1-130">X (reservado, 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="f07c1-130">X (reserved, 0x00000040)</span></span>  <br/> |<span data-ttu-id="f07c1-131">No se debe establecer.</span><span class="sxs-lookup"><span data-stu-id="f07c1-131">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="f07c1-132">X (reservado, 0x00000080)</span><span class="sxs-lookup"><span data-stu-id="f07c1-132">X (reserved, 0x00000080)</span></span>  <br/> |<span data-ttu-id="f07c1-133">No se debe establecer.</span><span class="sxs-lookup"><span data-stu-id="f07c1-133">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="f07c1-134">G (recipOriginal, 0x00000100)</span><span class="sxs-lookup"><span data-stu-id="f07c1-134">G (recipOriginal, 0x00000100)</span></span>  <br/> |<span data-ttu-id="f07c1-135">Indica que el destinatario es un asistente original.</span><span class="sxs-lookup"><span data-stu-id="f07c1-135">Indicates the recipient is an original attendee.</span></span> <span data-ttu-id="f07c1-136">Esta marca solo se usa en la propiedad **dispidApptUnsendableRecips** .</span><span class="sxs-lookup"><span data-stu-id="f07c1-136">This flag is only used in the **dispidApptUnsendableRecips** property.</span></span>  <br/> |
|<span data-ttu-id="f07c1-137">X (reservado, 0x00000200)</span><span class="sxs-lookup"><span data-stu-id="f07c1-137">X (reserved, 0x00000200)</span></span>  <br/> |<span data-ttu-id="f07c1-138">Reservado.</span><span class="sxs-lookup"><span data-stu-id="f07c1-138">Reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f07c1-139">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f07c1-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f07c1-140">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f07c1-140">Protocol specifications</span></span>

<span data-ttu-id="f07c1-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f07c1-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f07c1-142">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f07c1-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f07c1-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f07c1-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f07c1-144">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="f07c1-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f07c1-145">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f07c1-145">Header files</span></span>

<span data-ttu-id="f07c1-146">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f07c1-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="f07c1-147">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f07c1-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="f07c1-148">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f07c1-148">Mapitags.h</span></span>
  
> <span data-ttu-id="f07c1-149">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f07c1-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f07c1-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="f07c1-150">See also</span></span>



[<span data-ttu-id="f07c1-151">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f07c1-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f07c1-152">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="f07c1-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f07c1-153">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f07c1-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f07c1-154">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="f07c1-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

