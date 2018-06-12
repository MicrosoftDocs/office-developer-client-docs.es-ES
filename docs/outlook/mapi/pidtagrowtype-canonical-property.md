---
title: Propiedad canónico PidTagRowType
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 7fdb8781c39d7814ff2c38ff4df4545511d28a5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820132"
---
# <a name="pidtagrowtype-canonical-property"></a><span data-ttu-id="9a049-103">Propiedad canónico PidTagRowType</span><span class="sxs-lookup"><span data-stu-id="9a049-103">PidTagRowType Canonical Property</span></span>

  
  
<span data-ttu-id="9a049-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9a049-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9a049-105">Contiene un valor que indica el tipo de una fila de una tabla.</span><span class="sxs-lookup"><span data-stu-id="9a049-105">Contains a value that indicates the type of a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9a049-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9a049-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9a049-107">PR_ROW_TYPE</span><span class="sxs-lookup"><span data-stu-id="9a049-107">PR_ROW_TYPE</span></span>  <br/> |
|<span data-ttu-id="9a049-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9a049-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9a049-109">0x0FF5</span><span class="sxs-lookup"><span data-stu-id="9a049-109">0x0FF5</span></span>  <br/> |
|<span data-ttu-id="9a049-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9a049-110">Data type:</span></span>  <br/> |<span data-ttu-id="9a049-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9a049-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9a049-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9a049-112">Area:</span></span>  <br/> |<span data-ttu-id="9a049-113">MAPI no transmisible</span><span class="sxs-lookup"><span data-stu-id="9a049-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a049-114">Notas</span><span class="sxs-lookup"><span data-stu-id="9a049-114">Remarks</span></span>

<span data-ttu-id="9a049-115">Esta propiedad sólo aparece en las tablas de contenido.</span><span class="sxs-lookup"><span data-stu-id="9a049-115">This property appears only on contents tables.</span></span> <span data-ttu-id="9a049-116">Sólo existe una categoría cuando tiene elementos.</span><span class="sxs-lookup"><span data-stu-id="9a049-116">A category only exists when it has items.</span></span>
  
<span data-ttu-id="9a049-117">Esta propiedad puede tener exactamente uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="9a049-117">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="9a049-118">TBL_LEAF_ROW</span><span class="sxs-lookup"><span data-stu-id="9a049-118">TBL_LEAF_ROW</span></span> 
  
> <span data-ttu-id="9a049-119">Representa los datos reales, en lugar de una fila de la categoría.</span><span class="sxs-lookup"><span data-stu-id="9a049-119">Represents actual data, rather than a category row.</span></span>
    
<span data-ttu-id="9a049-120">TBL_EMPTY_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="9a049-120">TBL_EMPTY_CATEGORY</span></span> 
  
> <span data-ttu-id="9a049-121">Actualmente no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9a049-121">Not currently used.</span></span>
    
<span data-ttu-id="9a049-122">TBL_EXPANDED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="9a049-122">TBL_EXPANDED_CATEGORY</span></span> 
  
> <span data-ttu-id="9a049-123">La categoría se expande; la interfaz de usuario normalmente muestra esto con el signo menos (-) junto a ella.</span><span class="sxs-lookup"><span data-stu-id="9a049-123">The category is expanded; the user interface usually displays this with the minus sign ( - ) next to it.</span></span>
    
<span data-ttu-id="9a049-124">TBL_COLLAPSED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="9a049-124">TBL_COLLAPSED_CATEGORY</span></span> 
  
> <span data-ttu-id="9a049-125">La categoría está contraída; la interfaz de usuario normalmente muestra esto con el signo más (+) situado junto a él.</span><span class="sxs-lookup"><span data-stu-id="9a049-125">The category is collapsed; the user interface usually displays this with the plus sign (+) next to it.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="9a049-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9a049-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9a049-127">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="9a049-127">Protocol specifications</span></span>

<span data-ttu-id="9a049-128">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9a049-128">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9a049-129">Incluye las operaciones permitidas para los objetos de la tabla principal.</span><span class="sxs-lookup"><span data-stu-id="9a049-129">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9a049-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9a049-130">Header files</span></span>

<span data-ttu-id="9a049-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9a049-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="9a049-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9a049-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="9a049-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9a049-133">Mapitags.h</span></span>
  
> <span data-ttu-id="9a049-134">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="9a049-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9a049-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="9a049-135">See also</span></span>



[<span data-ttu-id="9a049-136">Propiedad canónico PidTagRowid</span><span class="sxs-lookup"><span data-stu-id="9a049-136">PidTagRowid Canonical Property</span></span>](pidtagrowid-canonical-property.md)


[<span data-ttu-id="9a049-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9a049-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9a049-138">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="9a049-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9a049-139">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="9a049-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9a049-140">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9a049-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

