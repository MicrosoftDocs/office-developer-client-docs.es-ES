---
title: Propiedad canónica PidTagDeliveryPoint
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliveryPoint
api_type:
- HeaderDef
ms.assetid: 715a9dbd-78f8-41e1-a76e-29448d06ec19
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e18b08bcbd76cacf7dbb5b5fd36d80d5f266364d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439425"
---
# <a name="pidtagdeliverypoint-canonical-property"></a><span data-ttu-id="2026a-103">Propiedad canónica PidTagDeliveryPoint</span><span class="sxs-lookup"><span data-stu-id="2026a-103">PidTagDeliveryPoint Canonical Property</span></span>

  
  
<span data-ttu-id="2026a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2026a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2026a-105">Especifica la naturaleza de la entidad funcional por medio de la cual se entregó un mensaje al destinatario.</span><span class="sxs-lookup"><span data-stu-id="2026a-105">Specifies the nature of the functional entity by means of which a message was or would have been delivered to the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2026a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2026a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2026a-107">PR_DELIVERY_POINT</span><span class="sxs-lookup"><span data-stu-id="2026a-107">PR_DELIVERY_POINT</span></span>  <br/> |
|<span data-ttu-id="2026a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2026a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2026a-109">0x0C07</span><span class="sxs-lookup"><span data-stu-id="2026a-109">0x0C07</span></span>  <br/> |
|<span data-ttu-id="2026a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2026a-110">Data type:</span></span>  <br/> |<span data-ttu-id="2026a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2026a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2026a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2026a-112">Area:</span></span>  <br/> |<span data-ttu-id="2026a-113">Destinatario MAPI</span><span class="sxs-lookup"><span data-stu-id="2026a-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2026a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2026a-114">Remarks</span></span>

<span data-ttu-id="2026a-115">Esta propiedad puede tener exactamente uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="2026a-115">This property can have exactly one of the following values:</span></span> 
  
<span data-ttu-id="2026a-116">MAPI_MH_DP_ML</span><span class="sxs-lookup"><span data-stu-id="2026a-116">MAPI_MH_DP_ML</span></span> 
  
> <span data-ttu-id="2026a-117">Entregado a una lista de distribución, un punto de entrega que a su vez puede distribuir el mensaje a muchos destinatarios.</span><span class="sxs-lookup"><span data-stu-id="2026a-117">Delivered to a distribution list, a delivery point which in turn may distribute the message to many recipients.</span></span>
    
<span data-ttu-id="2026a-118">MAPI_MH_DP_MS</span><span class="sxs-lookup"><span data-stu-id="2026a-118">MAPI_MH_DP_MS</span></span> 
  
> <span data-ttu-id="2026a-119">Se entrega a un almacén de mensajes en lugar de directamente a un destinatario.</span><span class="sxs-lookup"><span data-stu-id="2026a-119">Delivered to a message store instead of directly to a recipient.</span></span>
    
<span data-ttu-id="2026a-120">MAPI_MH_DP_OTHER_AU</span><span class="sxs-lookup"><span data-stu-id="2026a-120">MAPI_MH_DP_OTHER_AU</span></span> 
  
> <span data-ttu-id="2026a-121">Se entrega a una unidad de acceso (AU) que no sea una unidad de acceso de entrega física (PDAU), como un sistema FAX.</span><span class="sxs-lookup"><span data-stu-id="2026a-121">Delivered to an access unit (AU) other than a physical delivery access unit (PDAU), such as a FAX system.</span></span>
    
<span data-ttu-id="2026a-122">MAPI_MH_DP_PDAU</span><span class="sxs-lookup"><span data-stu-id="2026a-122">MAPI_MH_DP_PDAU</span></span> 
  
> <span data-ttu-id="2026a-123">Entregado a una unidad de acceso de entrega física, como un operador postal humano.</span><span class="sxs-lookup"><span data-stu-id="2026a-123">Delivered to a physical delivery access unit, such as a human postal carrier.</span></span>
    
<span data-ttu-id="2026a-124">MAPI_MH_DP_PDS_PATRON</span><span class="sxs-lookup"><span data-stu-id="2026a-124">MAPI_MH_DP_PDS_PATRON</span></span> 
  
> <span data-ttu-id="2026a-125">Se entrega a un sistema de entrega físico, como un buzón postal convencional.</span><span class="sxs-lookup"><span data-stu-id="2026a-125">Delivered to a physical delivery system patron, such as a conventional postal mailbox.</span></span>
    
<span data-ttu-id="2026a-126">MAPI_MH_DP_PRIVATE_UA</span><span class="sxs-lookup"><span data-stu-id="2026a-126">MAPI_MH_DP_PRIVATE_UA</span></span> 
  
> <span data-ttu-id="2026a-127">Se entrega a un agente de usuario privado (UA), como un cliente en un sistema de mensajería local.</span><span class="sxs-lookup"><span data-stu-id="2026a-127">Delivered to a private user agent (UA), such as a client in an in-house messaging system.</span></span>
    
<span data-ttu-id="2026a-128">MAPI_MH_DP_PUBLIC_UA</span><span class="sxs-lookup"><span data-stu-id="2026a-128">MAPI_MH_DP_PUBLIC_UA</span></span> 
  
> <span data-ttu-id="2026a-129">Se entrega a un agente de usuario público o a un proveedor de servicios públicos.</span><span class="sxs-lookup"><span data-stu-id="2026a-129">Delivered to a public user agent, or public service provider.</span></span>
    
<span data-ttu-id="2026a-130">El valor predeterminado es MAPI_MH_DP_PRIVATE_UA, es decir, un cliente MAPI.</span><span class="sxs-lookup"><span data-stu-id="2026a-130">The default value is MAPI_MH_DP_PRIVATE_UA, that is, a MAPI client.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2026a-131">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2026a-131">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2026a-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2026a-132">Header files</span></span>

<span data-ttu-id="2026a-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2026a-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="2026a-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2026a-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="2026a-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2026a-135">Mapitags.h</span></span>
  
> <span data-ttu-id="2026a-136">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="2026a-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2026a-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2026a-137">See also</span></span>



[<span data-ttu-id="2026a-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2026a-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2026a-139">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="2026a-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2026a-140">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2026a-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2026a-141">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="2026a-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

