---
title: Propiedad canónica PidTagReceivedRepresentingEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingEmailAddress
api_type:
- COM
ms.assetid: f85ce31c-f621-47ed-badf-4f59a45ec0a1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6916b1148caaf8283c6d7ae64ac2e05deb3ee0c3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398881"
---
# <a name="pidtagreceivedrepresentingemailaddress-canonical-property"></a><span data-ttu-id="6ba37-103">Propiedad canónica PidTagReceivedRepresentingEmailAddress</span><span class="sxs-lookup"><span data-stu-id="6ba37-103">PidTagReceivedRepresentingEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="6ba37-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ba37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ba37-105">Contiene la dirección de correo electrónico del usuario de mensajería que está representada por el usuario receptora.</span><span class="sxs-lookup"><span data-stu-id="6ba37-105">Contains the email address for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6ba37-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6ba37-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6ba37-107">PR_RCVD_REPRESENTING_EMAIL_ADDRESS, PR_RCVD_REPRESENTING_EMAIL_ADDRESS_A, PR_RCVD_REPRESENTING_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="6ba37-107">PR_RCVD_REPRESENTING_EMAIL_ADDRESS, PR_RCVD_REPRESENTING_EMAIL_ADDRESS_A, PR_RCVD_REPRESENTING_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="6ba37-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6ba37-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6ba37-109">0 x 0078</span><span class="sxs-lookup"><span data-stu-id="6ba37-109">0x0078</span></span>  <br/> |
|<span data-ttu-id="6ba37-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6ba37-110">Data type:</span></span>  <br/> |<span data-ttu-id="6ba37-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="6ba37-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="6ba37-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6ba37-112">Area:</span></span>  <br/> |<span data-ttu-id="6ba37-113">Address</span><span class="sxs-lookup"><span data-stu-id="6ba37-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ba37-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6ba37-114">Remarks</span></span>

<span data-ttu-id="6ba37-115">Estas propiedades son ejemplos de las propiedades de la dirección del usuario de mensajería que se va a representar el usuario receptora.</span><span class="sxs-lookup"><span data-stu-id="6ba37-115">These properties are examples of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="6ba37-116">Se deben configurar por el proveedor de transporte entrante, que también es responsable de la autorización o comprobación del delegado.</span><span class="sxs-lookup"><span data-stu-id="6ba37-116">They must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="6ba37-117">Si no se va a representar ningún usuario de mensajería, estas propiedades deben establecerse en la dirección de correo electrónico contenida en la propiedad **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6ba37-117">If no messaging user is being represented, these properties should be set to the email address contained in the **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="6ba37-118">Una aplicación cliente que responder a un mensaje recibido en nombre de otro cliente debe copiar estas propiedades desde el mensaje recibido en la propiedad **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) para el respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ba37-118">A client application replying to a message received on behalf of another client should copy these properties from the received message into the **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6ba37-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6ba37-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6ba37-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="6ba37-120">Protocol specifications</span></span>

<span data-ttu-id="6ba37-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ba37-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ba37-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="6ba37-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6ba37-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ba37-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ba37-124">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="6ba37-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="6ba37-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ba37-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ba37-126">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="6ba37-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="6ba37-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ba37-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ba37-128">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="6ba37-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="6ba37-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ba37-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ba37-130">Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con objetos de mensaje y calendario cuando actúen en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="6ba37-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="6ba37-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ba37-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ba37-132">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="6ba37-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6ba37-133">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6ba37-133">Header files</span></span>

<span data-ttu-id="6ba37-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6ba37-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="6ba37-135">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6ba37-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="6ba37-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6ba37-136">Mapitags.h</span></span>
  
> <span data-ttu-id="6ba37-137">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="6ba37-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6ba37-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ba37-138">See also</span></span>



[<span data-ttu-id="6ba37-139">Propiedad canónica PidTagEmailAddress</span><span class="sxs-lookup"><span data-stu-id="6ba37-139">PidTagEmailAddress Canonical Property</span></span>](pidtagemailaddress-canonical-property.md)


[<span data-ttu-id="6ba37-140">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6ba37-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6ba37-141">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="6ba37-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6ba37-142">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="6ba37-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6ba37-143">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="6ba37-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

