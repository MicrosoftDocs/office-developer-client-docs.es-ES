---
title: Propiedad canónica PidTagReceivedByEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByEntryId
api_type:
- COM
ms.assetid: 737f8584-fc52-4324-ac40-2fc554a3095d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ab3ffed8dd5b8d73d8024d27790f18397d615c2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567471"
---
# <a name="pidtagreceivedbyentryid-canonical-property"></a><span data-ttu-id="f83d8-103">Propiedad canónica PidTagReceivedByEntryId</span><span class="sxs-lookup"><span data-stu-id="f83d8-103">PidTagReceivedByEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="f83d8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f83d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f83d8-105">Contiene el identificador de entrada del usuario de mensajería que reciba el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f83d8-105">Contains the entry identifier of the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f83d8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f83d8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f83d8-107">PR_RECEIVED_BY_ENTRYID DE MAPI</span><span class="sxs-lookup"><span data-stu-id="f83d8-107">PR_RECEIVED_BY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="f83d8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f83d8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f83d8-109">0x003F</span><span class="sxs-lookup"><span data-stu-id="f83d8-109">0x003F</span></span>  <br/> |
|<span data-ttu-id="f83d8-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f83d8-110">Data type:</span></span>  <br/> |<span data-ttu-id="f83d8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f83d8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f83d8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f83d8-112">Area:</span></span>  <br/> |<span data-ttu-id="f83d8-113">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="f83d8-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f83d8-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f83d8-114">Remarks</span></span>

<span data-ttu-id="f83d8-115">Esta propiedad es una de las propiedades de la dirección del usuario de mensajería que recibe el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f83d8-115">This property is one of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="f83d8-116">Se debe establecer por el proveedor de transporte entrante.</span><span class="sxs-lookup"><span data-stu-id="f83d8-116">It must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="f83d8-117">Esta propiedad corresponde a un atributo X.400 entrega envelope por mensaje MH_T_.</span><span class="sxs-lookup"><span data-stu-id="f83d8-117">This property corresponds to an X.400 delivery envelope per-message MH_T_ attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f83d8-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f83d8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f83d8-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f83d8-119">Protocol specifications</span></span>

<span data-ttu-id="f83d8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f83d8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f83d8-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f83d8-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f83d8-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f83d8-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f83d8-123">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f83d8-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="f83d8-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f83d8-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f83d8-125">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="f83d8-125">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="f83d8-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f83d8-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f83d8-127">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y elementos de reunión.</span><span class="sxs-lookup"><span data-stu-id="f83d8-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
<span data-ttu-id="f83d8-128">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f83d8-128">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f83d8-129">Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con objetos de mensaje y calendario cuando actúen en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="f83d8-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="f83d8-130">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f83d8-130">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f83d8-131">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="f83d8-131">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f83d8-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f83d8-132">Header files</span></span>

<span data-ttu-id="f83d8-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f83d8-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="f83d8-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f83d8-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="f83d8-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f83d8-135">Mapitags.h</span></span>
  
> <span data-ttu-id="f83d8-136">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="f83d8-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f83d8-137">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f83d8-137">See also</span></span>



[<span data-ttu-id="f83d8-138">Propiedad canónica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="f83d8-138">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="f83d8-139">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f83d8-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f83d8-140">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f83d8-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f83d8-141">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f83d8-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f83d8-142">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f83d8-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

