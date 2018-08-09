---
title: Propiedad canónica PidTagExtendedRuleSizeLimit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleSizeLimit
api_type:
- HeaderDef
ms.assetid: 87186764-fb58-4cdf-804d-bb13c5a8cb65
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 01d25614780f10f30d9e1314ea7f60ad3fbb4af0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819496"
---
# <a name="pidtagextendedrulesizelimit-canonical-property"></a><span data-ttu-id="52447-103">Propiedad canónica PidTagExtendedRuleSizeLimit</span><span class="sxs-lookup"><span data-stu-id="52447-103">PidTagExtendedRuleSizeLimit Canonical Property</span></span>

  
  
<span data-ttu-id="52447-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="52447-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="52447-105">Contiene el tamaño máximo, en bytes, se permite al usuario acumular para una sola regla "extendida".</span><span class="sxs-lookup"><span data-stu-id="52447-105">Contains the maximum size, in bytes, the user is allowed to accumulate for a single "extended" rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="52447-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="52447-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="52447-107">PR_EXTENDED_RULE_SIZE_LIMIT</span><span class="sxs-lookup"><span data-stu-id="52447-107">PR_EXTENDED_RULE_SIZE_LIMIT</span></span>  <br/> |
|<span data-ttu-id="52447-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="52447-108">Identifier:</span></span>  <br/> |<span data-ttu-id="52447-109">0x0E9B</span><span class="sxs-lookup"><span data-stu-id="52447-109">0x0E9B</span></span>  <br/> |
|<span data-ttu-id="52447-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="52447-110">Data type:</span></span>  <br/> |<span data-ttu-id="52447-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="52447-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="52447-112">Área:</span><span class="sxs-lookup"><span data-stu-id="52447-112">Area:</span></span>  <br/> |<span data-ttu-id="52447-113">Rules</span><span class="sxs-lookup"><span data-stu-id="52447-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52447-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52447-114">Remarks</span></span>

<span data-ttu-id="52447-115">Si esta propiedad se establece en el objeto de inicio de sesión, el cliente debe mantener el tamaño de la propiedad **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) en el valor especificado por esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="52447-115">If this property is set on the logon object, the client should keep the size of the **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) property under the value specified by this property.</span></span> <span data-ttu-id="52447-116">Por el contrario, el servidor debe devolver un error si el cliente intenta establecer una propiedad binaria que es demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="52447-116">Conversely, the server should return an error if the client does attempt to set a binary property that is too large.</span></span>
  
<span data-ttu-id="52447-117">Para obtener información acerca de las reglas extendidas, vea [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="52447-117">For information about extended rules, see [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="52447-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="52447-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="52447-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="52447-119">Protocol specifications</span></span>

<span data-ttu-id="52447-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52447-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52447-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="52447-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="52447-122">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52447-122">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52447-123">Especifica las operaciones permitidas para los objetos de almacén de mensajes principales.</span><span class="sxs-lookup"><span data-stu-id="52447-123">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="52447-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="52447-124">Header files</span></span>

<span data-ttu-id="52447-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="52447-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="52447-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="52447-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="52447-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="52447-127">Mapitags.h</span></span>
  
> <span data-ttu-id="52447-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="52447-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52447-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="52447-129">See also</span></span>



[<span data-ttu-id="52447-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="52447-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="52447-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="52447-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="52447-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="52447-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="52447-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="52447-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

