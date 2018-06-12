---
title: Propiedad canónico PidTagDepth
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 25af87004ef5616a6c6fc575c647fdd1794d710f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819431"
---
# <a name="pidtagdepth-canonical-property"></a><span data-ttu-id="c185d-103">Propiedad canónico PidTagDepth</span><span class="sxs-lookup"><span data-stu-id="c185d-103">PidTagDepth Canonical Property</span></span>

  
  
<span data-ttu-id="c185d-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c185d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c185d-105">Contiene un número entero que representa el nivel de sangría, o profundidad, de un objeto en una tabla de jerarquías relativo.</span><span class="sxs-lookup"><span data-stu-id="c185d-105">Contains an integer that represents the relative level of indentation, or depth, of an object in a hierarchy table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c185d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c185d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c185d-107">PR_DEPTH</span><span class="sxs-lookup"><span data-stu-id="c185d-107">PR_DEPTH</span></span>  <br/> |
|<span data-ttu-id="c185d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c185d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c185d-109">0x3005</span><span class="sxs-lookup"><span data-stu-id="c185d-109">0x3005</span></span>  <br/> |
|<span data-ttu-id="c185d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c185d-110">Data type:</span></span>  <br/> |<span data-ttu-id="c185d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c185d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c185d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c185d-112">Area:</span></span>  <br/> |<span data-ttu-id="c185d-113">MAPI comunes</span><span class="sxs-lookup"><span data-stu-id="c185d-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c185d-114">Notas</span><span class="sxs-lookup"><span data-stu-id="c185d-114">Remarks</span></span>

<span data-ttu-id="c185d-115">Esta propiedad también puede especificar el nivel de la categorización de una fila en una tabla de contenido o la profundidad de jerarquía en una tabla de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="c185d-115">This property can also specify the categorization level of a row in a contents table or the hierarchy depth in a hierarchy table.</span></span> <span data-ttu-id="c185d-116">La profundidad está basada en cero, donde cero representa la categoría más a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="c185d-116">The depth is zero-based, where zero represents the leftmost category.</span></span> <span data-ttu-id="c185d-117">En todos los casos, el valor de la propiedad representa un valor relativo en lugar de un valor absoluto.</span><span class="sxs-lookup"><span data-stu-id="c185d-117">In all cases, the property value represents a relative value rather than an absolute value.</span></span> <span data-ttu-id="c185d-118">En la tabla de jerarquía, por ejemplo, el valor de profundidad es en relación con el contenedor desde el que se ha recuperado en la tabla de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="c185d-118">In the hierarchy table, for example, the depth value is relative to the container from which the hierarchy table was retrieved.</span></span> <span data-ttu-id="c185d-119">La profundidad no representan una profundidad absoluta desde el contenedor raíz.</span><span class="sxs-lookup"><span data-stu-id="c185d-119">The depth does not represent an absolute depth from the root container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c185d-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c185d-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c185d-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c185d-121">Protocol specifications</span></span>

<span data-ttu-id="c185d-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c185d-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c185d-123">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c185d-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c185d-124">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c185d-124">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c185d-125">Incluye las operaciones permitidas para los objetos de la tabla principal.</span><span class="sxs-lookup"><span data-stu-id="c185d-125">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="c185d-126">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c185d-126">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c185d-127">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="c185d-127">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c185d-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c185d-128">Header files</span></span>

<span data-ttu-id="c185d-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c185d-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="c185d-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c185d-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="c185d-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c185d-131">Mapitags.h</span></span>
  
> <span data-ttu-id="c185d-132">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c185d-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c185d-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="c185d-133">See also</span></span>



[<span data-ttu-id="c185d-134">Propiedad canónico PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="c185d-134">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="c185d-135">Propiedad canónico PidTagSelectable</span><span class="sxs-lookup"><span data-stu-id="c185d-135">PidTagSelectable Canonical Property</span></span>](pidtagselectable-canonical-property.md)


[<span data-ttu-id="c185d-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c185d-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c185d-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c185d-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c185d-138">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="c185d-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c185d-139">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c185d-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

