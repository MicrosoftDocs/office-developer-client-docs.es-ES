---
title: Propiedad canónica PidTagDepth
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDepth
api_type:
- HeaderDef
ms.assetid: 04d444a5-e97f-48e6-89a5-8a6cb2136408
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 75d390edd06aaf826f6b8c2d996e4e08bf6a7334
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360854"
---
# <a name="pidtagdepth-canonical-property"></a><span data-ttu-id="d9700-103">Propiedad canónica PidTagDepth</span><span class="sxs-lookup"><span data-stu-id="d9700-103">PidTagDepth Canonical Property</span></span>

  
  
<span data-ttu-id="d9700-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9700-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9700-105">Contiene un entero que representa el nivel relativo de sangría, o profundidad, de un objeto en una tabla de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="d9700-105">Contains an integer that represents the relative level of indentation, or depth, of an object in a hierarchy table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9700-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d9700-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d9700-107">PR_DEPTH</span><span class="sxs-lookup"><span data-stu-id="d9700-107">PR_DEPTH</span></span>  <br/> |
|<span data-ttu-id="d9700-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d9700-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d9700-109">0x3005</span><span class="sxs-lookup"><span data-stu-id="d9700-109">0x3005</span></span>  <br/> |
|<span data-ttu-id="d9700-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d9700-110">Data type:</span></span>  <br/> |<span data-ttu-id="d9700-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d9700-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d9700-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d9700-112">Area:</span></span>  <br/> |<span data-ttu-id="d9700-113">Common MAPI</span><span class="sxs-lookup"><span data-stu-id="d9700-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9700-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d9700-114">Remarks</span></span>

<span data-ttu-id="d9700-115">Esta propiedad también puede especificar el nivel de categorización de una fila en una tabla de contenido o la profundidad de jerarquía en una tabla de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="d9700-115">This property can also specify the categorization level of a row in a contents table or the hierarchy depth in a hierarchy table.</span></span> <span data-ttu-id="d9700-116">La profundidad es de base cero, donde cero representa la categoría más a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="d9700-116">The depth is zero-based, where zero represents the leftmost category.</span></span> <span data-ttu-id="d9700-117">En todos los casos, el valor de la propiedad representa un valor relativo en lugar de un valor absoluto.</span><span class="sxs-lookup"><span data-stu-id="d9700-117">In all cases, the property value represents a relative value rather than an absolute value.</span></span> <span data-ttu-id="d9700-118">En la tabla de jerarquías, por ejemplo, el valor de profundidad es relativo al contenedor desde el que se recuperó la tabla de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="d9700-118">In the hierarchy table, for example, the depth value is relative to the container from which the hierarchy table was retrieved.</span></span> <span data-ttu-id="d9700-119">La profundidad no representa una profundidad absoluta desde el contenedor raíz.</span><span class="sxs-lookup"><span data-stu-id="d9700-119">The depth does not represent an absolute depth from the root container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d9700-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d9700-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d9700-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d9700-121">Protocol specifications</span></span>

<span data-ttu-id="d9700-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9700-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9700-123">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d9700-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d9700-124">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9700-124">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9700-125">Incluye operaciones admitidas para los objetos de la tabla principal.</span><span class="sxs-lookup"><span data-stu-id="d9700-125">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="d9700-126">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9700-126">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9700-127">Especifica las propiedades y operaciones de las listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="d9700-127">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d9700-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d9700-128">Header files</span></span>

<span data-ttu-id="d9700-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d9700-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="d9700-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d9700-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="d9700-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="d9700-131">Mapitags.h</span></span>
  
> <span data-ttu-id="d9700-132">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d9700-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9700-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9700-133">See also</span></span>



[<span data-ttu-id="d9700-134">Propiedad canónica PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="d9700-134">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="d9700-135">Propiedad canónica PidTagSelectable</span><span class="sxs-lookup"><span data-stu-id="d9700-135">PidTagSelectable Canonical Property</span></span>](pidtagselectable-canonical-property.md)


[<span data-ttu-id="d9700-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d9700-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d9700-137">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="d9700-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d9700-138">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d9700-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d9700-139">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="d9700-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

