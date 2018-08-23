---
title: Propiedad canónica PidTagRuleActions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleActions
api_type:
- COM
ms.assetid: 3ec4259a-8fe9-46c3-82b8-42c6907b8515
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ede62c792b1241a150c9d0a05adbe47fe0b6c0e7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567464"
---
# <a name="pidtagruleactions-canonical-property"></a><span data-ttu-id="f695a-103">Propiedad canónica PidTagRuleActions</span><span class="sxs-lookup"><span data-stu-id="f695a-103">PidTagRuleActions Canonical Property</span></span>

  
  
<span data-ttu-id="f695a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f695a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f695a-105">Contiene el conjunto de acciones asociadas con la regla.</span><span class="sxs-lookup"><span data-stu-id="f695a-105">Contains the set of actions associated with the rule.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f695a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f695a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f695a-107">PR_RULE_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="f695a-107">PR_RULE_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="f695a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f695a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f695a-109">0x6680</span><span class="sxs-lookup"><span data-stu-id="f695a-109">0x6680</span></span>  <br/> |
|<span data-ttu-id="f695a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f695a-110">Data type:</span></span>  <br/> |<span data-ttu-id="f695a-111">PT_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="f695a-111">PT_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="f695a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f695a-112">Area:</span></span>  <br/> |<span data-ttu-id="f695a-113">Reglas del servidor</span><span class="sxs-lookup"><span data-stu-id="f695a-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f695a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f695a-114">Remarks</span></span>

<span data-ttu-id="f695a-115">Las acciones se expresan como una acción de regla y el búfer de valor de propiedad contiene la estructura de búfer de datos de acción de regla empaquetada tal como se especifica en [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f695a-115">The actions are expressed as a rule action and the property value buffer contains the rule action data buffer structure packaged as specified in [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f695a-116">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f695a-116">MFCMAPI reference</span></span>

<span data-ttu-id="f695a-117">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f695a-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f695a-118">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="f695a-118">**File**</span></span>|<span data-ttu-id="f695a-119">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="f695a-119">**Function**</span></span>|<span data-ttu-id="f695a-120">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="f695a-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f695a-121">ImportProcs.cpp</span><span class="sxs-lookup"><span data-stu-id="f695a-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="f695a-122">PropCopyMore, HrCopyActions</span><span class="sxs-lookup"><span data-stu-id="f695a-122">PropCopyMore, HrCopyActions</span></span>  <br/> |<span data-ttu-id="f695a-123">Estas funciones demuestran cómo analizar una propiedad PT_ACTIONS con el fin de copiar a otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="f695a-123">These functions demonstrate how to parse a PT_ACTIONS property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f695a-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f695a-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f695a-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f695a-125">Protocol specifications</span></span>

<span data-ttu-id="f695a-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f695a-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f695a-127">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f695a-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f695a-128">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f695a-128">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f695a-129">Manipula los mensajes de correo electrónico entrante en un servidor.</span><span class="sxs-lookup"><span data-stu-id="f695a-129">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f695a-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f695a-130">Header files</span></span>

<span data-ttu-id="f695a-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f695a-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="f695a-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f695a-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="f695a-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f695a-133">Mapitags.h</span></span>
  
> <span data-ttu-id="f695a-134">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f695a-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f695a-135">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f695a-135">See also</span></span>



[<span data-ttu-id="f695a-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f695a-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f695a-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f695a-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f695a-138">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f695a-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f695a-139">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f695a-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

