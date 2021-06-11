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
ms.openlocfilehash: 70f09d6db5940fcb9b980cc839988113bd3a3e2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316341"
---
# <a name="pidtagextendedrulemessageactions-canonical-property"></a><span data-ttu-id="5cc34-103">Propiedad canónica PidTagExtendedRuleMessageActions</span><span class="sxs-lookup"><span data-stu-id="5cc34-103">PidTagExtendedRuleMessageActions Canonical Property</span></span>

  
  
<span data-ttu-id="5cc34-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5cc34-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5cc34-105">Contiene información adicional acerca de las propiedades con nombre usadas en un mensaje De información asociada a carpetas (FAI).</span><span class="sxs-lookup"><span data-stu-id="5cc34-105">Contains additional information about the named properties used in a Folder Associated Information (FAI) message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5cc34-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5cc34-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5cc34-107">PR_EXTENDED_RULE_MSG_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="5cc34-107">PR_EXTENDED_RULE_MSG_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="5cc34-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5cc34-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5cc34-109">0x0E99</span><span class="sxs-lookup"><span data-stu-id="5cc34-109">0x0E99</span></span>  <br/> |
|<span data-ttu-id="5cc34-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5cc34-110">Data type:</span></span>  <br/> |<span data-ttu-id="5cc34-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5cc34-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5cc34-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5cc34-112">Area:</span></span>  <br/> |<span data-ttu-id="5cc34-113">Rules</span><span class="sxs-lookup"><span data-stu-id="5cc34-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5cc34-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5cc34-114">Remarks</span></span>

<span data-ttu-id="5cc34-115">Esta propiedad debe establecerse en un mensaje fai.</span><span class="sxs-lookup"><span data-stu-id="5cc34-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="5cc34-116">Esta propiedad tiene el mismo propósito que **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), pero contiene información adicional sobre la versión de la regla y las propiedades con nombre almacenadas en la acción de regla, así como información sobre las acciones que debe realizar esta regla.</span><span class="sxs-lookup"><span data-stu-id="5cc34-116">This property serves the same purpose as **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), but contains additional information about the version of the rule and the named properties stored in the rule action, as well as information about the actions to be performed by this rule.</span></span> <span data-ttu-id="5cc34-117">Todos los valores de cadena contenidos en cualquier parte del búfer de acciones usado para contener acciones deben estar en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="5cc34-117">All string values contained in any part of the action buffer used to contain actions must be in Unicode format.</span></span>
  
<span data-ttu-id="5cc34-118">Para obtener información sobre el formato de esta propiedad binaria, vea [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5cc34-118">For information about the format of this binary property, see [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5cc34-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5cc34-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5cc34-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="5cc34-120">Protocol specifications</span></span>

<span data-ttu-id="5cc34-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5cc34-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5cc34-122">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="5cc34-122">Provides references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="5cc34-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5cc34-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5cc34-124">Manipula los mensajes de correo electrónico entrantes en un servidor.</span><span class="sxs-lookup"><span data-stu-id="5cc34-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5cc34-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5cc34-125">Header files</span></span>

<span data-ttu-id="5cc34-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5cc34-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5cc34-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5cc34-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="5cc34-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5cc34-128">Mapitags.h</span></span>
  
> <span data-ttu-id="5cc34-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="5cc34-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5cc34-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="5cc34-130">See also</span></span>



[<span data-ttu-id="5cc34-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5cc34-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5cc34-132">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="5cc34-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5cc34-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5cc34-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5cc34-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="5cc34-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

