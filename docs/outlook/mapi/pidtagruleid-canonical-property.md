---
title: Propiedad canónica PidTagRuleId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleId
api_type:
- COM
ms.assetid: 341e8db0-52b7-4ba7-aaa6-eedf2783b4e8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8d88838893836c550136be9556299258b44e3e49
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359496"
---
# <a name="pidtagruleid-canonical-property"></a><span data-ttu-id="bb018-103">Propiedad canónica PidTagRuleId</span><span class="sxs-lookup"><span data-stu-id="bb018-103">PidTagRuleId Canonical Property</span></span>

  
  
<span data-ttu-id="bb018-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb018-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb018-105">Especifica un identificador único que el servidor de mensajería genera para cada regla cuando se crea la regla por primera vez.</span><span class="sxs-lookup"><span data-stu-id="bb018-105">Specifies a unique identifier the messaging server generates for each rule when the rule is first created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb018-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="bb018-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bb018-107">PR_RULE_ID</span><span class="sxs-lookup"><span data-stu-id="bb018-107">PR_RULE_ID</span></span>  <br/> |
|<span data-ttu-id="bb018-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="bb018-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bb018-109">0x6674</span><span class="sxs-lookup"><span data-stu-id="bb018-109">0x6674</span></span>  <br/> |
|<span data-ttu-id="bb018-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="bb018-110">Data type:</span></span>  <br/> |<span data-ttu-id="bb018-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="bb018-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="bb018-112">Área:</span><span class="sxs-lookup"><span data-stu-id="bb018-112">Area:</span></span>  <br/> |<span data-ttu-id="bb018-113">Reglas del lado servidor</span><span class="sxs-lookup"><span data-stu-id="bb018-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb018-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb018-114">Remarks</span></span>

<span data-ttu-id="bb018-115">El cliente no debe especificar esta propiedad al crear una nueva regla, pero debe especificarla al modificar o eliminar una regla.</span><span class="sxs-lookup"><span data-stu-id="bb018-115">The client must not specify this property when creating a new rule but must specify it when modifying or deleting a rule.</span></span>
  
<span data-ttu-id="bb018-116">Al eliminar una regla, la única propiedad que debe pasar el cliente **es PR_RULE_ID** y no debe pasar en ninguna otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="bb018-116">When deleting a rule, the only property the client must pass is **PR_RULE_ID** and should not pass in any other property.</span></span> <span data-ttu-id="bb018-117">El servidor debe omitir propiedades que no son esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="bb018-117">The server must ignore properties other than this property.</span></span> <span data-ttu-id="bb018-118">Al agregar una regla, el cliente no debe pasar **en PR_RULE_ID**, debe pasar las propiedades **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) y **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bb018-118">When adding a rule, the client must not pass in **PR_RULE_ID**, it must pass in the **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) and **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) properties.</span></span> <span data-ttu-id="bb018-119">Al modificar una regla, el  cliente debe pasar PR_RULE_ID y pasar el resto de las propiedades que deben modificarse.</span><span class="sxs-lookup"><span data-stu-id="bb018-119">When modifying a rule, the client must pass in **PR_RULE_ID** and should pass in the rest of the properties that need to be modified.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bb018-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb018-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bb018-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="bb018-121">Protocol specifications</span></span>

<span data-ttu-id="bb018-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb018-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb018-123">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="bb018-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bb018-124">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb018-124">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb018-125">Manipula los mensajes de correo electrónico entrantes en un servidor.</span><span class="sxs-lookup"><span data-stu-id="bb018-125">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bb018-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="bb018-126">Header files</span></span>

<span data-ttu-id="bb018-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb018-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb018-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="bb018-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="bb018-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bb018-129">Mapitags.h</span></span>
  
> <span data-ttu-id="bb018-130">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="bb018-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb018-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb018-131">See also</span></span>



[<span data-ttu-id="bb018-132">Propiedad canónica PidTagRuleCondition</span><span class="sxs-lookup"><span data-stu-id="bb018-132">PidTagRuleCondition Canonical Property</span></span>](pidtagrulecondition-canonical-property.md)
  
[<span data-ttu-id="bb018-133">Propiedad canónica PidTagRuleActions</span><span class="sxs-lookup"><span data-stu-id="bb018-133">PidTagRuleActions Canonical Property</span></span>](pidtagruleactions-canonical-property.md)
  
[<span data-ttu-id="bb018-134">Propiedad canónica PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="bb018-134">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="bb018-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bb018-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb018-136">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="bb018-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb018-137">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="bb018-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb018-138">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="bb018-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

