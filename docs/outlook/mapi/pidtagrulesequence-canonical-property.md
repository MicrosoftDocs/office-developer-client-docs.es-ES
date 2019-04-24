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
# <a name="pidtagrulesequence-canonical-property"></a><span data-ttu-id="0661c-103">Propiedad canónica PidTagRuleSequence</span><span class="sxs-lookup"><span data-stu-id="0661c-103">PidTagRuleSequence Canonical Property</span></span>

  
  
<span data-ttu-id="0661c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0661c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0661c-105">Un valor que se usa para determinar el orden en el que se evalúan y ejecutan las reglas.</span><span class="sxs-lookup"><span data-stu-id="0661c-105">A value used to determine the order in which rules are evaluated and executed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0661c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0661c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0661c-107">PR_RULE_SEQUENCE</span><span class="sxs-lookup"><span data-stu-id="0661c-107">PR_RULE_SEQUENCE</span></span>  <br/> |
|<span data-ttu-id="0661c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0661c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0661c-109">0x6676</span><span class="sxs-lookup"><span data-stu-id="0661c-109">0x6676</span></span>  <br/> |
|<span data-ttu-id="0661c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0661c-110">Data type:</span></span>  <br/> |<span data-ttu-id="0661c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0661c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0661c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0661c-112">Area:</span></span>  <br/> |<span data-ttu-id="0661c-113">Reglas del lado servidor</span><span class="sxs-lookup"><span data-stu-id="0661c-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0661c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0661c-114">Remarks</span></span>

<span data-ttu-id="0661c-115">Las reglas se evalúan en secuencia según el orden creciente de este valor.</span><span class="sxs-lookup"><span data-stu-id="0661c-115">Rules are evaluated in sequence according to the increasing order of this value.</span></span> <span data-ttu-id="0661c-116">El orden de evaluación de las reglas que tienen el mismo valor en esta propiedad es undefined.</span><span class="sxs-lookup"><span data-stu-id="0661c-116">The evaluation order for rules that have the same value in this property is undefined.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0661c-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0661c-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0661c-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0661c-118">Protocol specifications</span></span>

<span data-ttu-id="0661c-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0661c-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0661c-120">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0661c-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0661c-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0661c-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0661c-122">Manipula los mensajes de correo electrónico entrantes en un servidor.</span><span class="sxs-lookup"><span data-stu-id="0661c-122">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="0661c-123">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0661c-123">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0661c-124">Especifica los métodos para conectarse a los buzones y configurarlos como delegados, e interacciones con los elementos de calendario y mensajes cuando actúan en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="0661c-124">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
<span data-ttu-id="0661c-125">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0661c-125">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0661c-126">Incluye operaciones admitidas para los objetos de la tabla principal.</span><span class="sxs-lookup"><span data-stu-id="0661c-126">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="0661c-127">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0661c-127">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0661c-128">Especifica operaciones permitidas para los objetos de almacén de mensajes principales.</span><span class="sxs-lookup"><span data-stu-id="0661c-128">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0661c-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0661c-129">Header files</span></span>

<span data-ttu-id="0661c-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0661c-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="0661c-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0661c-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="0661c-132">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="0661c-132">Mapitags.h</span></span>
  
> <span data-ttu-id="0661c-133">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0661c-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0661c-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="0661c-134">See also</span></span>



[<span data-ttu-id="0661c-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0661c-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0661c-136">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="0661c-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0661c-137">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0661c-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0661c-138">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="0661c-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

