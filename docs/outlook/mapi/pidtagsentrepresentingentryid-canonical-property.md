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
# <a name="pidtagsentrepresentingentryid-canonical-property"></a><span data-ttu-id="ead11-103">Propiedad canónica PidTagSentRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="ead11-103">PidTagSentRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="ead11-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ead11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ead11-105">Contiene el identificador de entrada del usuario de mensajería representado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="ead11-105">Contains the entry identifier for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ead11-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ead11-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ead11-107">PR_SENT_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ead11-107">PR_SENT_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="ead11-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ead11-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ead11-109">0x0041</span><span class="sxs-lookup"><span data-stu-id="ead11-109">0x0041</span></span>  <br/> |
|<span data-ttu-id="ead11-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ead11-110">Data type:</span></span>  <br/> |<span data-ttu-id="ead11-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ead11-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ead11-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ead11-112">Area:</span></span>  <br/> |<span data-ttu-id="ead11-113">Address</span><span class="sxs-lookup"><span data-stu-id="ead11-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ead11-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ead11-114">Remarks</span></span>

<span data-ttu-id="ead11-115">Esta propiedad es una de las propiedades de dirección del usuario de mensajería que representa el remitente.</span><span class="sxs-lookup"><span data-stu-id="ead11-115">This property is one of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="ead11-116">Cuando una aplicación cliente envía un mensaje en nombre de otro cliente, debe establecer todas las propiedades de remitente representadas en los valores de ese cliente.</span><span class="sxs-lookup"><span data-stu-id="ead11-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="ead11-117">Un usuario de mensajería que envía en su propio nombre normalmente deja sin conjunto las propiedades del remitente representado.</span><span class="sxs-lookup"><span data-stu-id="ead11-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="ead11-118">El proveedor de transporte saliente siempre debe dejar esta propiedad sin cambios si la ha establecido el cliente de envío.</span><span class="sxs-lookup"><span data-stu-id="ead11-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="ead11-119">Si no se establece, el proveedor de transporte debe establecerlo en **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) en la copia saliente del mensaje y dejarla sin establecer en la copia local.</span><span class="sxs-lookup"><span data-stu-id="ead11-119">If it is unset, the transport provider should set it to **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ead11-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ead11-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ead11-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="ead11-121">Protocol specifications</span></span>

<span data-ttu-id="ead11-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ead11-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ead11-123">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="ead11-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ead11-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ead11-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ead11-125">Especifica las propiedades y operaciones permitidas para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ead11-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="ead11-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ead11-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ead11-127">Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="ead11-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="ead11-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ead11-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ead11-129">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="ead11-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="ead11-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ead11-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ead11-131">Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.</span><span class="sxs-lookup"><span data-stu-id="ead11-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="ead11-132">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ead11-132">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ead11-133">Especifica métodos para conectar y configurar buzones como delegados e interacciones con objetos de mensaje y calendario cuando actúan en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="ead11-133">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="ead11-134">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ead11-134">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ead11-135">Especifica las propiedades y operaciones permitidas para los objetos post.</span><span class="sxs-lookup"><span data-stu-id="ead11-135">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ead11-136">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ead11-136">Header files</span></span>

<span data-ttu-id="ead11-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ead11-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="ead11-138">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ead11-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="ead11-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ead11-139">Mapitags.h</span></span>
  
> <span data-ttu-id="ead11-140">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="ead11-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ead11-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ead11-141">See also</span></span>



[<span data-ttu-id="ead11-142">Propiedad canónica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="ead11-142">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="ead11-143">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ead11-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ead11-144">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="ead11-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ead11-145">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ead11-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ead11-146">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="ead11-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

