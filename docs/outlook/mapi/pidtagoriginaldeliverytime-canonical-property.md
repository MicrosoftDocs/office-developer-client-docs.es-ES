---
title: Propiedad canónica PidTagOriginalDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDeliveryTime
api_type:
- COM
ms.assetid: 700ccfc9-493a-483b-aca0-aa2d7f6bb229
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bbe277092b450a4254e02d00d2cf54e35ec6be44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355660"
---
# <a name="pidtagoriginaldeliverytime-canonical-property"></a><span data-ttu-id="8c554-103">Propiedad canónica PidTagOriginalDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="8c554-103">PidTagOriginalDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="8c554-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c554-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c554-105">Contiene una copia de la fecha y hora de entrega del mensaje original en un hilo.</span><span class="sxs-lookup"><span data-stu-id="8c554-105">Contains a copy of the original message's delivery date and time in a thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c554-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8c554-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8c554-107">PR_ORIGINAL_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="8c554-107">PR_ORIGINAL_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="8c554-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8c554-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8c554-109">0x0055</span><span class="sxs-lookup"><span data-stu-id="8c554-109">0x0055</span></span>  <br/> |
|<span data-ttu-id="8c554-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8c554-110">Data type:</span></span>  <br/> |<span data-ttu-id="8c554-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="8c554-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="8c554-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8c554-112">Area:</span></span>  <br/> |<span data-ttu-id="8c554-113">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="8c554-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c554-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8c554-114">Remarks</span></span>

<span data-ttu-id="8c554-115">Esta propiedad se copia de la propiedad **PR_MESSAGE_DELIVERY_TIME** original ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) en operaciones de respuesta o reenvío posteriores y se usa en informes leídos y no leídos.</span><span class="sxs-lookup"><span data-stu-id="8c554-115">This property is copied from the original **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property in subsequent reply or forward operations and used in read and nonread reports.</span></span> <span data-ttu-id="8c554-116">Los informes de entrega **usan PR_DELIVER_TIME** propiedad ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="8c554-116">Delivery reports use the **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) property instead.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8c554-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8c554-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8c554-118">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="8c554-118">Protocol specifications</span></span>

<span data-ttu-id="8c554-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c554-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c554-120">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="8c554-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8c554-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c554-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c554-122">Especifica las propiedades y operaciones permitidas en los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="8c554-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8c554-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8c554-123">Header files</span></span>

<span data-ttu-id="8c554-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8c554-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="8c554-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8c554-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="8c554-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8c554-126">Mapitags.h</span></span>
  
> <span data-ttu-id="8c554-127">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="8c554-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8c554-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8c554-128">See also</span></span>



[<span data-ttu-id="8c554-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8c554-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8c554-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="8c554-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8c554-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8c554-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8c554-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="8c554-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

