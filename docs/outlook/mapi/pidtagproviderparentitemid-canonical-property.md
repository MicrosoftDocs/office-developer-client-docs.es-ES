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
ms.openlocfilehash: d0ec4e793a5b7940802ee159c2e869695166ce93
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563285"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a><span data-ttu-id="17f5e-103">Propiedad canónica PidTagProviderParentItemId</span><span class="sxs-lookup"><span data-stu-id="17f5e-103">PidTagProviderParentItemId Canonical Property</span></span>

  
  
<span data-ttu-id="17f5e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17f5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17f5e-105">Especifica un identificador para el elemento principal de una carpeta o un elemento en un almacén.</span><span class="sxs-lookup"><span data-stu-id="17f5e-105">Specifies an identifier for the parent of a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="17f5e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="17f5e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="17f5e-107">PR_PROVIDER_PARENT_ITEMID</span><span class="sxs-lookup"><span data-stu-id="17f5e-107">PR_PROVIDER_PARENT_ITEMID</span></span>  <br/> |
|<span data-ttu-id="17f5e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="17f5e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="17f5e-109">0x0EA4</span><span class="sxs-lookup"><span data-stu-id="17f5e-109">0x0EA4</span></span>  <br/> |
|<span data-ttu-id="17f5e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="17f5e-110">Data type:</span></span>  <br/> |<span data-ttu-id="17f5e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="17f5e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="17f5e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="17f5e-112">Area:</span></span>  <br/> |<span data-ttu-id="17f5e-113">MAPI no transmisible</span><span class="sxs-lookup"><span data-stu-id="17f5e-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17f5e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="17f5e-114">Remarks</span></span>

<span data-ttu-id="17f5e-115">Los proveedores de almacén pueden especificar un valor para esta propiedad para un elemento principal de una carpeta o un elemento, pero deben mantener el valor de la misma entre sesiones.</span><span class="sxs-lookup"><span data-stu-id="17f5e-115">Store providers can specify a value for this property for a parent of a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="17f5e-116">Los proveedores de almacén use esta propiedad para identificar los resultados de búsqueda devueltos por un motor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="17f5e-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="17f5e-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="17f5e-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="17f5e-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="17f5e-118">Header files</span></span>

<span data-ttu-id="17f5e-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="17f5e-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="17f5e-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="17f5e-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="17f5e-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="17f5e-121">Mapitags.h</span></span>
  
> <span data-ttu-id="17f5e-122">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="17f5e-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="17f5e-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="17f5e-123">See also</span></span>



[<span data-ttu-id="17f5e-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="17f5e-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="17f5e-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="17f5e-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="17f5e-126">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="17f5e-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="17f5e-127">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="17f5e-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

