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
ms.openlocfilehash: 70e7a20a69b7467c1d8c31469273dcc28ce219ae
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382634"
---
# <a name="pidtagrulesequence-canonical-property"></a><span data-ttu-id="431ea-103">Propiedad canónica PidTagRuleSequence</span><span class="sxs-lookup"><span data-stu-id="431ea-103">PidTagRuleSequence Canonical Property</span></span>

  
  
<span data-ttu-id="431ea-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="431ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="431ea-105">Un valor utilizado para determinar el orden en que se evalúan y se ejecutan las reglas.</span><span class="sxs-lookup"><span data-stu-id="431ea-105">A value used to determine the order in which rules are evaluated and executed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="431ea-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="431ea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="431ea-107">PR_RULE_SEQUENCE</span><span class="sxs-lookup"><span data-stu-id="431ea-107">PR_RULE_SEQUENCE</span></span>  <br/> |
|<span data-ttu-id="431ea-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="431ea-108">Identifier:</span></span>  <br/> |<span data-ttu-id="431ea-109">0x6676</span><span class="sxs-lookup"><span data-stu-id="431ea-109">0x6676</span></span>  <br/> |
|<span data-ttu-id="431ea-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="431ea-110">Data type:</span></span>  <br/> |<span data-ttu-id="431ea-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="431ea-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="431ea-112">Área:</span><span class="sxs-lookup"><span data-stu-id="431ea-112">Area:</span></span>  <br/> |<span data-ttu-id="431ea-113">Reglas del servidor</span><span class="sxs-lookup"><span data-stu-id="431ea-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="431ea-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="431ea-114">Remarks</span></span>

<span data-ttu-id="431ea-115">Las reglas se evalúan en secuencia de acuerdo con el orden de aumento de este valor.</span><span class="sxs-lookup"><span data-stu-id="431ea-115">Rules are evaluated in sequence according to the increasing order of this value.</span></span> <span data-ttu-id="431ea-116">El orden de evaluación para las reglas que tienen el mismo valor de esta propiedad no está definido.</span><span class="sxs-lookup"><span data-stu-id="431ea-116">The evaluation order for rules that have the same value in this property is undefined.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="431ea-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="431ea-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="431ea-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="431ea-118">Protocol specifications</span></span>

<span data-ttu-id="431ea-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="431ea-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="431ea-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="431ea-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="431ea-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="431ea-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="431ea-122">Manipula los mensajes de correo electrónico entrante en un servidor.</span><span class="sxs-lookup"><span data-stu-id="431ea-122">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="431ea-123">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="431ea-123">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="431ea-124">Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con los elementos de mensaje y calendario cuando actúen en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="431ea-124">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
<span data-ttu-id="431ea-125">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="431ea-125">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="431ea-126">Incluye las operaciones permitidas para los objetos de la tabla principal.</span><span class="sxs-lookup"><span data-stu-id="431ea-126">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="431ea-127">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="431ea-127">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="431ea-128">Especifica las operaciones permitidas para los objetos de almacén de mensajes principales.</span><span class="sxs-lookup"><span data-stu-id="431ea-128">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="431ea-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="431ea-129">Header files</span></span>

<span data-ttu-id="431ea-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="431ea-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="431ea-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="431ea-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="431ea-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="431ea-132">Mapitags.h</span></span>
  
> <span data-ttu-id="431ea-133">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="431ea-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="431ea-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="431ea-134">See also</span></span>



[<span data-ttu-id="431ea-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="431ea-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="431ea-136">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="431ea-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="431ea-137">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="431ea-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="431ea-138">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="431ea-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

