---
title: Propiedad canónica PidLidCategories
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCategories
api_type:
- COM
ms.assetid: 6ad2aedc-405b-475e-ac76-7ecbbef28f73
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 01d4391850067d00645b5c0248e1bf858c2a9049
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818594"
---
# <a name="pidlidcategories-canonical-property"></a><span data-ttu-id="0e140-103">Propiedad canónica PidLidCategories</span><span class="sxs-lookup"><span data-stu-id="0e140-103">PidLidCategories Canonical Property</span></span>

  
  
<span data-ttu-id="0e140-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0e140-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0e140-105">Especifica una lista de categorías para un elemento.</span><span class="sxs-lookup"><span data-stu-id="0e140-105">Specifies a list of categories for an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e140-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0e140-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0e140-107">dispidCategories</span><span class="sxs-lookup"><span data-stu-id="0e140-107">dispidCategories</span></span>  <br/> |
|<span data-ttu-id="0e140-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="0e140-108">Property set:</span></span>  <br/> |<span data-ttu-id="0e140-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="0e140-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="0e140-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="0e140-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0e140-111">0x00002328</span><span class="sxs-lookup"><span data-stu-id="0e140-111">0x00002328</span></span>  <br/> |
|<span data-ttu-id="0e140-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0e140-112">Data type:</span></span>  <br/> |<span data-ttu-id="0e140-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0e140-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0e140-114">Área:</span><span class="sxs-lookup"><span data-stu-id="0e140-114">Area:</span></span>  <br/> |<span data-ttu-id="0e140-115">Common</span><span class="sxs-lookup"><span data-stu-id="0e140-115">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e140-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0e140-116">Remarks</span></span>

<span data-ttu-id="0e140-117">Para generar un campo de encabezado de palabras clave, los clientes deben establecer el valor de esta propiedad en los valores deseados.</span><span class="sxs-lookup"><span data-stu-id="0e140-117">To generate a keywords header field, clients must set the value of this property to the desired values.</span></span> <span data-ttu-id="0e140-118">Esta propiedad tiene varias cadenas; cada categoría se debe asignar a una palabra clave única.</span><span class="sxs-lookup"><span data-stu-id="0e140-118">This property has multiple strings; each category should be mapped to a single keyword.</span></span>
  
<span data-ttu-id="0e140-119">Extensiones multipropósito escritores de extensiones de correo Internet (MIME) deben copiar cada valor subcaracterística de esta propiedad para una palabra clave independiente en el campo de encabezado de palabras clave, con una coma (U + 002 C) y espacio (u+0020) separando cada palabra clave.</span><span class="sxs-lookup"><span data-stu-id="0e140-119">Multipurpose Internet Mail Extensions (MIME) writers should copy each sub-value of this property to a separate keyword in the Keywords header field, with a comma (U+002C) and space (U+0020) separating each keyword.</span></span> <span data-ttu-id="0e140-120">Los escritores MIME pueden colocar esta propiedad en lugar de copiarlo en el campo de encabezado de palabras clave, con el fin de evitar conflictos entre distintos conjuntos de categorías de distintas organizaciones.</span><span class="sxs-lookup"><span data-stu-id="0e140-120">MIME writers may drop this property instead of copying it to the keywords header field, in order to avoid conflict among different sets of categories in different organizations.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0e140-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e140-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0e140-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0e140-122">Protocol specifications</span></span>

<span data-ttu-id="0e140-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e140-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e140-124">Proporciona la definición del conjunto de propiedad y referencias a las especificaciones de protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0e140-124">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0e140-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e140-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e140-126">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="0e140-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0e140-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0e140-127">Header files</span></span>

<span data-ttu-id="0e140-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e140-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="0e140-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0e140-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0e140-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e140-130">See also</span></span>



[<span data-ttu-id="0e140-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0e140-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0e140-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="0e140-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0e140-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0e140-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0e140-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="0e140-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

