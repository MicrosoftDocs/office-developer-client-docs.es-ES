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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383523"
---
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="81d0e-103">Propiedad canónica PidTagFollowupIcon</span><span class="sxs-lookup"><span data-stu-id="81d0e-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="81d0e-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81d0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81d0e-105">Especifica el color del indicador del objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="81d0e-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="81d0e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="81d0e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="81d0e-107">PR_FOLLOWUP_ICON</span><span class="sxs-lookup"><span data-stu-id="81d0e-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="81d0e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="81d0e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="81d0e-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="81d0e-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="81d0e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="81d0e-110">Data type:</span></span>  <br/> |<span data-ttu-id="81d0e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="81d0e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="81d0e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="81d0e-112">Area:</span></span>  <br/> |<span data-ttu-id="81d0e-113">Cambiar el nombre de la carpeta de mensajes</span><span class="sxs-lookup"><span data-stu-id="81d0e-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81d0e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="81d0e-114">Remarks</span></span>

<span data-ttu-id="81d0e-115">Esta propiedad no debe existir a menos que el valor de la propiedad **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) se establece en "followupFlagged", o el objeto de mensaje es un objeto relacionado con la reunión.</span><span class="sxs-lookup"><span data-stu-id="81d0e-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="81d0e-116">Esta propiedad no debe existir en un objeto task.</span><span class="sxs-lookup"><span data-stu-id="81d0e-116">This property should not exist on a task object.</span></span> <span data-ttu-id="81d0e-117">Cuando se establece en otros objetos de mensaje, esta propiedad debe establecerse en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="81d0e-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="81d0e-118">**Valor numérico**</span><span class="sxs-lookup"><span data-stu-id="81d0e-118">**Numeric value**</span></span>|<span data-ttu-id="81d0e-119">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="81d0e-119">**Name**</span></span>|<span data-ttu-id="81d0e-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="81d0e-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="81d0e-121">No está presente</span><span class="sxs-lookup"><span data-stu-id="81d0e-121">Not present</span></span>  <br/> |<span data-ttu-id="81d0e-122">N/D</span><span class="sxs-lookup"><span data-stu-id="81d0e-122">N/A</span></span>  <br/> |<span data-ttu-id="81d0e-123">Sin color</span><span class="sxs-lookup"><span data-stu-id="81d0e-123">No color</span></span>  <br/> |
|<span data-ttu-id="81d0e-124">1</span><span class="sxs-lookup"><span data-stu-id="81d0e-124">1</span></span>  <br/> |<span data-ttu-id="81d0e-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="81d0e-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="81d0e-126">Marca púrpura</span><span class="sxs-lookup"><span data-stu-id="81d0e-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="81d0e-127">2</span><span class="sxs-lookup"><span data-stu-id="81d0e-127">2</span></span>  <br/> |<span data-ttu-id="81d0e-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="81d0e-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="81d0e-129">Marca naranja</span><span class="sxs-lookup"><span data-stu-id="81d0e-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="81d0e-130">3</span><span class="sxs-lookup"><span data-stu-id="81d0e-130">3</span></span>  <br/> |<span data-ttu-id="81d0e-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="81d0e-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="81d0e-132">Marca verde</span><span class="sxs-lookup"><span data-stu-id="81d0e-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="81d0e-133">4</span><span class="sxs-lookup"><span data-stu-id="81d0e-133">4</span></span>  <br/> |<span data-ttu-id="81d0e-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="81d0e-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="81d0e-135">Marca amarilla</span><span class="sxs-lookup"><span data-stu-id="81d0e-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="81d0e-136">5</span><span class="sxs-lookup"><span data-stu-id="81d0e-136">5</span></span>  <br/> |<span data-ttu-id="81d0e-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="81d0e-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="81d0e-138">Marca azul</span><span class="sxs-lookup"><span data-stu-id="81d0e-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="81d0e-139">6</span><span class="sxs-lookup"><span data-stu-id="81d0e-139">6</span></span>  <br/> |<span data-ttu-id="81d0e-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="81d0e-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="81d0e-141">Marca roja</span><span class="sxs-lookup"><span data-stu-id="81d0e-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="81d0e-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="81d0e-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="81d0e-143">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="81d0e-143">Protocol specifications</span></span>

<span data-ttu-id="81d0e-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81d0e-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81d0e-145">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="81d0e-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="81d0e-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81d0e-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81d0e-147">Especifica las propiedades y las operaciones relacionadas con marcas.</span><span class="sxs-lookup"><span data-stu-id="81d0e-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="81d0e-148">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="81d0e-148">Header files</span></span>

<span data-ttu-id="81d0e-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="81d0e-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="81d0e-150">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="81d0e-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="81d0e-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="81d0e-151">Mapitags.h</span></span>
  
> <span data-ttu-id="81d0e-152">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="81d0e-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81d0e-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="81d0e-153">See also</span></span>



[<span data-ttu-id="81d0e-154">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="81d0e-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="81d0e-155">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="81d0e-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="81d0e-156">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="81d0e-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="81d0e-157">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="81d0e-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

