---
title: Propiedad canónica PidTagFollowupIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFollowupIcon
api_type:
- HeaderDef
ms.assetid: 374cef41-141a-491b-8dd1-eaf1a2044204
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 205b6ddc2b65297d69a2223aab7b745b223ee553
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316285"
---
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="f9be6-103">Propiedad canónica PidTagFollowupIcon</span><span class="sxs-lookup"><span data-stu-id="f9be6-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="f9be6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9be6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9be6-105">Especifica el color de marca del objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="f9be6-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f9be6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f9be6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f9be6-107">PR_FOLLOWUP_ICON</span><span class="sxs-lookup"><span data-stu-id="f9be6-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="f9be6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f9be6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f9be6-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="f9be6-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="f9be6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f9be6-110">Data type:</span></span>  <br/> |<span data-ttu-id="f9be6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f9be6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f9be6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f9be6-112">Area:</span></span>  <br/> |<span data-ttu-id="f9be6-113">Cambiar el nombre de la carpeta del mensaje</span><span class="sxs-lookup"><span data-stu-id="f9be6-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9be6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f9be6-114">Remarks</span></span>

<span data-ttu-id="f9be6-115">Esta propiedad no debe existir a menos que el valor de la propiedad **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) esté establecido en "followupFlagged" o el objeto de mensaje sea un objeto relacionado con la reunión.</span><span class="sxs-lookup"><span data-stu-id="f9be6-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="f9be6-116">Esta propiedad no debe existir en un objeto de tarea.</span><span class="sxs-lookup"><span data-stu-id="f9be6-116">This property should not exist on a task object.</span></span> <span data-ttu-id="f9be6-117">Cuando se establece en otros objetos de mensaje, esta propiedad debe establecerse en uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="f9be6-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="f9be6-118">**Valor numérico**</span><span class="sxs-lookup"><span data-stu-id="f9be6-118">**Numeric value**</span></span>|<span data-ttu-id="f9be6-119">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="f9be6-119">**Name**</span></span>|<span data-ttu-id="f9be6-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f9be6-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f9be6-121">No presente</span><span class="sxs-lookup"><span data-stu-id="f9be6-121">Not present</span></span>  <br/> |<span data-ttu-id="f9be6-122">N/D</span><span class="sxs-lookup"><span data-stu-id="f9be6-122">N/A</span></span>  <br/> |<span data-ttu-id="f9be6-123">Sin color</span><span class="sxs-lookup"><span data-stu-id="f9be6-123">No color</span></span>  <br/> |
|<span data-ttu-id="f9be6-124">1 </span><span class="sxs-lookup"><span data-stu-id="f9be6-124">1</span></span>  <br/> |<span data-ttu-id="f9be6-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="f9be6-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="f9be6-126">Marca púrpura</span><span class="sxs-lookup"><span data-stu-id="f9be6-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="f9be6-127">2 </span><span class="sxs-lookup"><span data-stu-id="f9be6-127">2</span></span>  <br/> |<span data-ttu-id="f9be6-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="f9be6-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="f9be6-129">Marca naranja</span><span class="sxs-lookup"><span data-stu-id="f9be6-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="f9be6-130">3 </span><span class="sxs-lookup"><span data-stu-id="f9be6-130">3</span></span>  <br/> |<span data-ttu-id="f9be6-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="f9be6-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="f9be6-132">Marca verde</span><span class="sxs-lookup"><span data-stu-id="f9be6-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="f9be6-133">4 </span><span class="sxs-lookup"><span data-stu-id="f9be6-133">4</span></span>  <br/> |<span data-ttu-id="f9be6-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="f9be6-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="f9be6-135">Marca amarilla</span><span class="sxs-lookup"><span data-stu-id="f9be6-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="f9be6-136">5 </span><span class="sxs-lookup"><span data-stu-id="f9be6-136">5</span></span>  <br/> |<span data-ttu-id="f9be6-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="f9be6-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="f9be6-138">Marca azul</span><span class="sxs-lookup"><span data-stu-id="f9be6-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="f9be6-139">6 </span><span class="sxs-lookup"><span data-stu-id="f9be6-139">6</span></span>  <br/> |<span data-ttu-id="f9be6-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="f9be6-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="f9be6-141">Marca roja</span><span class="sxs-lookup"><span data-stu-id="f9be6-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f9be6-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9be6-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f9be6-143">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="f9be6-143">Protocol specifications</span></span>

<span data-ttu-id="f9be6-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f9be6-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f9be6-145">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="f9be6-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f9be6-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f9be6-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f9be6-147">Especifica las propiedades y operaciones relacionadas con la marcación.</span><span class="sxs-lookup"><span data-stu-id="f9be6-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f9be6-148">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f9be6-148">Header files</span></span>

<span data-ttu-id="f9be6-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f9be6-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="f9be6-150">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f9be6-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="f9be6-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f9be6-151">Mapitags.h</span></span>
  
> <span data-ttu-id="f9be6-152">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f9be6-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f9be6-153">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f9be6-153">See also</span></span>



[<span data-ttu-id="f9be6-154">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f9be6-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f9be6-155">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="f9be6-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f9be6-156">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f9be6-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f9be6-157">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="f9be6-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

