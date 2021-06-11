---
title: Propiedad canónica PidTagSentRepresentingEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingEntryId
api_type:
- COM
ms.assetid: f23bde8b-94cc-48c8-891a-166aa39aa3ee
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 87d8fa21ed641b40ee679a4b5fc8d68b1050ab0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359090"
---
# <a name="pidtagsentrepresentingentryid-canonical-property"></a><span data-ttu-id="37311-103">Propiedad canónica PidTagSentRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="37311-103">PidTagSentRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="37311-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37311-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37311-105">Contiene el identificador de entrada del usuario de mensajería representado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="37311-105">Contains the entry identifier for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="37311-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="37311-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="37311-107">PR_SENT_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="37311-107">PR_SENT_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="37311-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="37311-108">Identifier:</span></span>  <br/> |<span data-ttu-id="37311-109">0x0041</span><span class="sxs-lookup"><span data-stu-id="37311-109">0x0041</span></span>  <br/> |
|<span data-ttu-id="37311-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="37311-110">Data type:</span></span>  <br/> |<span data-ttu-id="37311-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="37311-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="37311-112">Área:</span><span class="sxs-lookup"><span data-stu-id="37311-112">Area:</span></span>  <br/> |<span data-ttu-id="37311-113">Dirección</span><span class="sxs-lookup"><span data-stu-id="37311-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37311-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="37311-114">Remarks</span></span>

<span data-ttu-id="37311-115">Esta propiedad es una de las propiedades de dirección para el usuario de mensajería que representa el remitente.</span><span class="sxs-lookup"><span data-stu-id="37311-115">This property is one of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="37311-116">Cuando una aplicación cliente envía un mensaje en nombre de otro cliente, debe establecer todas las propiedades de remitente representadas en los valores de ese cliente.</span><span class="sxs-lookup"><span data-stu-id="37311-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="37311-117">Por lo general, un usuario de mensajería que envía en su propio nombre deja sin conjunto las propiedades del remitente representado.</span><span class="sxs-lookup"><span data-stu-id="37311-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="37311-118">El proveedor de transporte saliente siempre debe dejar esta propiedad sin cambios si el cliente de envío la ha establecido.</span><span class="sxs-lookup"><span data-stu-id="37311-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="37311-119">Si no se establece, el proveedor de transporte debe establecerlo en **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) en la copia saliente del mensaje y dejarla sin establecer en la copia local.</span><span class="sxs-lookup"><span data-stu-id="37311-119">If it is unset, the transport provider should set it to **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="37311-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="37311-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="37311-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="37311-121">Protocol specifications</span></span>

<span data-ttu-id="37311-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37311-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37311-123">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="37311-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="37311-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37311-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37311-125">Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="37311-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="37311-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37311-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37311-127">Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="37311-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="37311-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37311-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37311-129">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="37311-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="37311-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37311-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37311-131">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="37311-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="37311-132">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37311-132">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37311-133">Especifica métodos para conectarse y configurar buzones como delegados e interacciones con objetos de mensaje y calendario cuando actúan en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="37311-133">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="37311-134">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37311-134">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37311-135">Especifica las propiedades y las operaciones que son permisibles para los objetos post.</span><span class="sxs-lookup"><span data-stu-id="37311-135">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="37311-136">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="37311-136">Header files</span></span>

<span data-ttu-id="37311-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="37311-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="37311-138">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="37311-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="37311-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="37311-139">Mapitags.h</span></span>
  
> <span data-ttu-id="37311-140">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="37311-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="37311-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="37311-141">See also</span></span>



[<span data-ttu-id="37311-142">Propiedad canónica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="37311-142">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="37311-143">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="37311-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="37311-144">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="37311-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="37311-145">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="37311-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="37311-146">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="37311-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

