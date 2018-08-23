---
title: Propiedad canónica PidTagDeferredSendNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendNumber
api_type:
- HeaderDef
ms.assetid: 8ada5c9b-bec5-42d8-bc58-f0411ec4e88b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 30ee7c1a7eb86fd4cdfe90fb6711bd1b295fd5e6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591089"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a><span data-ttu-id="2cc9d-103">Propiedad canónica PidTagDeferredSendNumber</span><span class="sxs-lookup"><span data-stu-id="2cc9d-103">PidTagDeferredSendNumber Canonical Property</span></span>

  
  
<span data-ttu-id="2cc9d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2cc9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2cc9d-105">Contiene un número que se puede usar para calcular el aplazamiento de enviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="2cc9d-105">Contains a number that can be used to compute the deferment of sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2cc9d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2cc9d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2cc9d-107">PR_DEFERRED_SEND_NUMBER</span><span class="sxs-lookup"><span data-stu-id="2cc9d-107">PR_DEFERRED_SEND_NUMBER</span></span>  <br/> |
|<span data-ttu-id="2cc9d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2cc9d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2cc9d-109">0x3FEB</span><span class="sxs-lookup"><span data-stu-id="2cc9d-109">0x3FEB</span></span>  <br/> |
|<span data-ttu-id="2cc9d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2cc9d-110">Data type:</span></span>  <br/> |<span data-ttu-id="2cc9d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2cc9d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2cc9d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2cc9d-112">Area:</span></span>  <br/> |<span data-ttu-id="2cc9d-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="2cc9d-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2cc9d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2cc9d-114">Remarks</span></span>

<span data-ttu-id="2cc9d-115">Esta propiedad se usa para los sistemas de la propiedad **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) cuando no está presente.</span><span class="sxs-lookup"><span data-stu-id="2cc9d-115">This property is used for computing the **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) property when it is not present.</span></span> <span data-ttu-id="2cc9d-116">Cuando se aplaza el envío de un mensaje, debe establecerse la propiedad **PR_DEFERRED_SEND_NUMBER** junto con la propiedad **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)), si la propiedad **PR_DEFERRED_SEND_TIME** está ausente.</span><span class="sxs-lookup"><span data-stu-id="2cc9d-116">When sending a message is deferred, the **PR_DEFERRED_SEND_NUMBER** property should be set along with the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) property, if the **PR_DEFERRED_SEND_TIME** property is absent.</span></span> 
  
<span data-ttu-id="2cc9d-117">El valor **PR_DEFERRED_SEND_NUMBER** debe establecerse entre 0 y 999.</span><span class="sxs-lookup"><span data-stu-id="2cc9d-117">The **PR_DEFERRED_SEND_NUMBER** value must be set between 0 and 999.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2cc9d-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2cc9d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2cc9d-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="2cc9d-119">Protocol specifications</span></span>

<span data-ttu-id="2cc9d-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2cc9d-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2cc9d-121">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="2cc9d-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2cc9d-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2cc9d-122">Header files</span></span>

<span data-ttu-id="2cc9d-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2cc9d-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="2cc9d-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2cc9d-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="2cc9d-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2cc9d-125">Mapitags.h</span></span>
  
> <span data-ttu-id="2cc9d-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="2cc9d-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2cc9d-127">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="2cc9d-127">See also</span></span>



[<span data-ttu-id="2cc9d-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2cc9d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2cc9d-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="2cc9d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2cc9d-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2cc9d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2cc9d-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="2cc9d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

