---
title: Propiedad canónica PidTagReceivedRepresentingEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingEntryId
api_type:
- COM
ms.assetid: 2ae2266c-f093-41e5-b4d0-e12aa0f03190
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 12e4c97947cfe579f550cc6d48ca0b64750b9ab6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820014"
---
# <a name="pidtagreceivedrepresentingentryid-canonical-property"></a><span data-ttu-id="c9b92-103">Propiedad canónica PidTagReceivedRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="c9b92-103">PidTagReceivedRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c9b92-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c9b92-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c9b92-105">Contiene el identificador de entrada del usuario de mensajería que está representada por el usuario receptora.</span><span class="sxs-lookup"><span data-stu-id="c9b92-105">Contains the entry identifier for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9b92-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c9b92-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c9b92-107">PR_RCVD_REPRESENTING_ENTRYID DE MAPI</span><span class="sxs-lookup"><span data-stu-id="c9b92-107">PR_RCVD_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="c9b92-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c9b92-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c9b92-109">0x0043</span><span class="sxs-lookup"><span data-stu-id="c9b92-109">0x0043</span></span>  <br/> |
|<span data-ttu-id="c9b92-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c9b92-110">Data type:</span></span>  <br/> |<span data-ttu-id="c9b92-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c9b92-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c9b92-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c9b92-112">Area:</span></span>  <br/> |<span data-ttu-id="c9b92-113">Address</span><span class="sxs-lookup"><span data-stu-id="c9b92-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9b92-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c9b92-114">Remarks</span></span>

<span data-ttu-id="c9b92-115">Esta propiedad es una de las propiedades de la dirección del usuario de mensajería que se va a representar el usuario receptora.</span><span class="sxs-lookup"><span data-stu-id="c9b92-115">This property is one of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="c9b92-116">Se debe establecer por el proveedor de transporte entrante, que también es responsable de la autorización o comprobación del delegado.</span><span class="sxs-lookup"><span data-stu-id="c9b92-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="c9b92-117">Si no se va a representar ningún usuario de mensajería, esta propiedad debe establecerse en el identificador de entrada contenido en la propiedad **PR_RECEIVED_BY_ENTRYID de MAPI** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c9b92-117">If no messaging user is being represented, this property should be set to the entry identifier contained in the **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="c9b92-118">Una aplicación cliente que responder a un mensaje recibido en nombre de otro cliente debe copiar esta propiedad desde el mensaje recibido en la propiedad **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) para la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c9b92-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c9b92-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9b92-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c9b92-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c9b92-120">Protocol specifications</span></span>

<span data-ttu-id="c9b92-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9b92-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9b92-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c9b92-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c9b92-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9b92-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9b92-124">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c9b92-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="c9b92-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9b92-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9b92-126">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="c9b92-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="c9b92-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9b92-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9b92-128">Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con objetos de mensaje y calendario cuando actúen en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="c9b92-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c9b92-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c9b92-129">Header files</span></span>

<span data-ttu-id="c9b92-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9b92-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9b92-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c9b92-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="c9b92-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c9b92-132">Mapitags.h</span></span>
  
> <span data-ttu-id="c9b92-133">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="c9b92-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9b92-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9b92-134">See also</span></span>



[<span data-ttu-id="c9b92-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c9b92-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9b92-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c9b92-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9b92-137">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c9b92-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9b92-138">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c9b92-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

