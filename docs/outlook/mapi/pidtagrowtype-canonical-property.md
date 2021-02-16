---
title: Propiedad canónica PidTagRowType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowType
api_type:
- COM
ms.assetid: d57ce5c8-1f60-4709-b86a-4468c4208dfe
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 962e8c92ae61e8b60862a3ae26a7cdfbf5034e89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359517"
---
# <a name="pidtagrowtype-canonical-property"></a><span data-ttu-id="f6343-103">Propiedad canónica PidTagRowType</span><span class="sxs-lookup"><span data-stu-id="f6343-103">PidTagRowType Canonical Property</span></span>

  
  
<span data-ttu-id="f6343-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6343-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6343-105">Contiene un valor que indica el tipo de una fila de una tabla.</span><span class="sxs-lookup"><span data-stu-id="f6343-105">Contains a value that indicates the type of a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f6343-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f6343-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f6343-107">PR_ROW_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6343-107">PR_ROW_TYPE</span></span>  <br/> |
|<span data-ttu-id="f6343-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f6343-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f6343-109">0x0FF5</span><span class="sxs-lookup"><span data-stu-id="f6343-109">0x0FF5</span></span>  <br/> |
|<span data-ttu-id="f6343-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f6343-110">Data type:</span></span>  <br/> |<span data-ttu-id="f6343-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f6343-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f6343-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f6343-112">Area:</span></span>  <br/> |<span data-ttu-id="f6343-113">MAPI no transmitible</span><span class="sxs-lookup"><span data-stu-id="f6343-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6343-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f6343-114">Remarks</span></span>

<span data-ttu-id="f6343-115">Esta propiedad solo aparece en las tablas de contenido.</span><span class="sxs-lookup"><span data-stu-id="f6343-115">This property appears only on contents tables.</span></span> <span data-ttu-id="f6343-116">Una categoría solo existe cuando tiene elementos.</span><span class="sxs-lookup"><span data-stu-id="f6343-116">A category only exists when it has items.</span></span>
  
<span data-ttu-id="f6343-117">Esta propiedad puede tener exactamente uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="f6343-117">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="f6343-118">TBL_LEAF_ROW</span><span class="sxs-lookup"><span data-stu-id="f6343-118">TBL_LEAF_ROW</span></span> 
  
> <span data-ttu-id="f6343-119">Representa datos reales, en lugar de una fila de categoría.</span><span class="sxs-lookup"><span data-stu-id="f6343-119">Represents actual data, rather than a category row.</span></span>
    
<span data-ttu-id="f6343-120">TBL_EMPTY_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="f6343-120">TBL_EMPTY_CATEGORY</span></span> 
  
> <span data-ttu-id="f6343-121">No se usa actualmente.</span><span class="sxs-lookup"><span data-stu-id="f6343-121">Not currently used.</span></span>
    
<span data-ttu-id="f6343-122">TBL_EXPANDED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="f6343-122">TBL_EXPANDED_CATEGORY</span></span> 
  
> <span data-ttu-id="f6343-123">La categoría se expande; La interfaz de usuario normalmente muestra esto con el signo menos ( - ) al lado.</span><span class="sxs-lookup"><span data-stu-id="f6343-123">The category is expanded; the user interface usually displays this with the minus sign ( - ) next to it.</span></span>
    
<span data-ttu-id="f6343-124">TBL_COLLAPSED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="f6343-124">TBL_COLLAPSED_CATEGORY</span></span> 
  
> <span data-ttu-id="f6343-125">La categoría está contrayda; La interfaz de usuario normalmente muestra esto con el signo más (+) junto a él.</span><span class="sxs-lookup"><span data-stu-id="f6343-125">The category is collapsed; the user interface usually displays this with the plus sign (+) next to it.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="f6343-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f6343-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f6343-127">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="f6343-127">Protocol specifications</span></span>

<span data-ttu-id="f6343-128">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f6343-128">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f6343-129">Incluye operaciones permitidas para los objetos de tabla principales.</span><span class="sxs-lookup"><span data-stu-id="f6343-129">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f6343-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f6343-130">Header files</span></span>

<span data-ttu-id="f6343-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f6343-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="f6343-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f6343-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="f6343-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f6343-133">Mapitags.h</span></span>
  
> <span data-ttu-id="f6343-134">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f6343-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f6343-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f6343-135">See also</span></span>



[<span data-ttu-id="f6343-136">Propiedad canónica PidTagRowid</span><span class="sxs-lookup"><span data-stu-id="f6343-136">PidTagRowid Canonical Property</span></span>](pidtagrowid-canonical-property.md)


[<span data-ttu-id="f6343-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f6343-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f6343-138">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="f6343-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f6343-139">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f6343-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f6343-140">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="f6343-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

