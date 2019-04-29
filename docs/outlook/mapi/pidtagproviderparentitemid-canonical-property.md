---
title: Propiedad canónica PidTagProviderParentItemId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderParentItemId
api_type:
- COM
ms.assetid: 6adb8e85-ae56-4542-8b19-ed3cfe7fe522
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0f99cf38e65c75ce1ba74bf72d88e19f4fbfa03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433419"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a><span data-ttu-id="c27d6-103">Propiedad canónica PidTagProviderParentItemId</span><span class="sxs-lookup"><span data-stu-id="c27d6-103">PidTagProviderParentItemId Canonical Property</span></span>

  
  
<span data-ttu-id="c27d6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c27d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c27d6-105">Especifica un identificador para el elemento primario de una carpeta o un elemento en un almacén.</span><span class="sxs-lookup"><span data-stu-id="c27d6-105">Specifies an identifier for the parent of a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c27d6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c27d6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c27d6-107">PR_PROVIDER_PARENT_ITEMID</span><span class="sxs-lookup"><span data-stu-id="c27d6-107">PR_PROVIDER_PARENT_ITEMID</span></span>  <br/> |
|<span data-ttu-id="c27d6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c27d6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c27d6-109">0x0EA4</span><span class="sxs-lookup"><span data-stu-id="c27d6-109">0x0EA4</span></span>  <br/> |
|<span data-ttu-id="c27d6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c27d6-110">Data type:</span></span>  <br/> |<span data-ttu-id="c27d6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c27d6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c27d6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c27d6-112">Area:</span></span>  <br/> |<span data-ttu-id="c27d6-113">MAPI no transmitible</span><span class="sxs-lookup"><span data-stu-id="c27d6-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c27d6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c27d6-114">Remarks</span></span>

<span data-ttu-id="c27d6-115">Los proveedores de almacén pueden especificar un valor para esta propiedad para un elemento primario de una carpeta o un elemento, pero deben mantener el valor igual entre sesiones.</span><span class="sxs-lookup"><span data-stu-id="c27d6-115">Store providers can specify a value for this property for a parent of a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="c27d6-116">Los proveedores de almacenamiento usan esta propiedad para identificar los resultados de la búsqueda que devuelve un motor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c27d6-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c27d6-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c27d6-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c27d6-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c27d6-118">Header files</span></span>

<span data-ttu-id="c27d6-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c27d6-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="c27d6-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c27d6-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="c27d6-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="c27d6-121">Mapitags.h</span></span>
  
> <span data-ttu-id="c27d6-122">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c27d6-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c27d6-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="c27d6-123">See also</span></span>



[<span data-ttu-id="c27d6-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c27d6-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c27d6-125">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="c27d6-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c27d6-126">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c27d6-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c27d6-127">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="c27d6-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

