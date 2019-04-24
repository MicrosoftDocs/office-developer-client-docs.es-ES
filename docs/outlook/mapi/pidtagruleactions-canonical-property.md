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
ms.openlocfilehash: ab246414f7caaf76f462d9b80e762fe614c77c21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278903"
---
# <a name="pidtagruleactions-canonical-property"></a><span data-ttu-id="5a261-103">Propiedad canónica PidTagRuleActions</span><span class="sxs-lookup"><span data-stu-id="5a261-103">PidTagRuleActions Canonical Property</span></span>

  
  
<span data-ttu-id="5a261-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a261-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a261-105">Contiene el conjunto de acciones asociadas a la regla.</span><span class="sxs-lookup"><span data-stu-id="5a261-105">Contains the set of actions associated with the rule.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a261-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5a261-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a261-107">PR_RULE_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="5a261-107">PR_RULE_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="5a261-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5a261-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5a261-109">0x6680</span><span class="sxs-lookup"><span data-stu-id="5a261-109">0x6680</span></span>  <br/> |
|<span data-ttu-id="5a261-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5a261-110">Data type:</span></span>  <br/> |<span data-ttu-id="5a261-111">PT_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="5a261-111">PT_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="5a261-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5a261-112">Area:</span></span>  <br/> |<span data-ttu-id="5a261-113">Reglas del lado servidor</span><span class="sxs-lookup"><span data-stu-id="5a261-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a261-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5a261-114">Remarks</span></span>

<span data-ttu-id="5a261-115">Las acciones se expresan como una acción de regla y el búfer de valor de propiedad contiene la estructura del búfer de datos de la acción de regla empaquetada como se especifica en [[ms-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5a261-115">The actions are expressed as a rule action and the property value buffer contains the rule action data buffer structure packaged as specified in [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5a261-116">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5a261-116">MFCMAPI reference</span></span>

<span data-ttu-id="5a261-117">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="5a261-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5a261-118">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="5a261-118">**File**</span></span>|<span data-ttu-id="5a261-119">**Función**</span><span class="sxs-lookup"><span data-stu-id="5a261-119">**Function**</span></span>|<span data-ttu-id="5a261-120">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="5a261-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5a261-121">ImportProcs. cpp</span><span class="sxs-lookup"><span data-stu-id="5a261-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="5a261-122">PropCopyMore, HrCopyActions</span><span class="sxs-lookup"><span data-stu-id="5a261-122">PropCopyMore, HrCopyActions</span></span>  <br/> |<span data-ttu-id="5a261-123">Estas funciones muestran cómo analizar una propiedad PT_ACTIONS para poder copiar en otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="5a261-123">These functions demonstrate how to parse a PT_ACTIONS property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5a261-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a261-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5a261-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="5a261-125">Protocol specifications</span></span>

<span data-ttu-id="5a261-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a261-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a261-127">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5a261-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5a261-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a261-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a261-129">Manipula los mensajes de correo electrónico entrantes en un servidor.</span><span class="sxs-lookup"><span data-stu-id="5a261-129">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5a261-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5a261-130">Header files</span></span>

<span data-ttu-id="5a261-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5a261-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a261-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5a261-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="5a261-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5a261-133">Mapitags.h</span></span>
  
> <span data-ttu-id="5a261-134">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="5a261-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a261-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a261-135">See also</span></span>



[<span data-ttu-id="5a261-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5a261-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a261-137">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="5a261-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a261-138">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5a261-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a261-139">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="5a261-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

