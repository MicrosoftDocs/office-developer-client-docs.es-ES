---
title: Propiedad canónico PidTagProviderParentItemId
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 96a9d153fadbe8b4c8baa8532b8c99771b1d7987
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819964"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a><span data-ttu-id="1c3a5-103">Propiedad canónico PidTagProviderParentItemId</span><span class="sxs-lookup"><span data-stu-id="1c3a5-103">PidTagProviderParentItemId Canonical Property</span></span>

  
  
<span data-ttu-id="1c3a5-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1c3a5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1c3a5-105">Especifica un identificador para el elemento principal de una carpeta o un elemento en un almacén.</span><span class="sxs-lookup"><span data-stu-id="1c3a5-105">Specifies an identifier for the parent of a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1c3a5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1c3a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1c3a5-107">PR_PROVIDER_PARENT_ITEMID</span><span class="sxs-lookup"><span data-stu-id="1c3a5-107">PR_PROVIDER_PARENT_ITEMID</span></span>  <br/> |
|<span data-ttu-id="1c3a5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1c3a5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1c3a5-109">0x0EA4</span><span class="sxs-lookup"><span data-stu-id="1c3a5-109">0x0EA4</span></span>  <br/> |
|<span data-ttu-id="1c3a5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1c3a5-110">Data type:</span></span>  <br/> |<span data-ttu-id="1c3a5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1c3a5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1c3a5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1c3a5-112">Area:</span></span>  <br/> |<span data-ttu-id="1c3a5-113">MAPI no transmisible</span><span class="sxs-lookup"><span data-stu-id="1c3a5-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c3a5-114">Notas</span><span class="sxs-lookup"><span data-stu-id="1c3a5-114">Remarks</span></span>

<span data-ttu-id="1c3a5-115">Los proveedores de almacén pueden especificar un valor para esta propiedad para un elemento principal de una carpeta o un elemento, pero deben mantener el valor de la misma entre sesiones.</span><span class="sxs-lookup"><span data-stu-id="1c3a5-115">Store providers can specify a value for this property for a parent of a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="1c3a5-116">Los proveedores de almacén use esta propiedad para identificar los resultados de búsqueda devueltos por un motor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1c3a5-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1c3a5-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1c3a5-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1c3a5-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1c3a5-118">Header files</span></span>

<span data-ttu-id="1c3a5-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1c3a5-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="1c3a5-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1c3a5-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="1c3a5-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1c3a5-121">Mapitags.h</span></span>
  
> <span data-ttu-id="1c3a5-122">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="1c3a5-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1c3a5-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="1c3a5-123">See also</span></span>



[<span data-ttu-id="1c3a5-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1c3a5-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1c3a5-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="1c3a5-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1c3a5-126">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="1c3a5-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1c3a5-127">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="1c3a5-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

