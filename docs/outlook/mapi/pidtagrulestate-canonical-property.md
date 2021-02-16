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
# <a name="pidtagrulestate-canonical-property"></a><span data-ttu-id="cc93a-103">Propiedad canónica PidTagRuleState</span><span class="sxs-lookup"><span data-stu-id="cc93a-103">PidTagRuleState Canonical Property</span></span>

  
  
<span data-ttu-id="cc93a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc93a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc93a-105">Valor que se interpreta como una combinación de máscara de bits de marcas que especifican el estado de la regla.</span><span class="sxs-lookup"><span data-stu-id="cc93a-105">A value interpreted as a bitmask combination of flags that specify the state of the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cc93a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cc93a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cc93a-107">PR_RULE_STATE</span><span class="sxs-lookup"><span data-stu-id="cc93a-107">PR_RULE_STATE</span></span>  <br/> |
|<span data-ttu-id="cc93a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cc93a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cc93a-109">0x6677</span><span class="sxs-lookup"><span data-stu-id="cc93a-109">0x6677</span></span>  <br/> |
|<span data-ttu-id="cc93a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="cc93a-110">Data type:</span></span>  <br/> |<span data-ttu-id="cc93a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cc93a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cc93a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cc93a-112">Area:</span></span>  <br/> |<span data-ttu-id="cc93a-113">Reglas del lado servidor</span><span class="sxs-lookup"><span data-stu-id="cc93a-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc93a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cc93a-114">Remarks</span></span>

<span data-ttu-id="cc93a-115">En la tabla siguiente se definen los valores posibles de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="cc93a-115">The following table defines the possible values of this property.</span></span>
  
<span data-ttu-id="cc93a-116">EN (ST_ENABLED, máscara de bits 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="cc93a-116">EN (ST_ENABLED, bitmask 0x00000001)</span></span>
  
> <span data-ttu-id="cc93a-117">La regla está habilitada para la ejecución.</span><span class="sxs-lookup"><span data-stu-id="cc93a-117">The rule is enabled for execution.</span></span> <span data-ttu-id="cc93a-118">Si no se establece esta marca, el servidor debe omitir esta regla al evaluar las reglas.</span><span class="sxs-lookup"><span data-stu-id="cc93a-118">If this flag is not set, the server must skip this rule when evaluating rules.</span></span>
    
<span data-ttu-id="cc93a-119">ER (ST_ERROR, máscara de bits 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="cc93a-119">ER (ST_ERROR, bitmask 0x00000002)</span></span>
  
> <span data-ttu-id="cc93a-120">El servidor ha encontrado un error al procesar la regla.</span><span class="sxs-lookup"><span data-stu-id="cc93a-120">The server has encountered an error processing the rule.</span></span>
    
<span data-ttu-id="cc93a-121">OF (ST_ONLY_WHEN_OOF, máscara de bits 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="cc93a-121">OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)</span></span>
  
> <span data-ttu-id="cc93a-122">La regla solo se ejecuta cuando el usuario establece el estado fuera de la oficina (OOF) en el buzón.</span><span class="sxs-lookup"><span data-stu-id="cc93a-122">The rule is executed only when the user sets the Out of Office (OOF) state on the mailbox.</span></span> <span data-ttu-id="cc93a-123">Esta marca no debe establecerse en una regla de carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="cc93a-123">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="cc93a-124">HI (ST_KEEP_OOF_HIST, máscara de bits 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="cc93a-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span></span>
  
> <span data-ttu-id="cc93a-125">Esta marca no debe establecerse en una regla de carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="cc93a-125">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="cc93a-126">EL (ST_EXIT_LEVEL, máscara de bits 0x00000010)</span><span class="sxs-lookup"><span data-stu-id="cc93a-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span></span>
  
> <span data-ttu-id="cc93a-127">La evaluación de reglas finalizará después de ejecutar esta regla, excepto para la evaluación de reglas fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="cc93a-127">Rule evaluation will end after executing this rule, except for evaluation of Out of Office rules.</span></span>
    
<span data-ttu-id="cc93a-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, máscara de bits 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="cc93a-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span></span>
  
> <span data-ttu-id="cc93a-129">Se puede omitir la evaluación de esta regla.</span><span class="sxs-lookup"><span data-stu-id="cc93a-129">Evaluation of this rule may be skipped.</span></span>
    
<span data-ttu-id="cc93a-130">PE (ST_RULE_PARSE_ERROR, máscara de bits 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="cc93a-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span></span>
  
> <span data-ttu-id="cc93a-131">El servidor ha encontrado un error al analizar los datos de regla proporcionados por el cliente.</span><span class="sxs-lookup"><span data-stu-id="cc93a-131">The server has encountered an error parsing the rule data provided by the client.</span></span>
    
<span data-ttu-id="cc93a-132">X</span><span class="sxs-lookup"><span data-stu-id="cc93a-132">X</span></span>
  
> <span data-ttu-id="cc93a-133">No se usa en este protocolo.</span><span class="sxs-lookup"><span data-stu-id="cc93a-133">Unused by this protocol.</span></span> <span data-ttu-id="cc93a-134">El cliente no debe modificar este bit.</span><span class="sxs-lookup"><span data-stu-id="cc93a-134">This bit must not be modified by the client.</span></span>
    
<span data-ttu-id="cc93a-135">Ten en cuenta la interacción entre ST_ONLY_WHEN_OOF y ST_EXIT_LEVEL marcas:</span><span class="sxs-lookup"><span data-stu-id="cc93a-135">Note on the interaction between ST_ONLY_WHEN_OOF and ST_EXIT_LEVEL flags:</span></span> 
  
<span data-ttu-id="cc93a-136">Cuando el estado "Fuera de la oficina" se establece en el buzón y una condición de regla se evalúa como TRUE,</span><span class="sxs-lookup"><span data-stu-id="cc93a-136">When the "Out of Office" state is set on the mailbox, and a rule condition evaluates to TRUE,</span></span> 
  
<span data-ttu-id="cc93a-137">Y:</span><span class="sxs-lookup"><span data-stu-id="cc93a-137">AND:</span></span>
  
- <span data-ttu-id="cc93a-138">La regla tiene la marca ST_EXIT_LEVEL y no tiene ST_ONLY_WHEN_OOF marca establecida.</span><span class="sxs-lookup"><span data-stu-id="cc93a-138">The rule has the ST_EXIT_LEVEL flag set and does not have ST_ONLY_WHEN_OOF flag set.</span></span> <span data-ttu-id="cc93a-139">A continuación, el servidor no debe evaluar las reglas posteriores que no tengan una marca ST_ONLY_WHEN_OOF establecida y debe evaluar las reglas posteriores que tengan ST_ONLY_WHEN_OOF marca establecida.</span><span class="sxs-lookup"><span data-stu-id="cc93a-139">Then, the server must not evaluate subsequent rules that do not have ST_ONLY_WHEN_OOF flag set, and must evaluate subsequent rules that have ST_ONLY_WHEN_OOF flag set.</span></span>
    
<span data-ttu-id="cc93a-140">O BIEN:</span><span class="sxs-lookup"><span data-stu-id="cc93a-140">OR:</span></span>
  
- <span data-ttu-id="cc93a-141">La regla tiene las marcas de ST_EXIT_LEVEL y ST_ONLY_WHEN_OOF establecidas.</span><span class="sxs-lookup"><span data-stu-id="cc93a-141">The rule has both the ST_EXIT_LEVEL and ST_ONLY_WHEN_OOF flags set.</span></span> <span data-ttu-id="cc93a-142">A continuación, el servidor no debe evaluar ninguna regla posterior.</span><span class="sxs-lookup"><span data-stu-id="cc93a-142">Then, the server must not evaluate any subsequent rules.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="cc93a-143">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc93a-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cc93a-144">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="cc93a-144">Protocol specifications</span></span>

<span data-ttu-id="cc93a-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc93a-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc93a-146">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="cc93a-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cc93a-147">[[MS-OJORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc93a-147">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc93a-148">Manipula los mensajes de correo electrónico entrantes en un servidor.</span><span class="sxs-lookup"><span data-stu-id="cc93a-148">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cc93a-149">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cc93a-149">Header files</span></span>

<span data-ttu-id="cc93a-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cc93a-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="cc93a-151">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cc93a-151">Provides data type definitions.</span></span>
    
<span data-ttu-id="cc93a-152">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cc93a-152">Mapitags.h</span></span>
  
> <span data-ttu-id="cc93a-153">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="cc93a-153">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc93a-154">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cc93a-154">See also</span></span>



[<span data-ttu-id="cc93a-155">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cc93a-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cc93a-156">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="cc93a-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cc93a-157">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="cc93a-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cc93a-158">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="cc93a-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

