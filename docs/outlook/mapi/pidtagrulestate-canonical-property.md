---
title: Propiedad canónica PidTagRuleState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleState
api_type:
- COM
ms.assetid: f62f3055-b855-4203-aa5c-6ba28b58c6f7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 519ee2b91275e4253845afa35a9a80470071966d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820182"
---
# <a name="pidtagrulestate-canonical-property"></a><span data-ttu-id="d8a0c-103">Propiedad canónica PidTagRuleState</span><span class="sxs-lookup"><span data-stu-id="d8a0c-103">PidTagRuleState Canonical Property</span></span>

  
  
<span data-ttu-id="d8a0c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d8a0c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d8a0c-105">Un valor que se interpreta como una combinación de máscara de bits de marcadores que especifican el estado de la regla.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-105">A value interpreted as a bitmask combination of flags that specify the state of the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d8a0c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d8a0c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d8a0c-107">PR_RULE_STATE</span><span class="sxs-lookup"><span data-stu-id="d8a0c-107">PR_RULE_STATE</span></span>  <br/> |
|<span data-ttu-id="d8a0c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d8a0c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d8a0c-109">0x6677</span><span class="sxs-lookup"><span data-stu-id="d8a0c-109">0x6677</span></span>  <br/> |
|<span data-ttu-id="d8a0c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d8a0c-110">Data type:</span></span>  <br/> |<span data-ttu-id="d8a0c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d8a0c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d8a0c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d8a0c-112">Area:</span></span>  <br/> |<span data-ttu-id="d8a0c-113">Reglas del servidor</span><span class="sxs-lookup"><span data-stu-id="d8a0c-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8a0c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d8a0c-114">Remarks</span></span>

<span data-ttu-id="d8a0c-115">En la tabla siguiente define los valores posibles de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-115">The following table defines the possible values of this property.</span></span>
  
<span data-ttu-id="d8a0c-116">ES-es (ST_ENABLED, 0 x 00000001 de máscara de bits)</span><span class="sxs-lookup"><span data-stu-id="d8a0c-116">EN (ST_ENABLED, bitmask 0x00000001)</span></span>
  
> <span data-ttu-id="d8a0c-117">La regla está habilitada para la ejecución.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-117">The rule is enabled for execution.</span></span> <span data-ttu-id="d8a0c-118">Si no se establece este indicador, el servidor debe omitir esta regla al evaluar las reglas.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-118">If this flag is not set, the server must skip this rule when evaluating rules.</span></span>
    
<span data-ttu-id="d8a0c-119">Recuperación de emergencia (error, máscara de bits 0 x 00000002)</span><span class="sxs-lookup"><span data-stu-id="d8a0c-119">ER (ST_ERROR, bitmask 0x00000002)</span></span>
  
> <span data-ttu-id="d8a0c-120">El servidor ha encontrado un error al procesar la regla.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-120">The server has encountered an error processing the rule.</span></span>
    
<span data-ttu-id="d8a0c-121">DE (ST_ONLY_WHEN_OOF, máscara de bits 0 x 00000004)</span><span class="sxs-lookup"><span data-stu-id="d8a0c-121">OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)</span></span>
  
> <span data-ttu-id="d8a0c-122">La regla sólo se ejecuta cuando el usuario establece el estado de fuera de oficina (OOF) en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-122">The rule is executed only when the user sets the Out of Office (OOF) state on the mailbox.</span></span> <span data-ttu-id="d8a0c-123">Esta marca no se debe establecer en una regla de carpeta pública.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-123">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="d8a0c-124">ALTA (ST_KEEP_OOF_HIST, máscara de bits 0 x 00000008)</span><span class="sxs-lookup"><span data-stu-id="d8a0c-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span></span>
  
> <span data-ttu-id="d8a0c-125">Esta marca no se debe establecer en una regla de carpeta pública.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-125">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="d8a0c-126">EL (ST_EXIT_LEVEL, máscara de bits 0 x 00000010)</span><span class="sxs-lookup"><span data-stu-id="d8a0c-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span></span>
  
> <span data-ttu-id="d8a0c-127">Evaluación de la regla finalizará después de ejecutar esta regla, excepto para la evaluación de las reglas de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-127">Rule evaluation will end after executing this rule, except for evaluation of Out of Office rules.</span></span>
    
<span data-ttu-id="d8a0c-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, 0 x 00000020 de máscara de bits)</span><span class="sxs-lookup"><span data-stu-id="d8a0c-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span></span>
  
> <span data-ttu-id="d8a0c-129">Es posible que se omitió la evaluación de esta regla.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-129">Evaluation of this rule may be skipped.</span></span>
    
<span data-ttu-id="d8a0c-130">PE (ST_RULE_PARSE_ERROR, máscara de bits 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="d8a0c-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span></span>
  
> <span data-ttu-id="d8a0c-131">El servidor ha encontrado un error al analizar los datos de regla proporcionados por el cliente.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-131">The server has encountered an error parsing the rule data provided by the client.</span></span>
    
<span data-ttu-id="d8a0c-132">X</span><span class="sxs-lookup"><span data-stu-id="d8a0c-132">X</span></span>
  
> <span data-ttu-id="d8a0c-133">No se utiliza este protocolo.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-133">Unused by this protocol.</span></span> <span data-ttu-id="d8a0c-134">No se debe modificar este bit por el cliente.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-134">This bit must not be modified by the client.</span></span>
    
<span data-ttu-id="d8a0c-135">Tenga en cuenta sobre la interacción entre ST_ONLY_WHEN_OOF y ST_EXIT_LEVEL indicadores:</span><span class="sxs-lookup"><span data-stu-id="d8a0c-135">Note on the interaction between ST_ONLY_WHEN_OOF and ST_EXIT_LEVEL flags:</span></span> 
  
<span data-ttu-id="d8a0c-136">Cuando se establece el estado "fuera de la oficina" en el buzón de correo, y una condición de regla se evalúa como TRUE,</span><span class="sxs-lookup"><span data-stu-id="d8a0c-136">When the "Out of Office" state is set on the mailbox, and a rule condition evaluates to TRUE,</span></span> 
  
<span data-ttu-id="d8a0c-137">Y:</span><span class="sxs-lookup"><span data-stu-id="d8a0c-137">AND:</span></span>
  
- <span data-ttu-id="d8a0c-138">La regla tiene establecido el indicador ST_EXIT_LEVEL y no tiene marca ST_ONLY_WHEN_OOF.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-138">The rule has the ST_EXIT_LEVEL flag set and does not have ST_ONLY_WHEN_OOF flag set.</span></span> <span data-ttu-id="d8a0c-139">A continuación, el servidor no debe evaluar las reglas posteriores que no tienen ST_ONLY_WHEN_OOF marcador establecido y debe evaluar las reglas posteriores que tienen la marca ST_ONLY_WHEN_OOF establecida.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-139">Then, the server must not evaluate subsequent rules that do not have ST_ONLY_WHEN_OOF flag set, and must evaluate subsequent rules that have ST_ONLY_WHEN_OOF flag set.</span></span>
    
<span data-ttu-id="d8a0c-140">OR:</span><span class="sxs-lookup"><span data-stu-id="d8a0c-140">OR:</span></span>
  
- <span data-ttu-id="d8a0c-141">La regla tiene marcas de la ST_EXIT_LEVEL y el ST_ONLY_WHEN_OOF establecer.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-141">The rule has both the ST_EXIT_LEVEL and ST_ONLY_WHEN_OOF flags set.</span></span> <span data-ttu-id="d8a0c-142">A continuación, el servidor no debe evaluar las reglas posteriores.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-142">Then, the server must not evaluate any subsequent rules.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="d8a0c-143">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d8a0c-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d8a0c-144">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d8a0c-144">Protocol specifications</span></span>

<span data-ttu-id="d8a0c-145">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8a0c-145">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8a0c-146">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d8a0c-147">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8a0c-147">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8a0c-148">Manipula los mensajes de correo electrónico entrante en un servidor.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-148">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d8a0c-149">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d8a0c-149">Header files</span></span>

<span data-ttu-id="d8a0c-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d8a0c-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="d8a0c-151">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-151">Provides data type definitions.</span></span>
    
<span data-ttu-id="d8a0c-152">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d8a0c-152">Mapitags.h</span></span>
  
> <span data-ttu-id="d8a0c-153">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d8a0c-153">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d8a0c-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8a0c-154">See also</span></span>



[<span data-ttu-id="d8a0c-155">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d8a0c-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d8a0c-156">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d8a0c-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d8a0c-157">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d8a0c-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d8a0c-158">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d8a0c-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
