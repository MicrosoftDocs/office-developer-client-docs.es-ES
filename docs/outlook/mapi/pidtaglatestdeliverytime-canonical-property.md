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
ms.openlocfilehash: 77ca51ae5a0e7e1d5a9be8f4ca05a1187fe71694
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407791"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a><span data-ttu-id="ad101-103">Propiedad canónica PidTagLatestDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="ad101-103">PidTagLatestDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="ad101-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad101-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad101-105">Contiene la fecha y hora más recientes en que un agente de transferencia de mensajes (MTA) debe entregar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="ad101-105">Contains the latest date and time when a message transfer agent (MTA) should deliver a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ad101-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ad101-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ad101-107">PR_LATEST_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="ad101-107">PR_LATEST_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="ad101-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ad101-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ad101-109">0x0019</span><span class="sxs-lookup"><span data-stu-id="ad101-109">0x0019</span></span>  <br/> |
|<span data-ttu-id="ad101-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ad101-110">Data type:</span></span>  <br/> |<span data-ttu-id="ad101-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ad101-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="ad101-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ad101-112">Area:</span></span>  <br/> |<span data-ttu-id="ad101-113">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="ad101-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad101-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ad101-114">Remarks</span></span>

<span data-ttu-id="ad101-115">Si un MTA no puede entregar un mensaje cuando esta propiedad especifica, cancela el mensaje sin entrega.</span><span class="sxs-lookup"><span data-stu-id="ad101-115">If an MTA cannot deliver a message by the time this property specifies, it cancels the message without delivery.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ad101-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ad101-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ad101-117">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ad101-117">Header files</span></span>

<span data-ttu-id="ad101-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ad101-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="ad101-119">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ad101-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="ad101-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ad101-120">Mapitags.h</span></span>
  
> <span data-ttu-id="ad101-121">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="ad101-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad101-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad101-122">See also</span></span>



[<span data-ttu-id="ad101-123">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ad101-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ad101-124">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ad101-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ad101-125">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ad101-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ad101-126">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="ad101-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

