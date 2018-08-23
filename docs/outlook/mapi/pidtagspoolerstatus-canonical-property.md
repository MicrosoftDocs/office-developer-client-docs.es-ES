---
title: Propiedad canónica PidTagSpoolerStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSpoolerStatus
api_type:
- COM
ms.assetid: a10d86fc-3a73-49dc-b974-ed852ec715e9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d04144a4f5ef714b59b608bfe19367bcb3c1ced8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588576"
---
# <a name="pidtagspoolerstatus-canonical-property"></a><span data-ttu-id="c2c1c-103">Propiedad canónica PidTagSpoolerStatus</span><span class="sxs-lookup"><span data-stu-id="c2c1c-103">PidTagSpoolerStatus Canonical Property</span></span>

  
  
<span data-ttu-id="c2c1c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2c1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2c1c-105">Contiene el estado del mensaje según la información que está disponible para la cola de MAPI.</span><span class="sxs-lookup"><span data-stu-id="c2c1c-105">Contains the status of the message based on information that is available to the MAPI spooler.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c2c1c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c2c1c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c2c1c-107">PR_SPOOLER_STATUS</span><span class="sxs-lookup"><span data-stu-id="c2c1c-107">PR_SPOOLER_STATUS</span></span>  <br/> |
|<span data-ttu-id="c2c1c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c2c1c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c2c1c-109">0x0E10</span><span class="sxs-lookup"><span data-stu-id="c2c1c-109">0x0E10</span></span>  <br/> |
|<span data-ttu-id="c2c1c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c2c1c-110">Data type:</span></span>  <br/> |<span data-ttu-id="c2c1c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c2c1c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c2c1c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c2c1c-112">Area:</span></span>  <br/> |<span data-ttu-id="c2c1c-113">MAPI no transmisible</span><span class="sxs-lookup"><span data-stu-id="c2c1c-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2c1c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c2c1c-114">Remarks</span></span>

<span data-ttu-id="c2c1c-115">Esta propiedad se calcula mediante MAPI en objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="c2c1c-115">This property is computed by MAPI on message objects.</span></span>
  
<span data-ttu-id="c2c1c-116">Esta propiedad aparece en los mensajes entrantes sólo y está reservada en todos los demás casos.</span><span class="sxs-lookup"><span data-stu-id="c2c1c-116">This property appears on inbound messages only and is reserved in all other cases.</span></span> <span data-ttu-id="c2c1c-117">Indica si un mensaje se ha entregado a su ubicación final o si un proveedor de enlace de mensajería potencialmente elimina el mensaje mientras se reenrutamiento.</span><span class="sxs-lookup"><span data-stu-id="c2c1c-117">It indicates whether or not a message has been delivered to its final location or whether a messaging hook provider potentially deleted the message while rerouting it.</span></span>
  
<span data-ttu-id="c2c1c-118">Aplicaciones de cliente nunca deben establecer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="c2c1c-118">Client applications should never set this property.</span></span> <span data-ttu-id="c2c1c-119">Para un mensaje entrante, un proveedor de servicio o cliente puede llamar a [IMAPIProp::GetProps](imapiprop-getprops.md) en esta propiedad para determinar el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="c2c1c-119">For an inbound message, a client or service provider can call [IMAPIProp::GetProps](imapiprop-getprops.md) on this property to determine the message status.</span></span> <span data-ttu-id="c2c1c-120">El valor S_OK indica que el mensaje se entregó correctamente al almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c2c1c-120">The value S_OK indicates that the message was successfully delivered to the message store.</span></span> <span data-ttu-id="c2c1c-121">El valor MAPI_E_OBJECT_DELETED indica que el mensaje se eliminó y nunca se ha confirmado en el almacén.</span><span class="sxs-lookup"><span data-stu-id="c2c1c-121">The value MAPI_E_OBJECT_DELETED indicates that the message was deleted and was never committed to the store.</span></span> 
  
<span data-ttu-id="c2c1c-122">Los proveedores de almacén de mensajes deben admitir esta propiedad en los mensajes, tablas de destinatarios y la tabla de cola saliente.</span><span class="sxs-lookup"><span data-stu-id="c2c1c-122">Message store providers should support this property on messages, recipient tables, and the outgoing queue table.</span></span> <span data-ttu-id="c2c1c-123">Los clientes y proveedores deben ser capaces de establecer columnas en la tabla cola saliente y restringir en función de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="c2c1c-123">Clients and providers should be able to set columns on the outgoing queue table and restrict based on this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c2c1c-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2c1c-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c2c1c-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c2c1c-125">Header files</span></span>

<span data-ttu-id="c2c1c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c2c1c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c2c1c-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c2c1c-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="c2c1c-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c2c1c-128">Mapitags.h</span></span>
  
> <span data-ttu-id="c2c1c-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c2c1c-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c2c1c-130">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c2c1c-130">See also</span></span>



[<span data-ttu-id="c2c1c-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c2c1c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c2c1c-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c2c1c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c2c1c-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c2c1c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c2c1c-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c2c1c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

