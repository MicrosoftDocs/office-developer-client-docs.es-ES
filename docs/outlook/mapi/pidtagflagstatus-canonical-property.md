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
ms.openlocfilehash: bca8fccaa43bb3157b3d4e2af7d6aafa64972b41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316299"
---
# <a name="pidtagflagstatus-canonical-property"></a><span data-ttu-id="59fea-103">Propiedad canónica PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="59fea-103">PidTagFlagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="59fea-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59fea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59fea-105">Especifica el estado de marca del objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="59fea-105">Specifies the flag state of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="59fea-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="59fea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="59fea-107">PR_FLAG_STATUS</span><span class="sxs-lookup"><span data-stu-id="59fea-107">PR_FLAG_STATUS</span></span>  <br/> |
|<span data-ttu-id="59fea-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="59fea-108">Identifier:</span></span>  <br/> |<span data-ttu-id="59fea-109">0x1090</span><span class="sxs-lookup"><span data-stu-id="59fea-109">0x1090</span></span>  <br/> |
|<span data-ttu-id="59fea-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="59fea-110">Data type:</span></span>  <br/> |<span data-ttu-id="59fea-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="59fea-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="59fea-112">Área:</span><span class="sxs-lookup"><span data-stu-id="59fea-112">Area:</span></span>  <br/> |<span data-ttu-id="59fea-113">Varios</span><span class="sxs-lookup"><span data-stu-id="59fea-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59fea-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="59fea-114">Remarks</span></span>

<span data-ttu-id="59fea-115">Esta propiedad no debe existir en un objeto relacionado con la reunión y no debe existir en un objeto de tarea.</span><span class="sxs-lookup"><span data-stu-id="59fea-115">This property must not exist on a meeting-related object, and it should not exist on a task object.</span></span> <span data-ttu-id="59fea-116">Cuando se establece en otros objetos de mensaje, esta propiedad debe establecerse en uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="59fea-116">When set on other message objects, this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="59fea-117">**Valor numérico**</span><span class="sxs-lookup"><span data-stu-id="59fea-117">**Numeric value**</span></span>|<span data-ttu-id="59fea-118">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="59fea-118">**Name**</span></span>|<span data-ttu-id="59fea-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="59fea-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="59fea-120">No presente</span><span class="sxs-lookup"><span data-stu-id="59fea-120">Not present</span></span>  <br/> |<span data-ttu-id="59fea-121">N/D</span><span class="sxs-lookup"><span data-stu-id="59fea-121">N/A</span></span>  <br/> |<span data-ttu-id="59fea-122">Sin inflar</span><span class="sxs-lookup"><span data-stu-id="59fea-122">Unflagged</span></span>  <br/> |
|<span data-ttu-id="59fea-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="59fea-123">0x00000001</span></span>  <br/> |<span data-ttu-id="59fea-124">followupComplete</span><span class="sxs-lookup"><span data-stu-id="59fea-124">followupComplete</span></span>  <br/> |<span data-ttu-id="59fea-125">Marcado completado</span><span class="sxs-lookup"><span data-stu-id="59fea-125">Flagged complete</span></span>  <br/> |
|<span data-ttu-id="59fea-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="59fea-126">0x00000002</span></span>  <br/> |<span data-ttu-id="59fea-127">followupFlagged</span><span class="sxs-lookup"><span data-stu-id="59fea-127">followupFlagged</span></span>  <br/> |<span data-ttu-id="59fea-128">Marcado</span><span class="sxs-lookup"><span data-stu-id="59fea-128">Flagged</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="59fea-129">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="59fea-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="59fea-130">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="59fea-130">Protocol specifications</span></span>

<span data-ttu-id="59fea-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="59fea-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="59fea-132">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="59fea-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="59fea-133">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="59fea-133">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="59fea-134">Especifica las propiedades y operaciones relacionadas con la marcación.</span><span class="sxs-lookup"><span data-stu-id="59fea-134">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="59fea-135">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="59fea-135">Header files</span></span>

<span data-ttu-id="59fea-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="59fea-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="59fea-137">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="59fea-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="59fea-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="59fea-138">Mapitags.h</span></span>
  
> <span data-ttu-id="59fea-139">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="59fea-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="59fea-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="59fea-140">See also</span></span>



[<span data-ttu-id="59fea-141">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="59fea-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="59fea-142">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="59fea-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="59fea-143">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="59fea-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="59fea-144">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="59fea-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

