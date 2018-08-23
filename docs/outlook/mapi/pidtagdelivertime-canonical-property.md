---
title: Propiedad canónica PidTagDeliverTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliverTime
api_type:
- HeaderDef
ms.assetid: da0ad17b-08ac-4c50-ac1d-13062b890dfd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 198e388f5cfb6ab0431e7b7a78b9a0be3d103597
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582122"
---
# <a name="pidtagdelivertime-canonical-property"></a><span data-ttu-id="1afaa-103">Propiedad canónica PidTagDeliverTime</span><span class="sxs-lookup"><span data-stu-id="1afaa-103">PidTagDeliverTime Canonical Property</span></span>

  
  
<span data-ttu-id="1afaa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1afaa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1afaa-105">Contiene la fecha y hora cuando se entregó el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="1afaa-105">Contains the date and time when the original message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1afaa-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1afaa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1afaa-107">PR_DELIVER_TIME</span><span class="sxs-lookup"><span data-stu-id="1afaa-107">PR_DELIVER_TIME</span></span>  <br/> |
|<span data-ttu-id="1afaa-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1afaa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1afaa-109">0x0010</span><span class="sxs-lookup"><span data-stu-id="1afaa-109">0x0010</span></span>  <br/> |
|<span data-ttu-id="1afaa-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1afaa-110">Data type:</span></span>  <br/> |<span data-ttu-id="1afaa-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="1afaa-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="1afaa-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1afaa-112">Area:</span></span>  <br/> |<span data-ttu-id="1afaa-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="1afaa-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1afaa-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1afaa-114">Remarks</span></span>

<span data-ttu-id="1afaa-115">Esta propiedad es una propiedad por destinatario en un informe de entrega que indica el tiempo que el mensaje original se entregó al usuario de mensajería para la que se está generando el informe de entrega.</span><span class="sxs-lookup"><span data-stu-id="1afaa-115">This property is a per-recipient property on a delivery report that indicates the time the original message was delivered to the messaging user for which the delivery report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1afaa-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1afaa-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1afaa-117">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1afaa-117">Header files</span></span>

<span data-ttu-id="1afaa-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1afaa-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="1afaa-119">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1afaa-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="1afaa-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1afaa-120">Mapitags.h</span></span>
  
> <span data-ttu-id="1afaa-121">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="1afaa-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1afaa-122">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="1afaa-122">See also</span></span>



[<span data-ttu-id="1afaa-123">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="1afaa-123">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)


[<span data-ttu-id="1afaa-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1afaa-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1afaa-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="1afaa-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1afaa-126">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1afaa-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1afaa-127">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="1afaa-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

