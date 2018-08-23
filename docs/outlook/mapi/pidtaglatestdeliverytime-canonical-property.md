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
ms.openlocfilehash: 3640ec4471b72dea81d56cc2c462ef145095480f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590928"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a><span data-ttu-id="35884-103">Propiedad canónica PidTagLatestDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="35884-103">PidTagLatestDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="35884-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35884-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35884-105">Contiene la última fecha y hora cuando un agente de transferencia de mensajes (MTA) debe entregar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="35884-105">Contains the latest date and time when a message transfer agent (MTA) should deliver a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="35884-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="35884-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="35884-107">PR_LATEST_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="35884-107">PR_LATEST_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="35884-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="35884-108">Identifier:</span></span>  <br/> |<span data-ttu-id="35884-109">0x0019</span><span class="sxs-lookup"><span data-stu-id="35884-109">0x0019</span></span>  <br/> |
|<span data-ttu-id="35884-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="35884-110">Data type:</span></span>  <br/> |<span data-ttu-id="35884-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="35884-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="35884-112">Área:</span><span class="sxs-lookup"><span data-stu-id="35884-112">Area:</span></span>  <br/> |<span data-ttu-id="35884-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="35884-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35884-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="35884-114">Remarks</span></span>

<span data-ttu-id="35884-115">Si un MTA no puede entregar un mensaje por el tiempo que especifica esta propiedad, cancela el mensaje sin entrega.</span><span class="sxs-lookup"><span data-stu-id="35884-115">If an MTA cannot deliver a message by the time this property specifies, it cancels the message without delivery.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="35884-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="35884-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="35884-117">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="35884-117">Header files</span></span>

<span data-ttu-id="35884-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35884-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="35884-119">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="35884-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="35884-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="35884-120">Mapitags.h</span></span>
  
> <span data-ttu-id="35884-121">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="35884-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35884-122">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="35884-122">See also</span></span>



[<span data-ttu-id="35884-123">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="35884-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="35884-124">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="35884-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="35884-125">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="35884-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="35884-126">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="35884-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

