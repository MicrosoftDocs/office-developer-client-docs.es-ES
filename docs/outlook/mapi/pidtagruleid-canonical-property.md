---
title: Propiedad canónico PidTagRuleId
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 52a6132dcd6aa2c3a2951f3d1a6458808364dccb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820157"
---
# <a name="pidtagruleid-canonical-property"></a><span data-ttu-id="0c8a9-103">Propiedad canónico PidTagRuleId</span><span class="sxs-lookup"><span data-stu-id="0c8a9-103">PidTagRuleId Canonical Property</span></span>

  
  
<span data-ttu-id="0c8a9-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0c8a9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0c8a9-105">Especifica un identificador único que genera el servidor de mensajería para cada regla cuando se crea la regla por primera vez.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-105">Specifies a unique identifier the messaging server generates for each rule when the rule is first created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0c8a9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0c8a9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0c8a9-107">PR_RULE_ID</span><span class="sxs-lookup"><span data-stu-id="0c8a9-107">PR_RULE_ID</span></span>  <br/> |
|<span data-ttu-id="0c8a9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0c8a9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0c8a9-109">0x6674</span><span class="sxs-lookup"><span data-stu-id="0c8a9-109">0x6674</span></span>  <br/> |
|<span data-ttu-id="0c8a9-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0c8a9-110">Data type:</span></span>  <br/> |<span data-ttu-id="0c8a9-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="0c8a9-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="0c8a9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0c8a9-112">Area:</span></span>  <br/> |<span data-ttu-id="0c8a9-113">Reglas del servidor</span><span class="sxs-lookup"><span data-stu-id="0c8a9-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c8a9-114">Notas</span><span class="sxs-lookup"><span data-stu-id="0c8a9-114">Remarks</span></span>

<span data-ttu-id="0c8a9-115">El cliente no debe especificar esta propiedad al crear una nueva regla, pero debe especificarlo al modificar o eliminar una regla.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-115">The client must not specify this property when creating a new rule but must specify it when modifying or deleting a rule.</span></span>
  
<span data-ttu-id="0c8a9-116">Cuando se elimina una regla, la única propiedad que el cliente debe pasar es **PR_RULE_ID** y no debe pasar en cualquier otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-116">When deleting a rule, the only property the client must pass is **PR_RULE_ID** and should not pass in any other property.</span></span> <span data-ttu-id="0c8a9-117">El servidor debe omitir las propiedades que no sean de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-117">The server must ignore properties other than this property.</span></span> <span data-ttu-id="0c8a9-118">Al agregar una regla, el cliente no debe pasar en **PR_RULE_ID**, debe pasar el **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) y **PR_RULE_PROVIDER** ([ PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) propiedades.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-118">When adding a rule, the client must not pass in **PR_RULE_ID**, it must pass in the **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) and **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) properties.</span></span> <span data-ttu-id="0c8a9-119">Al modificar una regla, el cliente debe pasar en **PR_RULE_ID** y debe pasar en el resto de las propiedades que deben modificarse.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-119">When modifying a rule, the client must pass in **PR_RULE_ID** and should pass in the rest of the properties that need to be modified.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0c8a9-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0c8a9-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0c8a9-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0c8a9-121">Protocol specifications</span></span>

<span data-ttu-id="0c8a9-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c8a9-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c8a9-123">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0c8a9-124">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c8a9-124">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c8a9-125">Manipula los mensajes de correo electrónico entrante en un servidor.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-125">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0c8a9-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0c8a9-126">Header files</span></span>

<span data-ttu-id="0c8a9-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0c8a9-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0c8a9-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="0c8a9-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0c8a9-129">Mapitags.h</span></span>
  
> <span data-ttu-id="0c8a9-130">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0c8a9-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="0c8a9-131">See also</span></span>



[<span data-ttu-id="0c8a9-132">Propiedad canónico PidTagRuleCondition</span><span class="sxs-lookup"><span data-stu-id="0c8a9-132">PidTagRuleCondition Canonical Property</span></span>](pidtagrulecondition-canonical-property.md)
  
[<span data-ttu-id="0c8a9-133">Propiedad canónico PidTagRuleActions</span><span class="sxs-lookup"><span data-stu-id="0c8a9-133">PidTagRuleActions Canonical Property</span></span>](pidtagruleactions-canonical-property.md)
  
[<span data-ttu-id="0c8a9-134">Propiedad canónico PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="0c8a9-134">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="0c8a9-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0c8a9-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0c8a9-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="0c8a9-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0c8a9-137">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="0c8a9-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0c8a9-138">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0c8a9-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

