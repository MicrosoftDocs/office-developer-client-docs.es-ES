---
title: Propiedad canónica PidTagDeferredDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredDeliveryTime
api_type:
- HeaderDef
ms.assetid: 263ac923-692f-40d4-bdd5-116dc5c49766
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7197159fd55016454de3fa806fc30d0700ef5f3d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359930"
---
# <a name="pidtagdeferreddeliverytime-canonical-property"></a><span data-ttu-id="04af6-103">Propiedad canónica PidTagDeferredDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="04af6-103">PidTagDeferredDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="04af6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04af6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04af6-105">Contiene la fecha y la hora en que el remitente de un mensaje desea entregar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="04af6-105">Contains the date and time when a message sender wants a message delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="04af6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="04af6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="04af6-107">PR_DEFERRED_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="04af6-107">PR_DEFERRED_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="04af6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="04af6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="04af6-109">0x000F</span><span class="sxs-lookup"><span data-stu-id="04af6-109">0x000F</span></span>  <br/> |
|<span data-ttu-id="04af6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="04af6-110">Data type:</span></span>  <br/> |<span data-ttu-id="04af6-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="04af6-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="04af6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="04af6-112">Area:</span></span>  <br/> |<span data-ttu-id="04af6-113">Sobre MAPI</span><span class="sxs-lookup"><span data-stu-id="04af6-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04af6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="04af6-114">Remarks</span></span>

<span data-ttu-id="04af6-115">MAPI no realiza la entrega diferida; se trata de una opción del sistema de mensajería subyacente para controlar la entrega diferida.</span><span class="sxs-lookup"><span data-stu-id="04af6-115">MAPI does not perform the deferred delivery; it is an option of the underlying messaging system to handle deferred delivery.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="04af6-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="04af6-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="04af6-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="04af6-117">Protocol specifications</span></span>

<span data-ttu-id="04af6-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04af6-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04af6-119">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="04af6-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="04af6-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04af6-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04af6-121">Especifica las propiedades y operaciones que se admiten en los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="04af6-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="04af6-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="04af6-122">Header files</span></span>

<span data-ttu-id="04af6-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="04af6-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="04af6-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="04af6-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="04af6-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="04af6-125">Mapitags.h</span></span>
  
> <span data-ttu-id="04af6-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="04af6-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="04af6-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="04af6-127">See also</span></span>



[<span data-ttu-id="04af6-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="04af6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="04af6-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="04af6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="04af6-130">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="04af6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="04af6-131">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="04af6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

