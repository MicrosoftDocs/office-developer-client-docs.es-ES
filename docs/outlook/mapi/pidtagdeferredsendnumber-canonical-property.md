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
ms.openlocfilehash: f2ccd004415bcbd42b56b1269fbdb4622ef1f8c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819453"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a><span data-ttu-id="4ea2f-103">Propiedad canónica PidTagDeferredSendNumber</span><span class="sxs-lookup"><span data-stu-id="4ea2f-103">PidTagDeferredSendNumber Canonical Property</span></span>

  
  
<span data-ttu-id="4ea2f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4ea2f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4ea2f-105">Contiene un número que se puede usar para calcular el aplazamiento de enviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="4ea2f-105">Contains a number that can be used to compute the deferment of sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4ea2f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4ea2f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4ea2f-107">PR_DEFERRED_SEND_NUMBER</span><span class="sxs-lookup"><span data-stu-id="4ea2f-107">PR_DEFERRED_SEND_NUMBER</span></span>  <br/> |
|<span data-ttu-id="4ea2f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4ea2f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4ea2f-109">0x3FEB</span><span class="sxs-lookup"><span data-stu-id="4ea2f-109">0x3FEB</span></span>  <br/> |
|<span data-ttu-id="4ea2f-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4ea2f-110">Data type:</span></span>  <br/> |<span data-ttu-id="4ea2f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4ea2f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4ea2f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4ea2f-112">Area:</span></span>  <br/> |<span data-ttu-id="4ea2f-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="4ea2f-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ea2f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ea2f-114">Remarks</span></span>

<span data-ttu-id="4ea2f-115">Esta propiedad se usa para los sistemas de la propiedad **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) cuando no está presente.</span><span class="sxs-lookup"><span data-stu-id="4ea2f-115">This property is used for computing the **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) property when it is not present.</span></span> <span data-ttu-id="4ea2f-116">Cuando se aplaza el envío de un mensaje, debe establecerse la propiedad **PR_DEFERRED_SEND_NUMBER** junto con la propiedad **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)), si la propiedad **PR_DEFERRED_SEND_TIME** está ausente.</span><span class="sxs-lookup"><span data-stu-id="4ea2f-116">When sending a message is deferred, the **PR_DEFERRED_SEND_NUMBER** property should be set along with the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) property, if the **PR_DEFERRED_SEND_TIME** property is absent.</span></span> 
  
<span data-ttu-id="4ea2f-117">El valor **PR_DEFERRED_SEND_NUMBER** debe establecerse entre 0 y 999.</span><span class="sxs-lookup"><span data-stu-id="4ea2f-117">The **PR_DEFERRED_SEND_NUMBER** value must be set between 0 and 999.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4ea2f-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4ea2f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4ea2f-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="4ea2f-119">Protocol specifications</span></span>

<span data-ttu-id="4ea2f-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ea2f-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ea2f-121">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4ea2f-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4ea2f-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4ea2f-122">Header files</span></span>

<span data-ttu-id="4ea2f-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4ea2f-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="4ea2f-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4ea2f-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="4ea2f-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4ea2f-125">Mapitags.h</span></span>
  
> <span data-ttu-id="4ea2f-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="4ea2f-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4ea2f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ea2f-127">See also</span></span>



[<span data-ttu-id="4ea2f-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4ea2f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4ea2f-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="4ea2f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4ea2f-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4ea2f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4ea2f-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="4ea2f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

