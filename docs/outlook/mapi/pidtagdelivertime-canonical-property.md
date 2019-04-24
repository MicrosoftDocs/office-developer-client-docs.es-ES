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
ms.openlocfilehash: 3e9318e396bf195ad701b92372a3136dee7fd0d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357725"
---
# <a name="pidtagdelivertime-canonical-property"></a><span data-ttu-id="d79c9-103">Propiedad canónica PidTagDeliverTime</span><span class="sxs-lookup"><span data-stu-id="d79c9-103">PidTagDeliverTime Canonical Property</span></span>

  
  
<span data-ttu-id="d79c9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d79c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d79c9-105">Contiene la fecha y la hora en que se entregó el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="d79c9-105">Contains the date and time when the original message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d79c9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d79c9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d79c9-107">PR_DELIVER_TIME</span><span class="sxs-lookup"><span data-stu-id="d79c9-107">PR_DELIVER_TIME</span></span>  <br/> |
|<span data-ttu-id="d79c9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d79c9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d79c9-109">0x0010</span><span class="sxs-lookup"><span data-stu-id="d79c9-109">0x0010</span></span>  <br/> |
|<span data-ttu-id="d79c9-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d79c9-110">Data type:</span></span>  <br/> |<span data-ttu-id="d79c9-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d79c9-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="d79c9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d79c9-112">Area:</span></span>  <br/> |<span data-ttu-id="d79c9-113">Sobre MAPI</span><span class="sxs-lookup"><span data-stu-id="d79c9-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d79c9-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d79c9-114">Remarks</span></span>

<span data-ttu-id="d79c9-115">Esta propiedad es una propiedad por destinatario en un informe de entrega que indica la hora en que se entregó el mensaje original al usuario de mensajería para el que se está generando el informe de entrega.</span><span class="sxs-lookup"><span data-stu-id="d79c9-115">This property is a per-recipient property on a delivery report that indicates the time the original message was delivered to the messaging user for which the delivery report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d79c9-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d79c9-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d79c9-117">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d79c9-117">Header files</span></span>

<span data-ttu-id="d79c9-118">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d79c9-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="d79c9-119">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d79c9-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="d79c9-120">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="d79c9-120">Mapitags.h</span></span>
  
> <span data-ttu-id="d79c9-121">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d79c9-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d79c9-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d79c9-122">See also</span></span>



[<span data-ttu-id="d79c9-123">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="d79c9-123">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)


[<span data-ttu-id="d79c9-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d79c9-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d79c9-125">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="d79c9-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d79c9-126">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d79c9-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d79c9-127">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="d79c9-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

