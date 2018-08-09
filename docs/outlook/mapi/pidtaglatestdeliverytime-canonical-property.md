---
title: Propiedad canónica PidTagLatestDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLatestDeliveryTime
api_type:
- HeaderDef
ms.assetid: 6c2e64bc-786e-4867-a504-46f4d1214337
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0cf25dc5a1182d019ea183f2c0714925f220aeb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819687"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a><span data-ttu-id="8ed0d-103">Propiedad canónica PidTagLatestDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="8ed0d-103">PidTagLatestDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="8ed0d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8ed0d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8ed0d-105">Contiene la última fecha y hora cuando un agente de transferencia de mensajes (MTA) debe entregar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-105">Contains the latest date and time when a message transfer agent (MTA) should deliver a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8ed0d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8ed0d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8ed0d-107">PR_LATEST_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="8ed0d-107">PR_LATEST_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="8ed0d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8ed0d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8ed0d-109">0x0019</span><span class="sxs-lookup"><span data-stu-id="8ed0d-109">0x0019</span></span>  <br/> |
|<span data-ttu-id="8ed0d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8ed0d-110">Data type:</span></span>  <br/> |<span data-ttu-id="8ed0d-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="8ed0d-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="8ed0d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8ed0d-112">Area:</span></span>  <br/> |<span data-ttu-id="8ed0d-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="8ed0d-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ed0d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8ed0d-114">Remarks</span></span>

<span data-ttu-id="8ed0d-115">Si un MTA no puede entregar un mensaje por el tiempo que especifica esta propiedad, cancela el mensaje sin entrega.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-115">If an MTA cannot deliver a message by the time this property specifies, it cancels the message without delivery.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8ed0d-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ed0d-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8ed0d-117">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8ed0d-117">Header files</span></span>

<span data-ttu-id="8ed0d-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8ed0d-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="8ed0d-119">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="8ed0d-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8ed0d-120">Mapitags.h</span></span>
  
> <span data-ttu-id="8ed0d-121">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8ed0d-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ed0d-122">See also</span></span>



[<span data-ttu-id="8ed0d-123">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8ed0d-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8ed0d-124">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="8ed0d-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8ed0d-125">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8ed0d-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8ed0d-126">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="8ed0d-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

