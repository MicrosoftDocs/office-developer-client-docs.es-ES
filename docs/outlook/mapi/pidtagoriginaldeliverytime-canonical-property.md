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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391377"
---
# <a name="pidtagoriginaldeliverytime-canonical-property"></a><span data-ttu-id="419fc-103">Propiedad canónica PidTagOriginalDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="419fc-103">PidTagOriginalDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="419fc-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="419fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="419fc-105">Contiene una copia de la fecha de entrega y el tiempo en un subproceso del mensaje original.</span><span class="sxs-lookup"><span data-stu-id="419fc-105">Contains a copy of the original message's delivery date and time in a thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="419fc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="419fc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="419fc-107">PR_ORIGINAL_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="419fc-107">PR_ORIGINAL_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="419fc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="419fc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="419fc-109">0x0055</span><span class="sxs-lookup"><span data-stu-id="419fc-109">0x0055</span></span>  <br/> |
|<span data-ttu-id="419fc-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="419fc-110">Data type:</span></span>  <br/> |<span data-ttu-id="419fc-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="419fc-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="419fc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="419fc-112">Area:</span></span>  <br/> |<span data-ttu-id="419fc-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="419fc-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="419fc-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="419fc-114">Remarks</span></span>

<span data-ttu-id="419fc-115">Esta propiedad se copió desde la propiedad **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) original en posterior responder o reenviar operaciones y usada en los informes de lectura y nonread.</span><span class="sxs-lookup"><span data-stu-id="419fc-115">This property is copied from the original **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property in subsequent reply or forward operations and used in read and nonread reports.</span></span> <span data-ttu-id="419fc-116">Informes de entrega su lugar, use la propiedad **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="419fc-116">Delivery reports use the **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) property instead.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="419fc-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="419fc-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="419fc-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="419fc-118">Protocol specifications</span></span>

<span data-ttu-id="419fc-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="419fc-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="419fc-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="419fc-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="419fc-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="419fc-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="419fc-122">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="419fc-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="419fc-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="419fc-123">Header files</span></span>

<span data-ttu-id="419fc-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="419fc-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="419fc-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="419fc-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="419fc-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="419fc-126">Mapitags.h</span></span>
  
> <span data-ttu-id="419fc-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="419fc-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="419fc-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="419fc-128">See also</span></span>



[<span data-ttu-id="419fc-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="419fc-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="419fc-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="419fc-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="419fc-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="419fc-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="419fc-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="419fc-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

