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
ms.openlocfilehash: b2047f04f3f4a8d2b3e58e07a71e7e2463eff9cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344978"
---
# <a name="pidlidcategories-canonical-property"></a><span data-ttu-id="b6540-103">Propiedad canónica PidLidCategories</span><span class="sxs-lookup"><span data-stu-id="b6540-103">PidLidCategories Canonical Property</span></span>

  
  
<span data-ttu-id="b6540-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6540-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6540-105">Especifica una lista de categorías para un elemento.</span><span class="sxs-lookup"><span data-stu-id="b6540-105">Specifies a list of categories for an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b6540-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b6540-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b6540-107">dispidCategories</span><span class="sxs-lookup"><span data-stu-id="b6540-107">dispidCategories</span></span>  <br/> |
|<span data-ttu-id="b6540-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="b6540-108">Property set:</span></span>  <br/> |<span data-ttu-id="b6540-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="b6540-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="b6540-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="b6540-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b6540-111">0x00002328</span><span class="sxs-lookup"><span data-stu-id="b6540-111">0x00002328</span></span>  <br/> |
|<span data-ttu-id="b6540-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b6540-112">Data type:</span></span>  <br/> |<span data-ttu-id="b6540-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b6540-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b6540-114">Área:</span><span class="sxs-lookup"><span data-stu-id="b6540-114">Area:</span></span>  <br/> |<span data-ttu-id="b6540-115">Común</span><span class="sxs-lookup"><span data-stu-id="b6540-115">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6540-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b6540-116">Remarks</span></span>

<span data-ttu-id="b6540-117">Para generar un campo de encabezado de palabras clave, los clientes deben establecer el valor de esta propiedad en los valores deseados.</span><span class="sxs-lookup"><span data-stu-id="b6540-117">To generate a keywords header field, clients must set the value of this property to the desired values.</span></span> <span data-ttu-id="b6540-118">Esta propiedad tiene varias cadenas; cada categoría debe asignarse a una sola palabra clave.</span><span class="sxs-lookup"><span data-stu-id="b6540-118">This property has multiple strings; each category should be mapped to a single keyword.</span></span>
  
<span data-ttu-id="b6540-119">Los escritores de extensiones multipropósito de correo de Internet (MIME) deben copiar cada sub-valor de esta propiedad en una palabra clave independiente en el campo de encabezado Palabras clave, con una coma (U+002C) y un espacio (U+0020) que separa cada palabra clave.</span><span class="sxs-lookup"><span data-stu-id="b6540-119">Multipurpose Internet Mail Extensions (MIME) writers should copy each sub-value of this property to a separate keyword in the Keywords header field, with a comma (U+002C) and space (U+0020) separating each keyword.</span></span> <span data-ttu-id="b6540-120">Los escritores MIME pueden colocar esta propiedad en lugar de copiarla en el campo de encabezado de palabras clave, con el fin de evitar conflictos entre diferentes conjuntos de categorías en diferentes organizaciones.</span><span class="sxs-lookup"><span data-stu-id="b6540-120">MIME writers may drop this property instead of copying it to the keywords header field, in order to avoid conflict among different sets of categories in different organizations.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b6540-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6540-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b6540-122">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="b6540-122">Protocol specifications</span></span>

<span data-ttu-id="b6540-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6540-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6540-124">Proporciona la definición del conjunto de propiedades y las referencias a las Exchange Server de protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="b6540-124">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b6540-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6540-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6540-126">Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="b6540-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b6540-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b6540-127">Header files</span></span>

<span data-ttu-id="b6540-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b6540-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="b6540-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b6540-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b6540-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6540-130">See also</span></span>



[<span data-ttu-id="b6540-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b6540-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b6540-132">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="b6540-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b6540-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b6540-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b6540-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="b6540-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

