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
ms.openlocfilehash: 33e41343e0c159be20ed1499fc24223947975e1d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359097"
---
# <a name="pidtagreceivedrepresentingentryid-canonical-property"></a><span data-ttu-id="7d457-103">Propiedad canónica PidTagReceivedRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="7d457-103">PidTagReceivedRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="7d457-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d457-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d457-105">Contiene el identificador de entrada para el usuario de mensajería representado por el usuario receptor.</span><span class="sxs-lookup"><span data-stu-id="7d457-105">Contains the entry identifier for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7d457-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7d457-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7d457-107">PR_RCVD_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7d457-107">PR_RCVD_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="7d457-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7d457-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7d457-109">0x0043</span><span class="sxs-lookup"><span data-stu-id="7d457-109">0x0043</span></span>  <br/> |
|<span data-ttu-id="7d457-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7d457-110">Data type:</span></span>  <br/> |<span data-ttu-id="7d457-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7d457-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7d457-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7d457-112">Area:</span></span>  <br/> |<span data-ttu-id="7d457-113">Address</span><span class="sxs-lookup"><span data-stu-id="7d457-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d457-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7d457-114">Remarks</span></span>

<span data-ttu-id="7d457-115">Esta propiedad es una de las propiedades de dirección para el usuario de mensajería que representa el usuario receptor.</span><span class="sxs-lookup"><span data-stu-id="7d457-115">This property is one of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="7d457-116">Debe ser establecido por el proveedor de transporte entrante, que también es responsable de la autorización o comprobación del delegado.</span><span class="sxs-lookup"><span data-stu-id="7d457-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="7d457-117">Si no se está representando un usuario de mensajería, esta propiedad debe establecerse en el identificador de entrada contenido en la propiedad **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7d457-117">If no messaging user is being represented, this property should be set to the entry identifier contained in the **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="7d457-118">Una aplicación cliente que responde a un mensaje recibido en nombre de otro cliente debe copiar esta propiedad del mensaje recibido en la propiedad **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7d457-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7d457-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d457-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7d457-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="7d457-120">Protocol specifications</span></span>

<span data-ttu-id="7d457-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d457-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d457-122">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7d457-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7d457-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d457-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d457-124">Especifica las propiedades y operaciones que se admiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="7d457-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="7d457-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d457-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d457-126">Controla el orden y el flujo de transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="7d457-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="7d457-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d457-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d457-128">Especifica los métodos para conectarse a los buzones y configurarlos como delegados, e interacciones con los objetos Message y Calendar cuando actúan en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="7d457-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7d457-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7d457-129">Header files</span></span>

<span data-ttu-id="7d457-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7d457-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="7d457-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7d457-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="7d457-132">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7d457-132">Mapitags.h</span></span>
  
> <span data-ttu-id="7d457-133">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="7d457-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d457-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d457-134">See also</span></span>



[<span data-ttu-id="7d457-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7d457-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7d457-136">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="7d457-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7d457-137">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7d457-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7d457-138">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="7d457-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

