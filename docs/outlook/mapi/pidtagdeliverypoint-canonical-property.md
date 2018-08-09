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
ms.openlocfilehash: 803481a71d505fc9f12e77b162a91200cac505d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819441"
---
# <a name="pidtagdeliverypoint-canonical-property"></a><span data-ttu-id="c48cd-103">Propiedad canónica PidTagDeliveryPoint</span><span class="sxs-lookup"><span data-stu-id="c48cd-103">PidTagDeliveryPoint Canonical Property</span></span>

  
  
<span data-ttu-id="c48cd-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c48cd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c48cd-105">Especifica la naturaleza de la entidad funcional por medio de que un mensaje se ha o habría se ha entregado al destinatario.</span><span class="sxs-lookup"><span data-stu-id="c48cd-105">Specifies the nature of the functional entity by means of which a message was or would have been delivered to the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c48cd-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c48cd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c48cd-107">PR_DELIVERY_POINT</span><span class="sxs-lookup"><span data-stu-id="c48cd-107">PR_DELIVERY_POINT</span></span>  <br/> |
|<span data-ttu-id="c48cd-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c48cd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c48cd-109">0x0C07</span><span class="sxs-lookup"><span data-stu-id="c48cd-109">0x0C07</span></span>  <br/> |
|<span data-ttu-id="c48cd-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c48cd-110">Data type:</span></span>  <br/> |<span data-ttu-id="c48cd-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c48cd-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c48cd-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c48cd-112">Area:</span></span>  <br/> |<span data-ttu-id="c48cd-113">Destinatario MAPI</span><span class="sxs-lookup"><span data-stu-id="c48cd-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c48cd-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c48cd-114">Remarks</span></span>

<span data-ttu-id="c48cd-115">Esta propiedad puede tener exactamente uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="c48cd-115">This property can have exactly one of the following values:</span></span> 
  
<span data-ttu-id="c48cd-116">MAPI_MH_DP_ML</span><span class="sxs-lookup"><span data-stu-id="c48cd-116">MAPI_MH_DP_ML</span></span> 
  
> <span data-ttu-id="c48cd-117">Entrega a una lista de distribución, una entrega punto que a su vez puede distribuir el mensaje a muchos destinatarios.</span><span class="sxs-lookup"><span data-stu-id="c48cd-117">Delivered to a distribution list, a delivery point which in turn may distribute the message to many recipients.</span></span>
    
<span data-ttu-id="c48cd-118">MAPI_MH_DP_MS</span><span class="sxs-lookup"><span data-stu-id="c48cd-118">MAPI_MH_DP_MS</span></span> 
  
> <span data-ttu-id="c48cd-119">Entrega a un almacén de mensajes en lugar de hacerlo directamente a un destinatario.</span><span class="sxs-lookup"><span data-stu-id="c48cd-119">Delivered to a message store instead of directly to a recipient.</span></span>
    
<span data-ttu-id="c48cd-120">MAPI_MH_DP_OTHER_AU</span><span class="sxs-lookup"><span data-stu-id="c48cd-120">MAPI_MH_DP_OTHER_AU</span></span> 
  
> <span data-ttu-id="c48cd-121">Entrega a una unidad de acceso (AU) que no sea una unidad de acceso de entrega física (PDAU), como un sistema de FAX.</span><span class="sxs-lookup"><span data-stu-id="c48cd-121">Delivered to an access unit (AU) other than a physical delivery access unit (PDAU), such as a FAX system.</span></span>
    
<span data-ttu-id="c48cd-122">MAPI_MH_DP_PDAU</span><span class="sxs-lookup"><span data-stu-id="c48cd-122">MAPI_MH_DP_PDAU</span></span> 
  
> <span data-ttu-id="c48cd-123">Entrega a una unidad de acceso de entrega física, como un operador postal humana.</span><span class="sxs-lookup"><span data-stu-id="c48cd-123">Delivered to a physical delivery access unit, such as a human postal carrier.</span></span>
    
<span data-ttu-id="c48cd-124">MAPI_MH_DP_PDS_PATRON</span><span class="sxs-lookup"><span data-stu-id="c48cd-124">MAPI_MH_DP_PDS_PATRON</span></span> 
  
> <span data-ttu-id="c48cd-125">Entrega a un usuario del sistema físico de entrega, como un buzón de correo postal convencional.</span><span class="sxs-lookup"><span data-stu-id="c48cd-125">Delivered to a physical delivery system patron, such as a conventional postal mailbox.</span></span>
    
<span data-ttu-id="c48cd-126">MAPI_MH_DP_PRIVATE_UA</span><span class="sxs-lookup"><span data-stu-id="c48cd-126">MAPI_MH_DP_PRIVATE_UA</span></span> 
  
> <span data-ttu-id="c48cd-127">Entrega a un agente de usuario privada (UA), como un cliente en un sistema de mensajería interno.</span><span class="sxs-lookup"><span data-stu-id="c48cd-127">Delivered to a private user agent (UA), such as a client in an in-house messaging system.</span></span>
    
<span data-ttu-id="c48cd-128">MAPI_MH_DP_PUBLIC_UA</span><span class="sxs-lookup"><span data-stu-id="c48cd-128">MAPI_MH_DP_PUBLIC_UA</span></span> 
  
> <span data-ttu-id="c48cd-129">Entregar a un agente de usuario público o proveedor de servicios públicos.</span><span class="sxs-lookup"><span data-stu-id="c48cd-129">Delivered to a public user agent, or public service provider.</span></span>
    
<span data-ttu-id="c48cd-130">El valor predeterminado es MAPI_MH_DP_PRIVATE_UA, es decir, un cliente MAPI.</span><span class="sxs-lookup"><span data-stu-id="c48cd-130">The default value is MAPI_MH_DP_PRIVATE_UA, that is, a MAPI client.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c48cd-131">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c48cd-131">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c48cd-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c48cd-132">Header files</span></span>

<span data-ttu-id="c48cd-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c48cd-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="c48cd-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c48cd-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="c48cd-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c48cd-135">Mapitags.h</span></span>
  
> <span data-ttu-id="c48cd-136">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="c48cd-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c48cd-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="c48cd-137">See also</span></span>



[<span data-ttu-id="c48cd-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c48cd-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c48cd-139">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c48cd-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c48cd-140">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c48cd-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c48cd-141">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c48cd-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

