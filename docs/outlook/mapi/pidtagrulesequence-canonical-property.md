---
title: Propiedad canónica PidTagRuleSequence
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleSequence
api_type:
- COM
ms.assetid: c42f2539-f7d6-464a-a82c-f0ac51823168
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7f36562ba189cd8f547056b93c0f0373ee9a3360
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563495"
---
# <a name="pidtagrulesequence-canonical-property"></a><span data-ttu-id="c55f8-103">Propiedad canónica PidTagRuleSequence</span><span class="sxs-lookup"><span data-stu-id="c55f8-103">PidTagRuleSequence Canonical Property</span></span>

  
  
<span data-ttu-id="c55f8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c55f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c55f8-105">Un valor utilizado para determinar el orden en que se evalúan y se ejecutan las reglas.</span><span class="sxs-lookup"><span data-stu-id="c55f8-105">A value used to determine the order in which rules are evaluated and executed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c55f8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c55f8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c55f8-107">PR_RULE_SEQUENCE</span><span class="sxs-lookup"><span data-stu-id="c55f8-107">PR_RULE_SEQUENCE</span></span>  <br/> |
|<span data-ttu-id="c55f8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c55f8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c55f8-109">0x6676</span><span class="sxs-lookup"><span data-stu-id="c55f8-109">0x6676</span></span>  <br/> |
|<span data-ttu-id="c55f8-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c55f8-110">Data type:</span></span>  <br/> |<span data-ttu-id="c55f8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c55f8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c55f8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c55f8-112">Area:</span></span>  <br/> |<span data-ttu-id="c55f8-113">Reglas del servidor</span><span class="sxs-lookup"><span data-stu-id="c55f8-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c55f8-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c55f8-114">Remarks</span></span>

<span data-ttu-id="c55f8-115">Las reglas se evalúan en secuencia de acuerdo con el orden de aumento de este valor.</span><span class="sxs-lookup"><span data-stu-id="c55f8-115">Rules are evaluated in sequence according to the increasing order of this value.</span></span> <span data-ttu-id="c55f8-116">El orden de evaluación para las reglas que tienen el mismo valor de esta propiedad no está definido.</span><span class="sxs-lookup"><span data-stu-id="c55f8-116">The evaluation order for rules that have the same value in this property is undefined.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c55f8-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c55f8-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c55f8-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c55f8-118">Protocol specifications</span></span>

<span data-ttu-id="c55f8-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c55f8-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c55f8-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c55f8-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c55f8-121">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c55f8-121">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c55f8-122">Manipula los mensajes de correo electrónico entrante en un servidor.</span><span class="sxs-lookup"><span data-stu-id="c55f8-122">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="c55f8-123">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c55f8-123">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c55f8-124">Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con los elementos de mensaje y calendario cuando actúen en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="c55f8-124">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
<span data-ttu-id="c55f8-125">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c55f8-125">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c55f8-126">Incluye las operaciones permitidas para los objetos de la tabla principal.</span><span class="sxs-lookup"><span data-stu-id="c55f8-126">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="c55f8-127">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c55f8-127">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c55f8-128">Especifica las operaciones permitidas para los objetos de almacén de mensajes principales.</span><span class="sxs-lookup"><span data-stu-id="c55f8-128">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c55f8-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c55f8-129">Header files</span></span>

<span data-ttu-id="c55f8-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c55f8-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="c55f8-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c55f8-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="c55f8-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c55f8-132">Mapitags.h</span></span>
  
> <span data-ttu-id="c55f8-133">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c55f8-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c55f8-134">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c55f8-134">See also</span></span>



[<span data-ttu-id="c55f8-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c55f8-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c55f8-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c55f8-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c55f8-137">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c55f8-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c55f8-138">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c55f8-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

