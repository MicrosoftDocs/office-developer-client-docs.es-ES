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
ms.openlocfilehash: 92008a387bb0130207af012df209a3aa6881d40e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593175"
---
# <a name="pidtagextendedrulemessagecondition-canonical-property"></a><span data-ttu-id="78561-103">Propiedad canónica PidTagExtendedRuleMessageCondition</span><span class="sxs-lookup"><span data-stu-id="78561-103">PidTagExtendedRuleMessageCondition Canonical Property</span></span>

  
  
<span data-ttu-id="78561-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78561-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78561-105">Contiene información acerca de las propiedades con nombre que se encuentran dentro de las condiciones de regla extendida.</span><span class="sxs-lookup"><span data-stu-id="78561-105">Contains information about any named properties that are contained inside of extended rule conditions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="78561-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="78561-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="78561-107">PR_EXTENDED_RULE_MSG_CONDITION</span><span class="sxs-lookup"><span data-stu-id="78561-107">PR_EXTENDED_RULE_MSG_CONDITION</span></span>  <br/> |
|<span data-ttu-id="78561-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="78561-108">Identifier:</span></span>  <br/> |<span data-ttu-id="78561-109">0x0E9A</span><span class="sxs-lookup"><span data-stu-id="78561-109">0x0E9A</span></span>  <br/> |
|<span data-ttu-id="78561-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="78561-110">Data type:</span></span>  <br/> |<span data-ttu-id="78561-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="78561-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="78561-112">Área:</span><span class="sxs-lookup"><span data-stu-id="78561-112">Area:</span></span>  <br/> |<span data-ttu-id="78561-113">Rules</span><span class="sxs-lookup"><span data-stu-id="78561-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78561-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="78561-114">Remarks</span></span>

<span data-ttu-id="78561-115">Esta propiedad debe establecerse en un mensaje FAI.</span><span class="sxs-lookup"><span data-stu-id="78561-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="78561-116">Sirve para el mismo propósito como **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), pero contiene información adicional acerca de las propiedades con nombre que se usa.</span><span class="sxs-lookup"><span data-stu-id="78561-116">It serves the same purpose as **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), but contains additional information about the named properties used.</span></span> <span data-ttu-id="78561-117">Todos los valores de cadena contenidos en cualquier parte del valor de esta propiedad de condición deben estar en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="78561-117">All string values contained in any part of this condition property value must be in Unicode format.</span></span>
  
<span data-ttu-id="78561-118">Para obtener información acerca del formato de esta propiedad binaria, vea [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="78561-118">For information about the format of this binary property, see [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="78561-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="78561-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="78561-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="78561-120">Protocol specifications</span></span>

<span data-ttu-id="78561-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78561-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78561-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="78561-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="78561-123">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78561-123">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78561-124">Manipula los mensajes de correo electrónico entrante en un servidor.</span><span class="sxs-lookup"><span data-stu-id="78561-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="78561-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="78561-125">Header files</span></span>

<span data-ttu-id="78561-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="78561-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="78561-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="78561-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="78561-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="78561-128">Mapitags.h</span></span>
  
> <span data-ttu-id="78561-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="78561-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="78561-130">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="78561-130">See also</span></span>



[<span data-ttu-id="78561-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="78561-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="78561-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="78561-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="78561-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="78561-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="78561-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="78561-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

