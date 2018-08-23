---
title: PROP_TYPE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TYPE
api_type:
- COM
ms.assetid: 746d63fa-bfb7-479f-94dc-ba40011c1ec9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7bcaf230eed9cf21388b68f06ab678dc143f64ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571825"
---
# <a name="proptype"></a><span data-ttu-id="7d9c6-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="7d9c6-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="7d9c6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d9c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d9c6-105">Devuelve el tipo de propiedad de una etiqueta de propiedad especificado.</span><span class="sxs-lookup"><span data-stu-id="7d9c6-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7d9c6-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7d9c6-106">Header file:</span></span>  <br/> |<span data-ttu-id="7d9c6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7d9c6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7d9c6-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="7d9c6-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="7d9c6-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7d9c6-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="7d9c6-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d9c6-110">Parameters</span></span>

 <span data-ttu-id="7d9c6-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="7d9c6-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="7d9c6-112">Etiqueta de la propiedad que contiene el tipo de propiedad que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="7d9c6-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d9c6-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7d9c6-113">Remarks</span></span>

<span data-ttu-id="7d9c6-114">La macro **PROP_TYPE** se puede usar para determinar el tipo de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="7d9c6-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="7d9c6-115">Por ejemplo, al llamar a los resultados de la PROP_TYPE (**entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))) en el valor PT_BINARY que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="7d9c6-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="7d9c6-116">Cada etiqueta de la propiedad contiene el tipo de propiedad de la palabra de orden inferior (bits del 0 al 15) y el identificador de propiedad de la palabra de orden superior (bits 16 a 31).</span><span class="sxs-lookup"><span data-stu-id="7d9c6-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="7d9c6-117">La macro **PROP_TYPE** extrae el tipo de propiedad y la coloca en los bits 0 a 15 del número entero que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="7d9c6-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="7d9c6-118">Se establecen los bits restantes del valor devuelto a ceros.</span><span class="sxs-lookup"><span data-stu-id="7d9c6-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7d9c6-119">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="7d9c6-119">See also</span></span>



[<span data-ttu-id="7d9c6-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7d9c6-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="7d9c6-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="7d9c6-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

