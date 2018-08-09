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
ms.openlocfilehash: d3a3545c544c7b5cf5200468a94edf720dd326e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820283"
---
# <a name="pidtagsentrepresentingsmtpaddress-canonical-property"></a><span data-ttu-id="2c5ad-103">Propiedad canónica PidTagSentRepresentingSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="2c5ad-103">PidTagSentRepresentingSmtpAddress Canonical Property</span></span>

  
  
<span data-ttu-id="2c5ad-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2c5ad-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2c5ad-105">Contiene la dirección de correo electrónico de Protocolo Simple de transferencia de correo (SMTP) para el usuario de mensajería que está representada por el remitente.</span><span class="sxs-lookup"><span data-stu-id="2c5ad-105">Contains the Simple Mail Transport Protocol (SMTP) email address for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2c5ad-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2c5ad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c5ad-107">PR_SENT_REPRESENTING_SMTP_ADDRESS, PR_SENT_REPRESENTING_SMTP_ADDRESS_A, PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="2c5ad-107">PR_SENT_REPRESENTING_SMTP_ADDRESS, PR_SENT_REPRESENTING_SMTP_ADDRESS_A, PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="2c5ad-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2c5ad-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2c5ad-109">0x5D02</span><span class="sxs-lookup"><span data-stu-id="2c5ad-109">0x5D02</span></span>  <br/> |
|<span data-ttu-id="2c5ad-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2c5ad-110">Data type:</span></span>  <br/> |<span data-ttu-id="2c5ad-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="2c5ad-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="2c5ad-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2c5ad-112">Area:</span></span>  <br/> |<span data-ttu-id="2c5ad-113">Address</span><span class="sxs-lookup"><span data-stu-id="2c5ad-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c5ad-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2c5ad-114">Remarks</span></span>

<span data-ttu-id="2c5ad-115">Esta propiedad es un ejemplo de las propiedades de dirección para el usuario de mensajería que se está representado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="2c5ad-115">This property is an example of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="2c5ad-116">Cuando una aplicación cliente envía un mensaje en nombre de otro cliente, debe establecer todas las propiedades de remitente representado en los valores para que el cliente.</span><span class="sxs-lookup"><span data-stu-id="2c5ad-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="2c5ad-117">Un usuario de mensajería enviar en su propio nombre normalmente deja las propiedades de remitente representado no establecido.</span><span class="sxs-lookup"><span data-stu-id="2c5ad-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="2c5ad-118">El proveedor de transporte saliente siempre debe dejar esta propiedad no se modifica si se ha establecido por el cliente envío.</span><span class="sxs-lookup"><span data-stu-id="2c5ad-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="2c5ad-119">Si está establecido, el proveedor de transporte debe establecer para la propiedad **PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) en la copia del mensaje saliente y deje sin establecer en la copia local.</span><span class="sxs-lookup"><span data-stu-id="2c5ad-119">If it is unset, the transport provider should set it to the **PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2c5ad-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c5ad-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2c5ad-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="2c5ad-121">Protocol specifications</span></span>

<span data-ttu-id="2c5ad-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c5ad-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c5ad-123">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="2c5ad-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2c5ad-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c5ad-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c5ad-125">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="2c5ad-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="2c5ad-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c5ad-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c5ad-127">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="2c5ad-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="2c5ad-128">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c5ad-128">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c5ad-129">Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con objetos de mensaje y calendario cuando actúen en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="2c5ad-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="2c5ad-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c5ad-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c5ad-131">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="2c5ad-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="2c5ad-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c5ad-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c5ad-133">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="2c5ad-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="2c5ad-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c5ad-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c5ad-135">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="2c5ad-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="2c5ad-136">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c5ad-136">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c5ad-137">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="2c5ad-137">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2c5ad-138">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2c5ad-138">Header files</span></span>

<span data-ttu-id="2c5ad-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2c5ad-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c5ad-140">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2c5ad-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="2c5ad-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2c5ad-141">Mapitags.h</span></span>
  
> <span data-ttu-id="2c5ad-142">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="2c5ad-142">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c5ad-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c5ad-143">See also</span></span>



[<span data-ttu-id="2c5ad-144">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2c5ad-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2c5ad-145">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="2c5ad-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2c5ad-146">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2c5ad-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2c5ad-147">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="2c5ad-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

