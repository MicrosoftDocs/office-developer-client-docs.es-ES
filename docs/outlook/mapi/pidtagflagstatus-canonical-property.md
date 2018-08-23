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
ms.openlocfilehash: 8dba5906a00beb6d38e4f3e375a9c57db79d42f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575962"
---
# <a name="pidtagflagstatus-canonical-property"></a><span data-ttu-id="0b04c-103">Propiedad canónica PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="0b04c-103">PidTagFlagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="0b04c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b04c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b04c-105">Especifica el estado de marca del objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="0b04c-105">Specifies the flag state of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0b04c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0b04c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0b04c-107">PR_FLAG_STATUS</span><span class="sxs-lookup"><span data-stu-id="0b04c-107">PR_FLAG_STATUS</span></span>  <br/> |
|<span data-ttu-id="0b04c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0b04c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0b04c-109">0x1090</span><span class="sxs-lookup"><span data-stu-id="0b04c-109">0x1090</span></span>  <br/> |
|<span data-ttu-id="0b04c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0b04c-110">Data type:</span></span>  <br/> |<span data-ttu-id="0b04c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0b04c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0b04c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0b04c-112">Area:</span></span>  <br/> |<span data-ttu-id="0b04c-113">Varios</span><span class="sxs-lookup"><span data-stu-id="0b04c-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b04c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0b04c-114">Remarks</span></span>

<span data-ttu-id="0b04c-115">Esta propiedad no debe existir en un objeto relacionado con la reunión y no debe existir en un objeto task.</span><span class="sxs-lookup"><span data-stu-id="0b04c-115">This property must not exist on a meeting-related object, and it should not exist on a task object.</span></span> <span data-ttu-id="0b04c-116">Cuando se establece en otros objetos de mensaje, esta propiedad debe establecerse en uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="0b04c-116">When set on other message objects, this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="0b04c-117">**Valor numérico**</span><span class="sxs-lookup"><span data-stu-id="0b04c-117">**Numeric value**</span></span>|<span data-ttu-id="0b04c-118">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="0b04c-118">**Name**</span></span>|<span data-ttu-id="0b04c-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0b04c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0b04c-120">No está presente</span><span class="sxs-lookup"><span data-stu-id="0b04c-120">Not present</span></span>  <br/> |<span data-ttu-id="0b04c-121">N/D</span><span class="sxs-lookup"><span data-stu-id="0b04c-121">N/A</span></span>  <br/> |<span data-ttu-id="0b04c-122">Sin marca</span><span class="sxs-lookup"><span data-stu-id="0b04c-122">Unflagged</span></span>  <br/> |
|<span data-ttu-id="0b04c-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0b04c-123">0x00000001</span></span>  <br/> |<span data-ttu-id="0b04c-124">followupComplete</span><span class="sxs-lookup"><span data-stu-id="0b04c-124">followupComplete</span></span>  <br/> |<span data-ttu-id="0b04c-125">Marcar como completado</span><span class="sxs-lookup"><span data-stu-id="0b04c-125">Flagged complete</span></span>  <br/> |
|<span data-ttu-id="0b04c-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="0b04c-126">0x00000002</span></span>  <br/> |<span data-ttu-id="0b04c-127">followupFlagged</span><span class="sxs-lookup"><span data-stu-id="0b04c-127">followupFlagged</span></span>  <br/> |<span data-ttu-id="0b04c-128">Marca</span><span class="sxs-lookup"><span data-stu-id="0b04c-128">Flagged</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0b04c-129">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0b04c-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0b04c-130">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0b04c-130">Protocol specifications</span></span>

<span data-ttu-id="0b04c-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b04c-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b04c-132">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0b04c-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0b04c-133">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b04c-133">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b04c-134">Especifica las propiedades y las operaciones relacionadas con marcas.</span><span class="sxs-lookup"><span data-stu-id="0b04c-134">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0b04c-135">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0b04c-135">Header files</span></span>

<span data-ttu-id="0b04c-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0b04c-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="0b04c-137">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0b04c-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="0b04c-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0b04c-138">Mapitags.h</span></span>
  
> <span data-ttu-id="0b04c-139">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0b04c-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b04c-140">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="0b04c-140">See also</span></span>



[<span data-ttu-id="0b04c-141">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0b04c-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0b04c-142">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="0b04c-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0b04c-143">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0b04c-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0b04c-144">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="0b04c-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

