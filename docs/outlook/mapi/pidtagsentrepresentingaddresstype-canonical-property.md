---
title: Propiedad canónico PidTagSentRepresentingAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingAddressType
api_type:
- COM
ms.assetid: 6ecbf653-1faf-47bd-81a4-20157859fdfd
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: a58ae878ba13415823e61db3b1717e3cf07f29c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820272"
---
# <a name="pidtagsentrepresentingaddresstype-canonical-property"></a><span data-ttu-id="91629-103">Propiedad canónico PidTagSentRepresentingAddressType</span><span class="sxs-lookup"><span data-stu-id="91629-103">PidTagSentRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="91629-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="91629-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="91629-105">Contiene el tipo de dirección del usuario de mensajería que está representada por el remitente.</span><span class="sxs-lookup"><span data-stu-id="91629-105">Contains the address type for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="91629-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="91629-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91629-107">PR_SENT_REPRESENTING_ADDRTYPE, PR_SENT_REPRESENTING_ADDRTYPE_A, PR_SENT_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="91629-107">PR_SENT_REPRESENTING_ADDRTYPE, PR_SENT_REPRESENTING_ADDRTYPE_A, PR_SENT_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="91629-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="91629-108">Identifier:</span></span>  <br/> |<span data-ttu-id="91629-109">0x0064</span><span class="sxs-lookup"><span data-stu-id="91629-109">0x0064</span></span>  <br/> |
|<span data-ttu-id="91629-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="91629-110">Data type:</span></span>  <br/> |<span data-ttu-id="91629-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="91629-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="91629-112">Área:</span><span class="sxs-lookup"><span data-stu-id="91629-112">Area:</span></span>  <br/> |<span data-ttu-id="91629-113">Address</span><span class="sxs-lookup"><span data-stu-id="91629-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91629-114">Notas</span><span class="sxs-lookup"><span data-stu-id="91629-114">Remarks</span></span>

<span data-ttu-id="91629-115">Estas propiedades son ejemplos de las propiedades de dirección para el usuario de mensajería que se está representado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="91629-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="91629-116">Cuando una aplicación cliente envía un mensaje en nombre de otro cliente, debe establecer todas las propiedades de remitente representado en los valores para que el cliente.</span><span class="sxs-lookup"><span data-stu-id="91629-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="91629-117">Un usuario de mensajería enviar en su propio nombre normalmente deja las propiedades de remitente representado no establecido.</span><span class="sxs-lookup"><span data-stu-id="91629-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="91629-118">El proveedor de transporte saliente siempre debe dejar esta propiedad no se modifica si se ha establecido por el cliente envío.</span><span class="sxs-lookup"><span data-stu-id="91629-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="91629-119">Si está establecido, el proveedor de transporte debe establecer para la propiedad **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) en la copia del mensaje saliente y deje sin establecer en la copia local.</span><span class="sxs-lookup"><span data-stu-id="91629-119">If it is unset, the transport provider should set it to the **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="91629-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="91629-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="91629-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="91629-121">Protocol specifications</span></span>

<span data-ttu-id="91629-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91629-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91629-123">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="91629-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="91629-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91629-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91629-125">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="91629-125">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="91629-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91629-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91629-127">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="91629-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="91629-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91629-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91629-129">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="91629-129">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="91629-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91629-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91629-131">Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con objetos de mensaje y calendario cuando actúen en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="91629-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="91629-132">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91629-132">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91629-133">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="91629-133">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="91629-134">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91629-134">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91629-135">Especifica las propiedades y operaciones que se permiten para registrar objetos.</span><span class="sxs-lookup"><span data-stu-id="91629-135">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="91629-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91629-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91629-137">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="91629-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="91629-138">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91629-138">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91629-139">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="91629-139">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="91629-140">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="91629-140">Header files</span></span>

<span data-ttu-id="91629-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91629-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="91629-142">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="91629-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="91629-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="91629-143">Mapitags.h</span></span>
  
> <span data-ttu-id="91629-144">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="91629-144">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91629-145">Ver también</span><span class="sxs-lookup"><span data-stu-id="91629-145">See also</span></span>



[<span data-ttu-id="91629-146">Propiedad canónico PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="91629-146">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)


[<span data-ttu-id="91629-147">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="91629-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91629-148">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="91629-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91629-149">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="91629-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91629-150">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="91629-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

