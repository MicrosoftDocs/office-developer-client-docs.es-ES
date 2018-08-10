---
title: Propiedad canónica PidTagImportance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9f6a67dcff6c74f44bbc64ae8b95f3e0ec284a90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819606"
---
# <a name="pidtagimportance-canonical-property"></a><span data-ttu-id="9e505-103">Propiedad canónica PidTagImportance</span><span class="sxs-lookup"><span data-stu-id="9e505-103">PidTagImportance Canonical Property</span></span>

  
  
<span data-ttu-id="9e505-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9e505-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9e505-105">Contiene un valor que indica la opinión de la dirección del remitente del mensaje de la importancia de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="9e505-105">Contains a value that indicates the message sender's opinion of the importance of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e505-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9e505-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9e505-107">PR_IMPORTANCE</span><span class="sxs-lookup"><span data-stu-id="9e505-107">PR_IMPORTANCE</span></span>  <br/> |
|<span data-ttu-id="9e505-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9e505-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9e505-109">0x0017</span><span class="sxs-lookup"><span data-stu-id="9e505-109">0x0017</span></span>  <br/> |
|<span data-ttu-id="9e505-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9e505-110">Data type:</span></span>  <br/> |<span data-ttu-id="9e505-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9e505-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9e505-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9e505-112">Area:</span></span>  <br/> |<span data-ttu-id="9e505-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="9e505-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e505-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9e505-114">Remarks</span></span>

<span data-ttu-id="9e505-115">No se deben confundir esta propiedad y la propiedad **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9e505-115">This property and the **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="9e505-116">Importancia indica un valor a los usuarios, mientras que la prioridad indica el orden o la velocidad a la que se debe enviar el mensaje por el software del sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="9e505-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="9e505-117">Normalmente, una mayor prioridad indica un costo mayor.</span><span class="sxs-lookup"><span data-stu-id="9e505-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="9e505-118">Mayor importancia generalmente se asocia con una presentación diferentes mediante la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="9e505-118">Higher importance usually is associated with a different display by the user interface.</span></span> 
  
<span data-ttu-id="9e505-119">Esta propiedad puede tener exactamente uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="9e505-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="9e505-120">IMPORTANCE_LOW</span><span class="sxs-lookup"><span data-stu-id="9e505-120">IMPORTANCE_LOW</span></span> 
  
> <span data-ttu-id="9e505-121">El mensaje tiene importancia baja.</span><span class="sxs-lookup"><span data-stu-id="9e505-121">The message has low importance.</span></span>
    
<span data-ttu-id="9e505-122">IMPORTANCE_HIGH</span><span class="sxs-lookup"><span data-stu-id="9e505-122">IMPORTANCE_HIGH</span></span> 
  
> <span data-ttu-id="9e505-123">El mensaje tiene importancia alta.</span><span class="sxs-lookup"><span data-stu-id="9e505-123">The message has high importance.</span></span>
    
<span data-ttu-id="9e505-124">IMPORTANCE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="9e505-124">IMPORTANCE_NORMAL</span></span> 
  
> <span data-ttu-id="9e505-125">El mensaje tiene importancia normal.</span><span class="sxs-lookup"><span data-stu-id="9e505-125">The message has normal importance.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="9e505-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9e505-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9e505-127">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="9e505-127">Protocol specifications</span></span>

<span data-ttu-id="9e505-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e505-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e505-129">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9e505-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9e505-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e505-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e505-131">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="9e505-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9e505-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9e505-132">Header files</span></span>

<span data-ttu-id="9e505-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9e505-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="9e505-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9e505-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="9e505-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9e505-135">Mapitags.h</span></span>
  
> <span data-ttu-id="9e505-136">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="9e505-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9e505-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e505-137">See also</span></span>



[<span data-ttu-id="9e505-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9e505-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9e505-139">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="9e505-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9e505-140">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9e505-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9e505-141">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="9e505-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
