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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385497"
---
# <a name="pidtagsentrepresentingentryid-canonical-property"></a><span data-ttu-id="21e27-103">Propiedad canónica PidTagSentRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="21e27-103">PidTagSentRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="21e27-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21e27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21e27-105">Contiene el identificador de entrada para el usuario de mensajería representado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="21e27-105">Contains the entry identifier for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="21e27-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="21e27-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="21e27-107">PR_SENT_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="21e27-107">PR_SENT_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="21e27-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="21e27-108">Identifier:</span></span>  <br/> |<span data-ttu-id="21e27-109">0x0041</span><span class="sxs-lookup"><span data-stu-id="21e27-109">0x0041</span></span>  <br/> |
|<span data-ttu-id="21e27-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="21e27-110">Data type:</span></span>  <br/> |<span data-ttu-id="21e27-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="21e27-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="21e27-112">Área:</span><span class="sxs-lookup"><span data-stu-id="21e27-112">Area:</span></span>  <br/> |<span data-ttu-id="21e27-113">Address</span><span class="sxs-lookup"><span data-stu-id="21e27-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21e27-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="21e27-114">Remarks</span></span>

<span data-ttu-id="21e27-115">Esta propiedad es una de las propiedades de dirección para el usuario de mensajería que se está representado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="21e27-115">This property is one of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="21e27-116">Cuando una aplicación cliente envía un mensaje en nombre de otro cliente, debe establecer todas las propiedades de remitente representado en los valores para que el cliente.</span><span class="sxs-lookup"><span data-stu-id="21e27-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="21e27-117">Un usuario de mensajería enviar en su propio nombre normalmente deja las propiedades de remitente representado no establecido.</span><span class="sxs-lookup"><span data-stu-id="21e27-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="21e27-118">El proveedor de transporte saliente siempre debe dejar esta propiedad no se modifica si se ha establecido por el cliente envío.</span><span class="sxs-lookup"><span data-stu-id="21e27-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="21e27-119">Si está establecido, el proveedor de transporte debe establecer para **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) en la copia del mensaje saliente y deje sin establecer en la copia local.</span><span class="sxs-lookup"><span data-stu-id="21e27-119">If it is unset, the transport provider should set it to **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="21e27-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="21e27-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="21e27-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="21e27-121">Protocol specifications</span></span>

<span data-ttu-id="21e27-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21e27-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21e27-123">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="21e27-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="21e27-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21e27-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21e27-125">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="21e27-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="21e27-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21e27-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21e27-127">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="21e27-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="21e27-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21e27-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21e27-129">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="21e27-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="21e27-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21e27-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21e27-131">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="21e27-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="21e27-132">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21e27-132">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21e27-133">Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con objetos de mensaje y calendario cuando actúen en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="21e27-133">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="21e27-134">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21e27-134">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21e27-135">Especifica las propiedades y operaciones que se permiten para registrar objetos.</span><span class="sxs-lookup"><span data-stu-id="21e27-135">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="21e27-136">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="21e27-136">Header files</span></span>

<span data-ttu-id="21e27-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="21e27-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="21e27-138">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="21e27-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="21e27-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="21e27-139">Mapitags.h</span></span>
  
> <span data-ttu-id="21e27-140">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="21e27-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="21e27-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="21e27-141">See also</span></span>



[<span data-ttu-id="21e27-142">Propiedad canónica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="21e27-142">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="21e27-143">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="21e27-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="21e27-144">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="21e27-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="21e27-145">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="21e27-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="21e27-146">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="21e27-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

