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
ms.openlocfilehash: 39840f27d67daca625daea08555ab89d5a362e63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819520"
---
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="61170-103">Propiedad canónica PidTagFollowupIcon</span><span class="sxs-lookup"><span data-stu-id="61170-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="61170-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="61170-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="61170-105">Especifica el color del indicador del objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="61170-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="61170-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="61170-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="61170-107">PR_FOLLOWUP_ICON</span><span class="sxs-lookup"><span data-stu-id="61170-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="61170-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="61170-108">Identifier:</span></span>  <br/> |<span data-ttu-id="61170-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="61170-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="61170-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="61170-110">Data type:</span></span>  <br/> |<span data-ttu-id="61170-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="61170-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="61170-112">Área:</span><span class="sxs-lookup"><span data-stu-id="61170-112">Area:</span></span>  <br/> |<span data-ttu-id="61170-113">Cambiar el nombre de la carpeta de mensajes</span><span class="sxs-lookup"><span data-stu-id="61170-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61170-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="61170-114">Remarks</span></span>

<span data-ttu-id="61170-115">Esta propiedad no debe existir a menos que el valor de la propiedad **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) se establece en "followupFlagged", o el objeto de mensaje es un objeto relacionado con la reunión.</span><span class="sxs-lookup"><span data-stu-id="61170-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="61170-116">Esta propiedad no debe existir en un objeto task.</span><span class="sxs-lookup"><span data-stu-id="61170-116">This property should not exist on a task object.</span></span> <span data-ttu-id="61170-117">Cuando se establece en otros objetos de mensaje, esta propiedad debe establecerse en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="61170-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="61170-118">**Valor numérico**</span><span class="sxs-lookup"><span data-stu-id="61170-118">**Numeric value**</span></span>|<span data-ttu-id="61170-119">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="61170-119">**Name**</span></span>|<span data-ttu-id="61170-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="61170-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="61170-121">No está presente</span><span class="sxs-lookup"><span data-stu-id="61170-121">Not present</span></span>  <br/> |<span data-ttu-id="61170-122">N/D</span><span class="sxs-lookup"><span data-stu-id="61170-122">N/A</span></span>  <br/> |<span data-ttu-id="61170-123">Sin color</span><span class="sxs-lookup"><span data-stu-id="61170-123">No color</span></span>  <br/> |
|<span data-ttu-id="61170-124">1</span><span class="sxs-lookup"><span data-stu-id="61170-124">1</span></span>  <br/> |<span data-ttu-id="61170-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="61170-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="61170-126">Marca púrpura</span><span class="sxs-lookup"><span data-stu-id="61170-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="61170-127">2</span><span class="sxs-lookup"><span data-stu-id="61170-127">2</span></span>  <br/> |<span data-ttu-id="61170-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="61170-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="61170-129">Marca naranja</span><span class="sxs-lookup"><span data-stu-id="61170-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="61170-130">3</span><span class="sxs-lookup"><span data-stu-id="61170-130">3</span></span>  <br/> |<span data-ttu-id="61170-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="61170-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="61170-132">Marca verde</span><span class="sxs-lookup"><span data-stu-id="61170-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="61170-133">4</span><span class="sxs-lookup"><span data-stu-id="61170-133">4</span></span>  <br/> |<span data-ttu-id="61170-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="61170-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="61170-135">Marca amarilla</span><span class="sxs-lookup"><span data-stu-id="61170-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="61170-136">5</span><span class="sxs-lookup"><span data-stu-id="61170-136">5</span></span>  <br/> |<span data-ttu-id="61170-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="61170-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="61170-138">Marca azul</span><span class="sxs-lookup"><span data-stu-id="61170-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="61170-139">6</span><span class="sxs-lookup"><span data-stu-id="61170-139">6</span></span>  <br/> |<span data-ttu-id="61170-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="61170-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="61170-141">Marca roja</span><span class="sxs-lookup"><span data-stu-id="61170-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="61170-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="61170-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="61170-143">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="61170-143">Protocol specifications</span></span>

<span data-ttu-id="61170-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61170-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61170-145">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="61170-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="61170-146">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61170-146">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61170-147">Especifica las propiedades y las operaciones relacionadas con marcas.</span><span class="sxs-lookup"><span data-stu-id="61170-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="61170-148">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="61170-148">Header files</span></span>

<span data-ttu-id="61170-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="61170-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="61170-150">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="61170-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="61170-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="61170-151">Mapitags.h</span></span>
  
> <span data-ttu-id="61170-152">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="61170-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="61170-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="61170-153">See also</span></span>



[<span data-ttu-id="61170-154">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="61170-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="61170-155">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="61170-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="61170-156">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="61170-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="61170-157">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="61170-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

