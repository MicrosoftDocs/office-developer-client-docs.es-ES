---
title: Propiedad canónica PidTagRuleCondition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleCondition
api_type:
- COM
ms.assetid: 8a11e846-c62f-4c06-876f-94623d50cc3b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 81dbd097523f4cb5016a3e846f63cfbe1c643de2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575864"
---
# <a name="pidtagrulecondition-canonical-property"></a><span data-ttu-id="e30eb-103">Propiedad canónica PidTagRuleCondition</span><span class="sxs-lookup"><span data-stu-id="e30eb-103">PidTagRuleCondition Canonical Property</span></span>

  
  
<span data-ttu-id="e30eb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e30eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e30eb-105">La condición que se usa al evaluar la regla.</span><span class="sxs-lookup"><span data-stu-id="e30eb-105">The condition used when you evaluate the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e30eb-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e30eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e30eb-107">PR_RULE_CONDITION</span><span class="sxs-lookup"><span data-stu-id="e30eb-107">PR_RULE_CONDITION</span></span>  <br/> |
|<span data-ttu-id="e30eb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e30eb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e30eb-109">0x6679</span><span class="sxs-lookup"><span data-stu-id="e30eb-109">0x6679</span></span>  <br/> |
|<span data-ttu-id="e30eb-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e30eb-110">Data type:</span></span>  <br/> |<span data-ttu-id="e30eb-111">PT_SRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="e30eb-111">PT_SRESTRICTION</span></span>  <br/> |
|<span data-ttu-id="e30eb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e30eb-112">Area:</span></span>  <br/> |<span data-ttu-id="e30eb-113">Reglas del servidor</span><span class="sxs-lookup"><span data-stu-id="e30eb-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e30eb-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e30eb-114">Remarks</span></span>

<span data-ttu-id="e30eb-115">La condición se expresa como una **restricción** y el búfer de **PropertyValue** contiene la estructura de **restricción** empaquetada tal como se especifica en [[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e30eb-115">The condition is expressed as a **Restriction** and the **PropertyValue** buffer contains the **Restriction** structure packaged as specified in [[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e30eb-116">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e30eb-116">MFCMAPI reference</span></span>

<span data-ttu-id="e30eb-117">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="e30eb-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e30eb-118">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="e30eb-118">**File**</span></span>|<span data-ttu-id="e30eb-119">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="e30eb-119">**Function**</span></span>|<span data-ttu-id="e30eb-120">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="e30eb-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e30eb-121">ImportProcs.cpp</span><span class="sxs-lookup"><span data-stu-id="e30eb-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="e30eb-122">PropCopyMore, HrCopyRestriction</span><span class="sxs-lookup"><span data-stu-id="e30eb-122">PropCopyMore, HrCopyRestriction</span></span>  <br/> |<span data-ttu-id="e30eb-123">Estas funciones demuestran cómo analizar una propiedad **PT_SRESTRICTION** con el fin de copiar a otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="e30eb-123">These functions demonstrate how to parse a **PT_SRESTRICTION** property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e30eb-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e30eb-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e30eb-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e30eb-125">Protocol specifications</span></span>

<span data-ttu-id="e30eb-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e30eb-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e30eb-127">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e30eb-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e30eb-128">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e30eb-128">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e30eb-129">Manipula los mensajes de correo electrónico entrante en un servidor.</span><span class="sxs-lookup"><span data-stu-id="e30eb-129">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="e30eb-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e30eb-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e30eb-131">Define las estructuras de datos básicos que se usan en las operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="e30eb-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e30eb-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e30eb-132">Header files</span></span>

<span data-ttu-id="e30eb-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e30eb-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="e30eb-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e30eb-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="e30eb-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e30eb-135">Mapitags.h</span></span>
  
> <span data-ttu-id="e30eb-136">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="e30eb-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e30eb-137">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e30eb-137">See also</span></span>



[<span data-ttu-id="e30eb-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e30eb-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e30eb-139">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e30eb-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e30eb-140">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e30eb-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e30eb-141">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e30eb-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

