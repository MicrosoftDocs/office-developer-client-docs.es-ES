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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321248"
---
# <a name="pidtagrulesequence-canonical-property"></a><span data-ttu-id="40bf1-103">Propiedad canónica PidTagRuleSequence</span><span class="sxs-lookup"><span data-stu-id="40bf1-103">PidTagRuleSequence Canonical Property</span></span>

  
  
<span data-ttu-id="40bf1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40bf1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40bf1-105">Valor que se usa para determinar el orden en que se evalúan y ejecutan las reglas.</span><span class="sxs-lookup"><span data-stu-id="40bf1-105">A value used to determine the order in which rules are evaluated and executed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40bf1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="40bf1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="40bf1-107">PR_RULE_SEQUENCE</span><span class="sxs-lookup"><span data-stu-id="40bf1-107">PR_RULE_SEQUENCE</span></span>  <br/> |
|<span data-ttu-id="40bf1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="40bf1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="40bf1-109">0x6676</span><span class="sxs-lookup"><span data-stu-id="40bf1-109">0x6676</span></span>  <br/> |
|<span data-ttu-id="40bf1-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="40bf1-110">Data type:</span></span>  <br/> |<span data-ttu-id="40bf1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="40bf1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="40bf1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="40bf1-112">Area:</span></span>  <br/> |<span data-ttu-id="40bf1-113">Reglas del lado servidor</span><span class="sxs-lookup"><span data-stu-id="40bf1-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40bf1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="40bf1-114">Remarks</span></span>

<span data-ttu-id="40bf1-115">Las reglas se evalúan en secuencia según el orden creciente de este valor.</span><span class="sxs-lookup"><span data-stu-id="40bf1-115">Rules are evaluated in sequence according to the increasing order of this value.</span></span> <span data-ttu-id="40bf1-116">El orden de evaluación de las reglas que tienen el mismo valor en esta propiedad no está definido.</span><span class="sxs-lookup"><span data-stu-id="40bf1-116">The evaluation order for rules that have the same value in this property is undefined.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="40bf1-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="40bf1-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="40bf1-118">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="40bf1-118">Protocol specifications</span></span>

<span data-ttu-id="40bf1-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40bf1-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40bf1-120">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="40bf1-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="40bf1-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40bf1-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40bf1-122">Manipula los mensajes de correo electrónico entrantes en un servidor.</span><span class="sxs-lookup"><span data-stu-id="40bf1-122">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="40bf1-123">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40bf1-123">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40bf1-124">Especifica métodos para conectarse a buzones y configurarlos como delegados e interacciones con elementos de calendario y mensajes cuando actúan en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="40bf1-124">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
<span data-ttu-id="40bf1-125">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40bf1-125">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40bf1-126">Incluye operaciones permitidas para los objetos de tabla principal.</span><span class="sxs-lookup"><span data-stu-id="40bf1-126">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="40bf1-127">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40bf1-127">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40bf1-128">Especifica las operaciones permitidas para los objetos principales del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="40bf1-128">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="40bf1-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="40bf1-129">Header files</span></span>

<span data-ttu-id="40bf1-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="40bf1-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="40bf1-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="40bf1-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="40bf1-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="40bf1-132">Mapitags.h</span></span>
  
> <span data-ttu-id="40bf1-133">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="40bf1-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="40bf1-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="40bf1-134">See also</span></span>



[<span data-ttu-id="40bf1-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="40bf1-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="40bf1-136">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="40bf1-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="40bf1-137">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="40bf1-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="40bf1-138">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="40bf1-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

