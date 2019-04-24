---
title: Propiedad canónica PidTagReceivedByEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByEmailAddress
api_type:
- COM
ms.assetid: 5f9ebe20-b037-422b-9991-69f85122a706
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cea63037f926cdd178b6036c82e87cbba48d7347
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359237"
---
# <a name="pidtagreceivedbyemailaddress-canonical-property"></a><span data-ttu-id="f29a1-103">Propiedad canónica PidTagReceivedByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f29a1-103">PidTagReceivedByEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="f29a1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f29a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f29a1-105">Contiene la dirección de correo electrónico del usuario de mensajería que recibe el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f29a1-105">Contains the email address for the messaging user who receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f29a1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f29a1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f29a1-107">PR_RECEIVED_BY_EMAIL_ADDRESS, PR_RECEIVED_BY_EMAIL_ADDRESS_A, PR_RECEIVED_BY_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="f29a1-107">PR_RECEIVED_BY_EMAIL_ADDRESS, PR_RECEIVED_BY_EMAIL_ADDRESS_A, PR_RECEIVED_BY_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="f29a1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f29a1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f29a1-109">0x0076</span><span class="sxs-lookup"><span data-stu-id="f29a1-109">0x0076</span></span>  <br/> |
|<span data-ttu-id="f29a1-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f29a1-110">Data type:</span></span>  <br/> |<span data-ttu-id="f29a1-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="f29a1-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="f29a1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f29a1-112">Area:</span></span>  <br/> |<span data-ttu-id="f29a1-113">Address</span><span class="sxs-lookup"><span data-stu-id="f29a1-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f29a1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f29a1-114">Remarks</span></span>

<span data-ttu-id="f29a1-115">Estas propiedades son ejemplos de las propiedades de dirección del usuario de mensajería que recibe el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f29a1-115">These properties are examples of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="f29a1-116">El proveedor de transporte entrante debe establecerlos.</span><span class="sxs-lookup"><span data-stu-id="f29a1-116">They must be set by the incoming transport provider.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f29a1-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f29a1-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f29a1-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f29a1-118">Protocol specifications</span></span>

<span data-ttu-id="f29a1-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f29a1-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f29a1-120">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f29a1-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f29a1-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f29a1-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f29a1-122">Especifica las propiedades y operaciones que se admiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f29a1-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="f29a1-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f29a1-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f29a1-124">Controla el orden y el flujo de transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="f29a1-124">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="f29a1-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f29a1-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f29a1-126">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="f29a1-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="f29a1-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f29a1-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f29a1-128">Especifica los métodos para conectarse a los buzones y configurarlos como delegados, e interacciones con los objetos Message y Calendar cuando actúan en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="f29a1-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="f29a1-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f29a1-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f29a1-130">Especifica las propiedades y operaciones que se admiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f29a1-130">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="f29a1-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f29a1-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f29a1-132">Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="f29a1-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f29a1-133">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f29a1-133">Header files</span></span>

<span data-ttu-id="f29a1-134">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f29a1-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="f29a1-135">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f29a1-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="f29a1-136">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f29a1-136">Mapitags.h</span></span>
  
> <span data-ttu-id="f29a1-137">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="f29a1-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f29a1-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="f29a1-138">See also</span></span>



[<span data-ttu-id="f29a1-139">Propiedad canónica PidTagEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f29a1-139">PidTagEmailAddress Canonical Property</span></span>](pidtagemailaddress-canonical-property.md)


[<span data-ttu-id="f29a1-140">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f29a1-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f29a1-141">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="f29a1-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f29a1-142">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f29a1-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f29a1-143">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="f29a1-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

