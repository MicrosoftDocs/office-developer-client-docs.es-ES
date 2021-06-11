---
title: Propiedad canónica PidTagSentRepresentingName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: bfee6c5e-d4c6-442e-af71-23156569fed5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8e2df13f4e9c5d1d636c4f71ea6805ac031899e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314934"
---
# <a name="pidtagsentrepresentingname-canonical-property"></a><span data-ttu-id="92578-103">Propiedad canónica PidTagSentRepresentingName</span><span class="sxs-lookup"><span data-stu-id="92578-103">PidTagSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="92578-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92578-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92578-105">Contiene el nombre para mostrar del usuario de mensajería representado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="92578-105">Contains the display name for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="92578-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="92578-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="92578-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="92578-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="92578-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="92578-108">Identifier:</span></span>  <br/> |<span data-ttu-id="92578-109">0x0042</span><span class="sxs-lookup"><span data-stu-id="92578-109">0x0042</span></span>  <br/> |
|<span data-ttu-id="92578-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="92578-110">Data type:</span></span>  <br/> |<span data-ttu-id="92578-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="92578-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="92578-112">Área:</span><span class="sxs-lookup"><span data-stu-id="92578-112">Area:</span></span>  <br/> |<span data-ttu-id="92578-113">Dirección</span><span class="sxs-lookup"><span data-stu-id="92578-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92578-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="92578-114">Remarks</span></span>

<span data-ttu-id="92578-115">Estas propiedades son ejemplos de las propiedades de dirección del usuario de mensajería que representa el remitente.</span><span class="sxs-lookup"><span data-stu-id="92578-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="92578-116">Cuando una aplicación cliente envía un mensaje en nombre de otro cliente, debe establecer todas las propiedades de remitente representadas en los valores de ese cliente.</span><span class="sxs-lookup"><span data-stu-id="92578-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="92578-117">Por lo general, un usuario de mensajería que envía en su propio nombre deja sin conjunto las propiedades del remitente representado.</span><span class="sxs-lookup"><span data-stu-id="92578-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="92578-118">El proveedor de transporte saliente siempre debe dejar esta propiedad sin cambios si el cliente de envío la ha establecido.</span><span class="sxs-lookup"><span data-stu-id="92578-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="92578-119">Si no se establece, el proveedor de transporte debe establecerlo en **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) en la copia saliente del mensaje y dejarla sin establecer en la copia local.</span><span class="sxs-lookup"><span data-stu-id="92578-119">If it is unset, the transport provider should set it to **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="92578-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="92578-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="92578-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="92578-121">Protocol specifications</span></span>

<span data-ttu-id="92578-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92578-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92578-123">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="92578-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="92578-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/cc433482%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92578-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/cc433482%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="92578-125">Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="92578-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="92578-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/cc463884%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92578-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/cc463884%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="92578-127">Especifica las propiedades y las operaciones que representan elementos RSS.</span><span class="sxs-lookup"><span data-stu-id="92578-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="92578-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92578-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92578-129">Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="92578-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="92578-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92578-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92578-131">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="92578-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="92578-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92578-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92578-133">Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="92578-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="92578-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92578-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92578-135">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="92578-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="92578-136">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92578-136">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92578-137">Especifica la ubicación y las propiedades de los datos de configuración de cliente y servidor, como listas de categorías compartidas y horas laborables.</span><span class="sxs-lookup"><span data-stu-id="92578-137">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="92578-138">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92578-138">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92578-139">Especifica métodos para conectarse y configurar buzones como delegados e interacciones con objetos de mensaje y calendario cuando actúan en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="92578-139">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="92578-140">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92578-140">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92578-141">Especifica las propiedades y las operaciones que son permisibles para los objetos post.</span><span class="sxs-lookup"><span data-stu-id="92578-141">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="92578-142">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92578-142">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92578-143">Especifica las propiedades y las operaciones permitidas para los objetos de lista de distribución personal y de contacto.</span><span class="sxs-lookup"><span data-stu-id="92578-143">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="92578-144">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92578-144">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92578-145">Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficiente.</span><span class="sxs-lookup"><span data-stu-id="92578-145">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="92578-146">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="92578-146">Header files</span></span>

<span data-ttu-id="92578-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="92578-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="92578-148">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="92578-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="92578-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="92578-149">Mapitags.h</span></span>
  
> <span data-ttu-id="92578-150">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="92578-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="92578-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="92578-151">See also</span></span>



[<span data-ttu-id="92578-152">Propiedad canónica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="92578-152">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="92578-153">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="92578-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="92578-154">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="92578-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="92578-155">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="92578-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="92578-156">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="92578-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

