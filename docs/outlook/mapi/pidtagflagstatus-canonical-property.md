---
title: Propiedad canónica PidTagFlagStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagStatus
api_type:
- HeaderDef
ms.assetid: b5117360-0939-4535-83fe-3b4a240b5217
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 38df67757082bd12e008e56632ec7e6961ba9d42
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819501"
---
# <a name="pidtagflagstatus-canonical-property"></a><span data-ttu-id="c7d9d-103">Propiedad canónica PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="c7d9d-103">PidTagFlagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="c7d9d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c7d9d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c7d9d-105">Especifica el estado de marca del objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="c7d9d-105">Specifies the flag state of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c7d9d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c7d9d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c7d9d-107">PR_FLAG_STATUS</span><span class="sxs-lookup"><span data-stu-id="c7d9d-107">PR_FLAG_STATUS</span></span>  <br/> |
|<span data-ttu-id="c7d9d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c7d9d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c7d9d-109">0x1090</span><span class="sxs-lookup"><span data-stu-id="c7d9d-109">0x1090</span></span>  <br/> |
|<span data-ttu-id="c7d9d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c7d9d-110">Data type:</span></span>  <br/> |<span data-ttu-id="c7d9d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c7d9d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c7d9d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c7d9d-112">Area:</span></span>  <br/> |<span data-ttu-id="c7d9d-113">Varios</span><span class="sxs-lookup"><span data-stu-id="c7d9d-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7d9d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c7d9d-114">Remarks</span></span>

<span data-ttu-id="c7d9d-115">Esta propiedad no debe existir en un objeto relacionado con la reunión y no debe existir en un objeto task.</span><span class="sxs-lookup"><span data-stu-id="c7d9d-115">This property must not exist on a meeting-related object, and it should not exist on a task object.</span></span> <span data-ttu-id="c7d9d-116">Cuando se establece en otros objetos de mensaje, esta propiedad debe establecerse en uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="c7d9d-116">When set on other message objects, this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="c7d9d-117">**Valor numérico**</span><span class="sxs-lookup"><span data-stu-id="c7d9d-117">**Numeric value**</span></span>|<span data-ttu-id="c7d9d-118">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c7d9d-118">**Name**</span></span>|<span data-ttu-id="c7d9d-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c7d9d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c7d9d-120">No está presente</span><span class="sxs-lookup"><span data-stu-id="c7d9d-120">Not present</span></span>  <br/> |<span data-ttu-id="c7d9d-121">N/D</span><span class="sxs-lookup"><span data-stu-id="c7d9d-121">N/A</span></span>  <br/> |<span data-ttu-id="c7d9d-122">Sin marca</span><span class="sxs-lookup"><span data-stu-id="c7d9d-122">Unflagged</span></span>  <br/> |
|<span data-ttu-id="c7d9d-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c7d9d-123">0x00000001</span></span>  <br/> |<span data-ttu-id="c7d9d-124">followupComplete</span><span class="sxs-lookup"><span data-stu-id="c7d9d-124">followupComplete</span></span>  <br/> |<span data-ttu-id="c7d9d-125">Marcar como completado</span><span class="sxs-lookup"><span data-stu-id="c7d9d-125">Flagged complete</span></span>  <br/> |
|<span data-ttu-id="c7d9d-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c7d9d-126">0x00000002</span></span>  <br/> |<span data-ttu-id="c7d9d-127">followupFlagged</span><span class="sxs-lookup"><span data-stu-id="c7d9d-127">followupFlagged</span></span>  <br/> |<span data-ttu-id="c7d9d-128">Marca</span><span class="sxs-lookup"><span data-stu-id="c7d9d-128">Flagged</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c7d9d-129">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7d9d-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c7d9d-130">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c7d9d-130">Protocol specifications</span></span>

<span data-ttu-id="c7d9d-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7d9d-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7d9d-132">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c7d9d-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c7d9d-133">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7d9d-133">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7d9d-134">Especifica las propiedades y las operaciones relacionadas con marcas.</span><span class="sxs-lookup"><span data-stu-id="c7d9d-134">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c7d9d-135">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c7d9d-135">Header files</span></span>

<span data-ttu-id="c7d9d-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c7d9d-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="c7d9d-137">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c7d9d-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="c7d9d-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c7d9d-138">Mapitags.h</span></span>
  
> <span data-ttu-id="c7d9d-139">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c7d9d-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c7d9d-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7d9d-140">See also</span></span>



[<span data-ttu-id="c7d9d-141">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c7d9d-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c7d9d-142">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c7d9d-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c7d9d-143">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c7d9d-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c7d9d-144">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c7d9d-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

