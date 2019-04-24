---
title: Propiedad canónica PidTagReceivedRepresentingName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingName
api_type:
- COM
ms.assetid: 8f699782-8a82-4834-bc55-a0b3cf18a117
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5fce7e6d2163bdb8d1682dbef10d627b34ddd889
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356738"
---
# <a name="pidtagreceivedrepresentingname-canonical-property"></a><span data-ttu-id="15c80-103">Propiedad canónica PidTagReceivedRepresentingName</span><span class="sxs-lookup"><span data-stu-id="15c80-103">PidTagReceivedRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="15c80-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15c80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15c80-105">Contiene el nombre para mostrar del usuario de mensajería representado por el usuario de recepción.</span><span class="sxs-lookup"><span data-stu-id="15c80-105">Contains the display name for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="15c80-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="15c80-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="15c80-107">PR_RCVD_REPRESENTING_NAME, PR_RCVD_REPRESENTING_NAME_A, PR_RCVD_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="15c80-107">PR_RCVD_REPRESENTING_NAME, PR_RCVD_REPRESENTING_NAME_A, PR_RCVD_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="15c80-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="15c80-108">Identifier:</span></span>  <br/> |<span data-ttu-id="15c80-109">0x0044</span><span class="sxs-lookup"><span data-stu-id="15c80-109">0x0044</span></span>  <br/> |
|<span data-ttu-id="15c80-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="15c80-110">Data type:</span></span>  <br/> |<span data-ttu-id="15c80-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="15c80-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="15c80-112">Área:</span><span class="sxs-lookup"><span data-stu-id="15c80-112">Area:</span></span>  <br/> |<span data-ttu-id="15c80-113">Address</span><span class="sxs-lookup"><span data-stu-id="15c80-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15c80-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="15c80-114">Remarks</span></span>

<span data-ttu-id="15c80-115">Estas propiedades son ejemplos de las propiedades de dirección del usuario de mensajería que representa el usuario receptor.</span><span class="sxs-lookup"><span data-stu-id="15c80-115">These properties are examples of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="15c80-116">El proveedor de transporte entrante debe establecerlos, que también es responsable de la autorización o la comprobación del delegado.</span><span class="sxs-lookup"><span data-stu-id="15c80-116">They must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="15c80-117">Si no se está representando un usuario de mensajería, estas propiedades deben establecerse en el nombre para mostrar contenido en la propiedad **PR_RECEIVED_BY_NAME** ([PidTagReceivedByName](pidtagreceivedbyname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="15c80-117">If no messaging user is being represented, these properties should be set to the display name contained in the **PR_RECEIVED_BY_NAME** ([PidTagReceivedByName](pidtagreceivedbyname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="15c80-118">Una aplicación cliente que responde a un mensaje recibido en nombre de otro cliente debe copiar estas propiedades del mensaje recibido en la propiedad **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="15c80-118">A client application replying to a message received on behalf of another client should copy these properties from the received message into the **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="15c80-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="15c80-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="15c80-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="15c80-120">Protocol specifications</span></span>

<span data-ttu-id="15c80-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15c80-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15c80-122">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="15c80-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="15c80-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15c80-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15c80-124">Especifica las propiedades y operaciones que se admiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="15c80-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="15c80-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15c80-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15c80-126">Controla el orden y el flujo de transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="15c80-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="15c80-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15c80-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15c80-128">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="15c80-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="15c80-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15c80-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15c80-130">Especifica los métodos para conectarse a los buzones y configurarlos como delegados, e interacciones con los objetos Message y Calendar cuando actúan en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="15c80-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="15c80-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15c80-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15c80-132">Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="15c80-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="15c80-133">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="15c80-133">Header files</span></span>

<span data-ttu-id="15c80-134">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="15c80-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="15c80-135">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="15c80-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="15c80-136">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="15c80-136">Mapitags.h</span></span>
  
> <span data-ttu-id="15c80-137">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="15c80-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15c80-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="15c80-138">See also</span></span>



[<span data-ttu-id="15c80-139">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="15c80-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="15c80-140">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="15c80-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="15c80-141">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="15c80-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="15c80-142">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="15c80-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

