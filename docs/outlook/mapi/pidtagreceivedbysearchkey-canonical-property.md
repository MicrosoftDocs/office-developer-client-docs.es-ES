---
title: Propiedad canónica PidTagReceivedBySearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedBySearchKey
api_type:
- COM
ms.assetid: 4b37555a-1d07-4f42-95e3-b8fa37ed0c3b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a139c39c5814b22d9b55bc937a7c300d89f1d5bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820033"
---
# <a name="pidtagreceivedbysearchkey-canonical-property"></a><span data-ttu-id="fc02d-103">Propiedad canónica PidTagReceivedBySearchKey</span><span class="sxs-lookup"><span data-stu-id="fc02d-103">PidTagReceivedBySearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="fc02d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fc02d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fc02d-105">Contiene la clave de búsqueda del usuario de mensajería que recibe el mensaje.</span><span class="sxs-lookup"><span data-stu-id="fc02d-105">Contains the search key of the messaging user who receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fc02d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fc02d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc02d-107">PR_RECEIVED_BY_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="fc02d-107">PR_RECEIVED_BY_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="fc02d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fc02d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fc02d-109">0x0051</span><span class="sxs-lookup"><span data-stu-id="fc02d-109">0x0051</span></span>  <br/> |
|<span data-ttu-id="fc02d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fc02d-110">Data type:</span></span>  <br/> |<span data-ttu-id="fc02d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fc02d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fc02d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fc02d-112">Area:</span></span>  <br/> |<span data-ttu-id="fc02d-113">Address</span><span class="sxs-lookup"><span data-stu-id="fc02d-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc02d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fc02d-114">Remarks</span></span>

<span data-ttu-id="fc02d-115">Esta propiedad es una de las propiedades de la dirección del usuario de mensajería que recibe el mensaje.</span><span class="sxs-lookup"><span data-stu-id="fc02d-115">This property is one of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="fc02d-116">Se debe establecer por el proveedor de transporte entrante.</span><span class="sxs-lookup"><span data-stu-id="fc02d-116">It must be set by the incoming transport provider.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fc02d-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc02d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fc02d-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="fc02d-118">Protocol specifications</span></span>

<span data-ttu-id="fc02d-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc02d-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc02d-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fc02d-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fc02d-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc02d-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc02d-122">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="fc02d-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="fc02d-123">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc02d-123">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc02d-124">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="fc02d-124">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="fc02d-125">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc02d-125">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc02d-126">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="fc02d-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="fc02d-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc02d-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc02d-128">Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con objetos de mensaje y calendario cuando actúen en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="fc02d-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="fc02d-129">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc02d-129">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc02d-130">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="fc02d-130">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fc02d-131">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fc02d-131">Header files</span></span>

<span data-ttu-id="fc02d-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc02d-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc02d-133">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fc02d-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="fc02d-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fc02d-134">Mapitags.h</span></span>
  
> <span data-ttu-id="fc02d-135">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="fc02d-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc02d-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc02d-136">See also</span></span>



[<span data-ttu-id="fc02d-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fc02d-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fc02d-138">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="fc02d-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fc02d-139">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fc02d-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fc02d-140">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="fc02d-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

