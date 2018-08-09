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
ms.openlocfilehash: f4eae388d51b0428d508a675681fa4cd1d94e46f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820159"
---
# <a name="pidtagrulecondition-canonical-property"></a><span data-ttu-id="e0324-103">Propiedad canónica PidTagRuleCondition</span><span class="sxs-lookup"><span data-stu-id="e0324-103">PidTagRuleCondition Canonical Property</span></span>

  
  
<span data-ttu-id="e0324-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e0324-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e0324-105">La condición que se usa al evaluar la regla.</span><span class="sxs-lookup"><span data-stu-id="e0324-105">The condition used when you evaluate the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e0324-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e0324-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e0324-107">PR_RULE_CONDITION</span><span class="sxs-lookup"><span data-stu-id="e0324-107">PR_RULE_CONDITION</span></span>  <br/> |
|<span data-ttu-id="e0324-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e0324-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e0324-109">0x6679</span><span class="sxs-lookup"><span data-stu-id="e0324-109">0x6679</span></span>  <br/> |
|<span data-ttu-id="e0324-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e0324-110">Data type:</span></span>  <br/> |<span data-ttu-id="e0324-111">PT_SRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="e0324-111">PT_SRESTRICTION</span></span>  <br/> |
|<span data-ttu-id="e0324-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e0324-112">Area:</span></span>  <br/> |<span data-ttu-id="e0324-113">Reglas del servidor</span><span class="sxs-lookup"><span data-stu-id="e0324-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0324-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e0324-114">Remarks</span></span>

<span data-ttu-id="e0324-115">La condición se expresa como una **restricción** y el búfer de **PropertyValue** contiene la estructura de **restricción** empaquetada tal como se especifica en [[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e0324-115">The condition is expressed as a **Restriction** and the **PropertyValue** buffer contains the **Restriction** structure packaged as specified in [[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e0324-116">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e0324-116">MFCMAPI reference</span></span>

<span data-ttu-id="e0324-117">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="e0324-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e0324-118">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="e0324-118">**File**</span></span>|<span data-ttu-id="e0324-119">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="e0324-119">**Function**</span></span>|<span data-ttu-id="e0324-120">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="e0324-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e0324-121">ImportProcs.cpp</span><span class="sxs-lookup"><span data-stu-id="e0324-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="e0324-122">PropCopyMore, HrCopyRestriction</span><span class="sxs-lookup"><span data-stu-id="e0324-122">PropCopyMore, HrCopyRestriction</span></span>  <br/> |<span data-ttu-id="e0324-123">Estas funciones demuestran cómo analizar una propiedad **PT_SRESTRICTION** con el fin de copiar a otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="e0324-123">These functions demonstrate how to parse a **PT_SRESTRICTION** property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e0324-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e0324-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e0324-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e0324-125">Protocol specifications</span></span>

<span data-ttu-id="e0324-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0324-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0324-127">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e0324-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e0324-128">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0324-128">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0324-129">Manipula los mensajes de correo electrónico entrante en un servidor.</span><span class="sxs-lookup"><span data-stu-id="e0324-129">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="e0324-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0324-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0324-131">Define las estructuras de datos básicos que se usan en las operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="e0324-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e0324-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e0324-132">Header files</span></span>

<span data-ttu-id="e0324-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e0324-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="e0324-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e0324-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="e0324-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e0324-135">Mapitags.h</span></span>
  
> <span data-ttu-id="e0324-136">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="e0324-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e0324-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0324-137">See also</span></span>



[<span data-ttu-id="e0324-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e0324-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e0324-139">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e0324-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e0324-140">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e0324-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e0324-141">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e0324-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

