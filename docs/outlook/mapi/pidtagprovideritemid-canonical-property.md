---
title: Propiedad canónica PidTagProviderItemId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderItemId
api_type:
- COM
ms.assetid: fadbf1af-32c2-43ea-8475-15b31b2a9e68
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 35a2d88ec838a9a76355ba6580e9cdbb3f28de56
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819989"
---
# <a name="pidtagprovideritemid-canonical-property"></a><span data-ttu-id="bf749-103">Propiedad canónica PidTagProviderItemId</span><span class="sxs-lookup"><span data-stu-id="bf749-103">PidTagProviderItemId Canonical Property</span></span>

  
  
<span data-ttu-id="bf749-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bf749-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bf749-105">Especifica un identificador para una carpeta o un elemento en un almacén.</span><span class="sxs-lookup"><span data-stu-id="bf749-105">Specifies an identifier for a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf749-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="bf749-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bf749-107">PR_PROVIDER_ITEMID</span><span class="sxs-lookup"><span data-stu-id="bf749-107">PR_PROVIDER_ITEMID</span></span>  <br/> |
|<span data-ttu-id="bf749-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="bf749-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bf749-109">0x0EA3</span><span class="sxs-lookup"><span data-stu-id="bf749-109">0x0EA3</span></span>  <br/> |
|<span data-ttu-id="bf749-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="bf749-110">Data type:</span></span>  <br/> |<span data-ttu-id="bf749-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bf749-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bf749-112">Área:</span><span class="sxs-lookup"><span data-stu-id="bf749-112">Area:</span></span>  <br/> |<span data-ttu-id="bf749-113">MapiNonTransmittable</span><span class="sxs-lookup"><span data-stu-id="bf749-113">MapiNonTransmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf749-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf749-114">Remarks</span></span>

<span data-ttu-id="bf749-115">Los proveedores de almacén pueden especificar un valor para esta propiedad para una carpeta o un elemento, pero deben mantener el valor de la misma entre sesiones.</span><span class="sxs-lookup"><span data-stu-id="bf749-115">Store providers can specify a value for this property for a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="bf749-116">Los proveedores de almacén use esta propiedad para identificar los resultados de búsqueda devueltos por un motor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="bf749-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bf749-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf749-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bf749-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="bf749-118">Header files</span></span>

<span data-ttu-id="bf749-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bf749-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="bf749-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="bf749-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="bf749-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bf749-121">Mapitags.h</span></span>
  
> <span data-ttu-id="bf749-122">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="bf749-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf749-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf749-123">See also</span></span>



[<span data-ttu-id="bf749-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bf749-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bf749-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="bf749-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bf749-126">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="bf749-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bf749-127">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="bf749-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

