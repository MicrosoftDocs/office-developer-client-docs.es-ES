---
title: Propiedad canónica PidTagReceivedByName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByName
api_type:
- COM
ms.assetid: edd29217-74bb-4321-82fd-65f0fbfd05f8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 039a51c2bb4cf1fe2a83e2ba144a87462b5d6d0c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359216"
---
# <a name="pidtagreceivedbyname-canonical-property"></a><span data-ttu-id="46af6-103">Propiedad canónica PidTagReceivedByName</span><span class="sxs-lookup"><span data-stu-id="46af6-103">PidTagReceivedByName Canonical Property</span></span>

  
  
<span data-ttu-id="46af6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46af6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46af6-105">Contiene el nombre para mostrar del usuario de mensajería que recibe el mensaje.</span><span class="sxs-lookup"><span data-stu-id="46af6-105">Contains the display name of the messaging user who receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="46af6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="46af6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="46af6-107">PR_RECEIVED_BY_NAME, PR_RECEIVED_BY_NAME_A, PR_RECEIVED_BY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="46af6-107">PR_RECEIVED_BY_NAME, PR_RECEIVED_BY_NAME_A, PR_RECEIVED_BY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="46af6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="46af6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="46af6-109">0x0040</span><span class="sxs-lookup"><span data-stu-id="46af6-109">0x0040</span></span>  <br/> |
|<span data-ttu-id="46af6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="46af6-110">Data type:</span></span>  <br/> |<span data-ttu-id="46af6-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="46af6-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="46af6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="46af6-112">Area:</span></span>  <br/> |<span data-ttu-id="46af6-113">Address</span><span class="sxs-lookup"><span data-stu-id="46af6-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46af6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="46af6-114">Remarks</span></span>

<span data-ttu-id="46af6-115">Estas propiedades son un ejemplo de las propiedades de dirección del usuario de mensajería que recibe el mensaje.</span><span class="sxs-lookup"><span data-stu-id="46af6-115">These properties are an example of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="46af6-116">El proveedor de transporte entrante debe establecerlos.</span><span class="sxs-lookup"><span data-stu-id="46af6-116">They must be set by the incoming transport provider.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="46af6-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="46af6-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="46af6-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="46af6-118">Protocol specifications</span></span>

<span data-ttu-id="46af6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46af6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46af6-120">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="46af6-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="46af6-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46af6-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46af6-122">Especifica las propiedades y operaciones que se admiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="46af6-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="46af6-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46af6-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46af6-124">Controla el orden y el flujo de transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="46af6-124">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="46af6-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46af6-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46af6-126">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="46af6-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="46af6-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46af6-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46af6-128">Especifica los métodos para conectarse a los buzones y configurarlos como delegados, e interacciones con los objetos Message y Calendar cuando actúan en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="46af6-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="46af6-129">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46af6-129">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46af6-130">Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="46af6-130">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="46af6-131">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="46af6-131">Header files</span></span>

<span data-ttu-id="46af6-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="46af6-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="46af6-133">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="46af6-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="46af6-134">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="46af6-134">Mapitags.h</span></span>
  
> <span data-ttu-id="46af6-135">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="46af6-135">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="46af6-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="46af6-136">See also</span></span>



[<span data-ttu-id="46af6-137">Propiedad canónica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="46af6-137">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="46af6-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="46af6-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="46af6-139">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="46af6-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="46af6-140">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="46af6-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="46af6-141">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="46af6-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

