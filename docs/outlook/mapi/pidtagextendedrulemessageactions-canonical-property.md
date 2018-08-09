---
title: Propiedad canónica PidTagExtendedRuleMessageActions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageActions
api_type:
- HeaderDef
ms.assetid: 1cf277d4-76ec-4902-9e54-f1780cee49bf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5425496a5b7845daabf736978e6ed24518451fe0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819509"
---
# <a name="pidtagextendedrulemessageactions-canonical-property"></a><span data-ttu-id="d1744-103">Propiedad canónica PidTagExtendedRuleMessageActions</span><span class="sxs-lookup"><span data-stu-id="d1744-103">PidTagExtendedRuleMessageActions Canonical Property</span></span>

  
  
<span data-ttu-id="d1744-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d1744-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d1744-105">Contiene información adicional acerca de las propiedades con nombre que se utiliza en un mensaje de información de asociados de carpeta (FAI).</span><span class="sxs-lookup"><span data-stu-id="d1744-105">Contains additional information about the named properties used in a Folder Associated Information (FAI) message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1744-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d1744-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d1744-107">PR_EXTENDED_RULE_MSG_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="d1744-107">PR_EXTENDED_RULE_MSG_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="d1744-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d1744-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d1744-109">0x0E99</span><span class="sxs-lookup"><span data-stu-id="d1744-109">0x0E99</span></span>  <br/> |
|<span data-ttu-id="d1744-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d1744-110">Data type:</span></span>  <br/> |<span data-ttu-id="d1744-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d1744-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d1744-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d1744-112">Area:</span></span>  <br/> |<span data-ttu-id="d1744-113">Rules</span><span class="sxs-lookup"><span data-stu-id="d1744-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1744-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d1744-114">Remarks</span></span>

<span data-ttu-id="d1744-115">Esta propiedad debe establecerse en un mensaje FAI.</span><span class="sxs-lookup"><span data-stu-id="d1744-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="d1744-116">Esta propiedad sirve para el mismo propósito como **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), pero contiene información adicional acerca de la versión de la regla y las propiedades con nombre que se almacenan en la acción de regla, así como información sobre las acciones que deben ser realizado por esta regla.</span><span class="sxs-lookup"><span data-stu-id="d1744-116">This property serves the same purpose as **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), but contains additional information about the version of the rule and the named properties stored in the rule action, as well as information about the actions to be performed by this rule.</span></span> <span data-ttu-id="d1744-117">Todos los valores de cadena contenidos en cualquier parte del búfer de acción que se usa para contener acciones deben estar en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="d1744-117">All string values contained in any part of the action buffer used to contain actions must be in Unicode format.</span></span>
  
<span data-ttu-id="d1744-118">Para obtener información acerca del formato de esta propiedad binaria, vea [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d1744-118">For information about the format of this binary property, see [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d1744-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1744-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d1744-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d1744-120">Protocol specifications</span></span>

<span data-ttu-id="d1744-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1744-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1744-122">Proporciona referencias a las especificaciones de protocolo relacionadas de Exchange Server..</span><span class="sxs-lookup"><span data-stu-id="d1744-122">Provides references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="d1744-123">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1744-123">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1744-124">Manipula los mensajes de correo electrónico entrante en un servidor.</span><span class="sxs-lookup"><span data-stu-id="d1744-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d1744-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d1744-125">Header files</span></span>

<span data-ttu-id="d1744-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d1744-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d1744-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d1744-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="d1744-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d1744-128">Mapitags.h</span></span>
  
> <span data-ttu-id="d1744-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d1744-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d1744-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1744-130">See also</span></span>



[<span data-ttu-id="d1744-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d1744-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d1744-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d1744-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d1744-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d1744-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d1744-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d1744-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

