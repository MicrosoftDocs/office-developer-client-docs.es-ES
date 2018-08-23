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
ms.openlocfilehash: e0f13b0b8d2f7eb6fd7ba60e9e351b62251aa13d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572840"
---
# <a name="pidtagprovideritemid-canonical-property"></a><span data-ttu-id="d437f-103">Propiedad canónica PidTagProviderItemId</span><span class="sxs-lookup"><span data-stu-id="d437f-103">PidTagProviderItemId Canonical Property</span></span>

  
  
<span data-ttu-id="d437f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d437f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d437f-105">Especifica un identificador para una carpeta o un elemento en un almacén.</span><span class="sxs-lookup"><span data-stu-id="d437f-105">Specifies an identifier for a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d437f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d437f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d437f-107">PR_PROVIDER_ITEMID</span><span class="sxs-lookup"><span data-stu-id="d437f-107">PR_PROVIDER_ITEMID</span></span>  <br/> |
|<span data-ttu-id="d437f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d437f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d437f-109">0x0EA3</span><span class="sxs-lookup"><span data-stu-id="d437f-109">0x0EA3</span></span>  <br/> |
|<span data-ttu-id="d437f-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d437f-110">Data type:</span></span>  <br/> |<span data-ttu-id="d437f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d437f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d437f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d437f-112">Area:</span></span>  <br/> |<span data-ttu-id="d437f-113">MapiNonTransmittable</span><span class="sxs-lookup"><span data-stu-id="d437f-113">MapiNonTransmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d437f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d437f-114">Remarks</span></span>

<span data-ttu-id="d437f-115">Los proveedores de almacén pueden especificar un valor para esta propiedad para una carpeta o un elemento, pero deben mantener el valor de la misma entre sesiones.</span><span class="sxs-lookup"><span data-stu-id="d437f-115">Store providers can specify a value for this property for a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="d437f-116">Los proveedores de almacén use esta propiedad para identificar los resultados de búsqueda devueltos por un motor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d437f-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d437f-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d437f-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d437f-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d437f-118">Header files</span></span>

<span data-ttu-id="d437f-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d437f-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="d437f-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d437f-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="d437f-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d437f-121">Mapitags.h</span></span>
  
> <span data-ttu-id="d437f-122">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d437f-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d437f-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d437f-123">See also</span></span>



[<span data-ttu-id="d437f-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d437f-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d437f-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d437f-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d437f-126">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d437f-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d437f-127">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d437f-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

