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
ms.openlocfilehash: a0e15462cd3dc14c93155e34e47b7caac2c04087
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338615"
---
# <a name="pidtagrulestate-canonical-property"></a><span data-ttu-id="022ac-103">Propiedad canónica PidTagRuleState</span><span class="sxs-lookup"><span data-stu-id="022ac-103">PidTagRuleState Canonical Property</span></span>

  
  
<span data-ttu-id="022ac-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="022ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="022ac-105">Un valor que se interpreta como una combinación de máscara de máscara que especifica el estado de la regla.</span><span class="sxs-lookup"><span data-stu-id="022ac-105">A value interpreted as a bitmask combination of flags that specify the state of the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="022ac-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="022ac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="022ac-107">PR_RULE_STATE</span><span class="sxs-lookup"><span data-stu-id="022ac-107">PR_RULE_STATE</span></span>  <br/> |
|<span data-ttu-id="022ac-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="022ac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="022ac-109">0x6677</span><span class="sxs-lookup"><span data-stu-id="022ac-109">0x6677</span></span>  <br/> |
|<span data-ttu-id="022ac-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="022ac-110">Data type:</span></span>  <br/> |<span data-ttu-id="022ac-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="022ac-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="022ac-112">Área:</span><span class="sxs-lookup"><span data-stu-id="022ac-112">Area:</span></span>  <br/> |<span data-ttu-id="022ac-113">Reglas del lado servidor</span><span class="sxs-lookup"><span data-stu-id="022ac-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="022ac-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="022ac-114">Remarks</span></span>

<span data-ttu-id="022ac-115">En la tabla siguiente se definen los valores posibles de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="022ac-115">The following table defines the possible values of this property.</span></span>
  
<span data-ttu-id="022ac-116">EN (ST_ENABLED, máscara de la letra 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="022ac-116">EN (ST_ENABLED, bitmask 0x00000001)</span></span>
  
> <span data-ttu-id="022ac-117">La regla está habilitada para la ejecución.</span><span class="sxs-lookup"><span data-stu-id="022ac-117">The rule is enabled for execution.</span></span> <span data-ttu-id="022ac-118">Si no se establece esta marca, el servidor debe omitir esta regla al evaluar las reglas.</span><span class="sxs-lookup"><span data-stu-id="022ac-118">If this flag is not set, the server must skip this rule when evaluating rules.</span></span>
    
<span data-ttu-id="022ac-119">ER (ST_ERROR, máscara de la letra 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="022ac-119">ER (ST_ERROR, bitmask 0x00000002)</span></span>
  
> <span data-ttu-id="022ac-120">El servidor ha encontrado un error al procesar la regla.</span><span class="sxs-lookup"><span data-stu-id="022ac-120">The server has encountered an error processing the rule.</span></span>
    
<span data-ttu-id="022ac-121">DE (ST_ONLY_WHEN_OOF, máscara de 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="022ac-121">OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)</span></span>
  
> <span data-ttu-id="022ac-122">La regla solo se ejecuta cuando el usuario establece el estado fuera de la oficina (OOF) en el buzón.</span><span class="sxs-lookup"><span data-stu-id="022ac-122">The rule is executed only when the user sets the Out of Office (OOF) state on the mailbox.</span></span> <span data-ttu-id="022ac-123">Esta marca no debe establecerse en una regla de carpeta pública.</span><span class="sxs-lookup"><span data-stu-id="022ac-123">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="022ac-124">HI (ST_KEEP_OOF_HIST, máscara de 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="022ac-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span></span>
  
> <span data-ttu-id="022ac-125">Esta marca no debe establecerse en una regla de carpeta pública.</span><span class="sxs-lookup"><span data-stu-id="022ac-125">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="022ac-126">El (ST_EXIT_LEVEL, máscara de la máscara 0x00000010)</span><span class="sxs-lookup"><span data-stu-id="022ac-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span></span>
  
> <span data-ttu-id="022ac-127">La evaluación de la regla finalizará después de ejecutar esta regla, excepto para la evaluación de las reglas de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="022ac-127">Rule evaluation will end after executing this rule, except for evaluation of Out of Office rules.</span></span>
    
<span data-ttu-id="022ac-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, máscara de máscara 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="022ac-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span></span>
  
> <span data-ttu-id="022ac-129">Se puede omitir la evaluación de esta regla.</span><span class="sxs-lookup"><span data-stu-id="022ac-129">Evaluation of this rule may be skipped.</span></span>
    
<span data-ttu-id="022ac-130">PE (ST_RULE_PARSE_ERROR, máscara de 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="022ac-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span></span>
  
> <span data-ttu-id="022ac-131">El servidor detectó un error al analizar los datos de la regla proporcionada por el cliente.</span><span class="sxs-lookup"><span data-stu-id="022ac-131">The server has encountered an error parsing the rule data provided by the client.</span></span>
    
<span data-ttu-id="022ac-132">X</span><span class="sxs-lookup"><span data-stu-id="022ac-132">X</span></span>
  
> <span data-ttu-id="022ac-133">No se usa con este protocolo.</span><span class="sxs-lookup"><span data-stu-id="022ac-133">Unused by this protocol.</span></span> <span data-ttu-id="022ac-134">El cliente no debe modificar este bit.</span><span class="sxs-lookup"><span data-stu-id="022ac-134">This bit must not be modified by the client.</span></span>
    
<span data-ttu-id="022ac-135">Tenga en cuenta la interacción entre ST_ONLY_WHEN_OOF y las marcas ST_EXIT_LEVEL:</span><span class="sxs-lookup"><span data-stu-id="022ac-135">Note on the interaction between ST_ONLY_WHEN_OOF and ST_EXIT_LEVEL flags:</span></span> 
  
<span data-ttu-id="022ac-136">Cuando el estado "fuera de la oficina" está establecido en el buzón y una condición de regla se evalúa como TRUE,</span><span class="sxs-lookup"><span data-stu-id="022ac-136">When the "Out of Office" state is set on the mailbox, and a rule condition evaluates to TRUE,</span></span> 
  
<span data-ttu-id="022ac-137">Y</span><span class="sxs-lookup"><span data-stu-id="022ac-137">AND:</span></span>
  
- <span data-ttu-id="022ac-138">La regla tiene establecida la marca ST_EXIT_LEVEL y no tiene establecida la marca ST_ONLY_WHEN_OOF.</span><span class="sxs-lookup"><span data-stu-id="022ac-138">The rule has the ST_EXIT_LEVEL flag set and does not have ST_ONLY_WHEN_OOF flag set.</span></span> <span data-ttu-id="022ac-139">A continuación, el servidor no debe evaluar las reglas subsiguientes que no tienen establecida ninguna marca ST_ONLY_WHEN_OOF y debe evaluar las reglas posteriores que tienen establecida la marca ST_ONLY_WHEN_OOF.</span><span class="sxs-lookup"><span data-stu-id="022ac-139">Then, the server must not evaluate subsequent rules that do not have ST_ONLY_WHEN_OOF flag set, and must evaluate subsequent rules that have ST_ONLY_WHEN_OOF flag set.</span></span>
    
<span data-ttu-id="022ac-140">O</span><span class="sxs-lookup"><span data-stu-id="022ac-140">OR:</span></span>
  
- <span data-ttu-id="022ac-141">La regla tiene establecidos los dos indicadores ST_EXIT_LEVEL y ST_ONLY_WHEN_OOF.</span><span class="sxs-lookup"><span data-stu-id="022ac-141">The rule has both the ST_EXIT_LEVEL and ST_ONLY_WHEN_OOF flags set.</span></span> <span data-ttu-id="022ac-142">A continuación, el servidor no debe evaluar ninguna regla posterior.</span><span class="sxs-lookup"><span data-stu-id="022ac-142">Then, the server must not evaluate any subsequent rules.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="022ac-143">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="022ac-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="022ac-144">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="022ac-144">Protocol specifications</span></span>

<span data-ttu-id="022ac-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="022ac-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="022ac-146">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="022ac-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="022ac-147">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="022ac-147">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="022ac-148">Manipula los mensajes de correo electrónico entrantes en un servidor.</span><span class="sxs-lookup"><span data-stu-id="022ac-148">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="022ac-149">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="022ac-149">Header files</span></span>

<span data-ttu-id="022ac-150">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="022ac-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="022ac-151">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="022ac-151">Provides data type definitions.</span></span>
    
<span data-ttu-id="022ac-152">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="022ac-152">Mapitags.h</span></span>
  
> <span data-ttu-id="022ac-153">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="022ac-153">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="022ac-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="022ac-154">See also</span></span>



[<span data-ttu-id="022ac-155">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="022ac-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="022ac-156">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="022ac-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="022ac-157">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="022ac-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="022ac-158">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="022ac-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

