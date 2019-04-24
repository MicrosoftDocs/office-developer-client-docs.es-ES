---
title: Propiedad canónica PidTagExtendedRuleMessageCondition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageCondition
api_type:
- HeaderDef
ms.assetid: 891851e1-e4a4-4c20-a26c-7223bcca35f7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7c444485c3a443694e2902343a02da5605bde39f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316334"
---
# <a name="pidtagextendedrulemessagecondition-canonical-property"></a><span data-ttu-id="98baa-103">Propiedad canónica PidTagExtendedRuleMessageCondition</span><span class="sxs-lookup"><span data-stu-id="98baa-103">PidTagExtendedRuleMessageCondition Canonical Property</span></span>

  
  
<span data-ttu-id="98baa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98baa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98baa-105">Contiene información acerca de las propiedades con nombre que están incluidas dentro de las condiciones de regla extendida.</span><span class="sxs-lookup"><span data-stu-id="98baa-105">Contains information about any named properties that are contained inside of extended rule conditions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="98baa-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="98baa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="98baa-107">PR_EXTENDED_RULE_MSG_CONDITION</span><span class="sxs-lookup"><span data-stu-id="98baa-107">PR_EXTENDED_RULE_MSG_CONDITION</span></span>  <br/> |
|<span data-ttu-id="98baa-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="98baa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="98baa-109">0x0E9A</span><span class="sxs-lookup"><span data-stu-id="98baa-109">0x0E9A</span></span>  <br/> |
|<span data-ttu-id="98baa-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="98baa-110">Data type:</span></span>  <br/> |<span data-ttu-id="98baa-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="98baa-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="98baa-112">Área:</span><span class="sxs-lookup"><span data-stu-id="98baa-112">Area:</span></span>  <br/> |<span data-ttu-id="98baa-113">Reglas</span><span class="sxs-lookup"><span data-stu-id="98baa-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98baa-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="98baa-114">Remarks</span></span>

<span data-ttu-id="98baa-115">Esta propiedad debe establecerse en un mensaje FAI.</span><span class="sxs-lookup"><span data-stu-id="98baa-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="98baa-116">Tiene el mismo propósito que **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), pero contiene información adicional acerca de las propiedades con nombre que se usan.</span><span class="sxs-lookup"><span data-stu-id="98baa-116">It serves the same purpose as **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), but contains additional information about the named properties used.</span></span> <span data-ttu-id="98baa-117">Todos los valores de cadena contenidos en cualquier parte del valor de la propiedad Condition deben tener formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="98baa-117">All string values contained in any part of this condition property value must be in Unicode format.</span></span>
  
<span data-ttu-id="98baa-118">Para obtener información sobre el formato de esta propiedad binaria, vea [[ms-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="98baa-118">For information about the format of this binary property, see [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="98baa-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="98baa-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="98baa-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="98baa-120">Protocol specifications</span></span>

<span data-ttu-id="98baa-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98baa-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98baa-122">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="98baa-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="98baa-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98baa-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98baa-124">Manipula los mensajes de correo electrónico entrantes en un servidor.</span><span class="sxs-lookup"><span data-stu-id="98baa-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="98baa-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="98baa-125">Header files</span></span>

<span data-ttu-id="98baa-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="98baa-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="98baa-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="98baa-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="98baa-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="98baa-128">Mapitags.h</span></span>
  
> <span data-ttu-id="98baa-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="98baa-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98baa-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="98baa-130">See also</span></span>



[<span data-ttu-id="98baa-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="98baa-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="98baa-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="98baa-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="98baa-133">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="98baa-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="98baa-134">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="98baa-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

