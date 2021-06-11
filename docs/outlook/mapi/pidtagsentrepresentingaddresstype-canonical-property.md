---
title: Propiedad canónica PidTagSentRepresentingAddressType
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bbf1ae0d7b38886fe08af2ad13f1a2be6b6e01cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342577"
---
# <a name="pidtagsentrepresentingaddresstype-canonical-property"></a><span data-ttu-id="cd237-103">Propiedad canónica PidTagSentRepresentingAddressType</span><span class="sxs-lookup"><span data-stu-id="cd237-103">PidTagSentRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="cd237-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd237-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd237-105">Contiene el tipo de dirección del usuario de mensajería representado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="cd237-105">Contains the address type for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cd237-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cd237-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cd237-107">PR_SENT_REPRESENTING_ADDRTYPE, PR_SENT_REPRESENTING_ADDRTYPE_A, PR_SENT_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="cd237-107">PR_SENT_REPRESENTING_ADDRTYPE, PR_SENT_REPRESENTING_ADDRTYPE_A, PR_SENT_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="cd237-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cd237-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cd237-109">0x0064</span><span class="sxs-lookup"><span data-stu-id="cd237-109">0x0064</span></span>  <br/> |
|<span data-ttu-id="cd237-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="cd237-110">Data type:</span></span>  <br/> |<span data-ttu-id="cd237-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="cd237-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="cd237-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cd237-112">Area:</span></span>  <br/> |<span data-ttu-id="cd237-113">Dirección</span><span class="sxs-lookup"><span data-stu-id="cd237-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd237-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cd237-114">Remarks</span></span>

<span data-ttu-id="cd237-115">Estas propiedades son ejemplos de las propiedades de dirección del usuario de mensajería que representa el remitente.</span><span class="sxs-lookup"><span data-stu-id="cd237-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="cd237-116">Cuando una aplicación cliente envía un mensaje en nombre de otro cliente, debe establecer todas las propiedades de remitente representadas en los valores de ese cliente.</span><span class="sxs-lookup"><span data-stu-id="cd237-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="cd237-117">Por lo general, un usuario de mensajería que envía en su propio nombre deja sin conjunto las propiedades del remitente representado.</span><span class="sxs-lookup"><span data-stu-id="cd237-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="cd237-118">El proveedor de transporte saliente siempre debe dejar esta propiedad sin cambios si el cliente de envío la ha establecido.</span><span class="sxs-lookup"><span data-stu-id="cd237-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="cd237-119">Si no se establece, el proveedor de transporte debe establecerlo en la propiedad **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) de la copia saliente del mensaje y dejarla sin establecer en la copia local.</span><span class="sxs-lookup"><span data-stu-id="cd237-119">If it is unset, the transport provider should set it to the **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cd237-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cd237-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cd237-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="cd237-121">Protocol specifications</span></span>

<span data-ttu-id="cd237-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd237-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd237-123">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="cd237-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cd237-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd237-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd237-125">Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="cd237-125">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="cd237-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd237-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd237-127">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="cd237-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="cd237-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd237-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd237-129">Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="cd237-129">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="cd237-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd237-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd237-131">Especifica métodos para conectarse y configurar buzones como delegados e interacciones con objetos de mensaje y calendario cuando actúan en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="cd237-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="cd237-132">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd237-132">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd237-133">Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="cd237-133">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="cd237-134">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd237-134">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd237-135">Especifica las propiedades y las operaciones que son permisibles para los objetos post.</span><span class="sxs-lookup"><span data-stu-id="cd237-135">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="cd237-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd237-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd237-137">Especifica las propiedades y las operaciones permitidas para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="cd237-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="cd237-138">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd237-138">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd237-139">Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficiente.</span><span class="sxs-lookup"><span data-stu-id="cd237-139">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cd237-140">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cd237-140">Header files</span></span>

<span data-ttu-id="cd237-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cd237-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="cd237-142">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cd237-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="cd237-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cd237-143">Mapitags.h</span></span>
  
> <span data-ttu-id="cd237-144">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="cd237-144">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cd237-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd237-145">See also</span></span>



[<span data-ttu-id="cd237-146">Propiedad canónica PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="cd237-146">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)


[<span data-ttu-id="cd237-147">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cd237-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cd237-148">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="cd237-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cd237-149">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="cd237-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cd237-150">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="cd237-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

