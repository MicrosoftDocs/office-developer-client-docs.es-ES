---
title: Propiedad canónica PidTagSentRepresentingSmtpAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ed122a2-0967-4de3-a2ee-69f81ae77b16
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a9114b1c9c3f5b09c5636f7d55d7111dd86afc06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341940"
---
# <a name="pidtagsentrepresentingsmtpaddress-canonical-property"></a><span data-ttu-id="36889-103">Propiedad canónica PidTagSentRepresentingSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="36889-103">PidTagSentRepresentingSmtpAddress Canonical Property</span></span>

  
  
<span data-ttu-id="36889-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36889-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36889-105">Contiene la dirección de correo electrónico del Protocolo simple de transporte de correo (SMTP) para el usuario de mensajería representado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="36889-105">Contains the Simple Mail Transport Protocol (SMTP) email address for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="36889-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="36889-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="36889-107">PR_SENT_REPRESENTING_SMTP_ADDRESS, PR_SENT_REPRESENTING_SMTP_ADDRESS_A, PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="36889-107">PR_SENT_REPRESENTING_SMTP_ADDRESS, PR_SENT_REPRESENTING_SMTP_ADDRESS_A, PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="36889-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="36889-108">Identifier:</span></span>  <br/> |<span data-ttu-id="36889-109">0x5D02</span><span class="sxs-lookup"><span data-stu-id="36889-109">0x5D02</span></span>  <br/> |
|<span data-ttu-id="36889-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="36889-110">Data type:</span></span>  <br/> |<span data-ttu-id="36889-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="36889-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="36889-112">Área:</span><span class="sxs-lookup"><span data-stu-id="36889-112">Area:</span></span>  <br/> |<span data-ttu-id="36889-113">Dirección</span><span class="sxs-lookup"><span data-stu-id="36889-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36889-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="36889-114">Remarks</span></span>

<span data-ttu-id="36889-115">Esta propiedad es un ejemplo de las propiedades de dirección para el usuario de mensajería que representa el remitente.</span><span class="sxs-lookup"><span data-stu-id="36889-115">This property is an example of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="36889-116">Cuando una aplicación cliente envía un mensaje en nombre de otro cliente, debe establecer todas las propiedades de remitente representadas en los valores de ese cliente.</span><span class="sxs-lookup"><span data-stu-id="36889-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="36889-117">Por lo general, un usuario de mensajería que envía en su propio nombre deja sin conjunto las propiedades del remitente representado.</span><span class="sxs-lookup"><span data-stu-id="36889-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="36889-118">El proveedor de transporte saliente siempre debe dejar esta propiedad sin cambios si el cliente de envío la ha establecido.</span><span class="sxs-lookup"><span data-stu-id="36889-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="36889-119">Si no se establece, el proveedor de transporte debe establecerlo en la propiedad **PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) en la copia saliente del mensaje y dejarla sin establecer en la copia local.</span><span class="sxs-lookup"><span data-stu-id="36889-119">If it is unset, the transport provider should set it to the **PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="36889-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="36889-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="36889-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="36889-121">Protocol specifications</span></span>

<span data-ttu-id="36889-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36889-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36889-123">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="36889-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="36889-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36889-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36889-125">Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="36889-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="36889-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36889-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36889-127">Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="36889-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="36889-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36889-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36889-129">Especifica métodos para conectarse y configurar buzones como delegados e interacciones con objetos de mensaje y calendario cuando actúan en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="36889-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="36889-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36889-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36889-131">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="36889-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="36889-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36889-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36889-133">Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="36889-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="36889-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36889-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36889-135">Especifica las propiedades y las operaciones permitidas para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="36889-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="36889-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36889-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36889-137">Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficiente.</span><span class="sxs-lookup"><span data-stu-id="36889-137">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="36889-138">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="36889-138">Header files</span></span>

<span data-ttu-id="36889-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="36889-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="36889-140">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="36889-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="36889-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="36889-141">Mapitags.h</span></span>
  
> <span data-ttu-id="36889-142">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="36889-142">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="36889-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="36889-143">See also</span></span>



[<span data-ttu-id="36889-144">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="36889-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="36889-145">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="36889-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="36889-146">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="36889-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="36889-147">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="36889-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

