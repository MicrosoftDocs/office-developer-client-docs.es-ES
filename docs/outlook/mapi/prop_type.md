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
ms.openlocfilehash: 91a9d15544ebc71d27c8a9a6f930f3c32ecaa4fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820438"
---
# <a name="proptype"></a><span data-ttu-id="1677d-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="1677d-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="1677d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1677d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1677d-105">Devuelve el tipo de propiedad de una etiqueta de propiedad especificado.</span><span class="sxs-lookup"><span data-stu-id="1677d-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1677d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1677d-106">Header file:</span></span>  <br/> |<span data-ttu-id="1677d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1677d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1677d-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="1677d-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="1677d-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1677d-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="1677d-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1677d-110">Parameters</span></span>

 <span data-ttu-id="1677d-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="1677d-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="1677d-112">Etiqueta de la propiedad que contiene el tipo de propiedad que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="1677d-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1677d-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1677d-113">Remarks</span></span>

<span data-ttu-id="1677d-114">La macro **PROP_TYPE** se puede usar para determinar el tipo de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="1677d-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="1677d-115">Por ejemplo, al llamar a los resultados de la PROP_TYPE (**entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))) en el valor PT_BINARY que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="1677d-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="1677d-116">Cada etiqueta de la propiedad contiene el tipo de propiedad de la palabra de orden inferior (bits del 0 al 15) y el identificador de propiedad de la palabra de orden superior (bits 16 a 31).</span><span class="sxs-lookup"><span data-stu-id="1677d-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="1677d-117">La macro **PROP_TYPE** extrae el tipo de propiedad y la coloca en los bits 0 a 15 del número entero que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="1677d-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="1677d-118">Se establecen los bits restantes del valor devuelto a ceros.</span><span class="sxs-lookup"><span data-stu-id="1677d-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1677d-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="1677d-119">See also</span></span>



[<span data-ttu-id="1677d-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1677d-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="1677d-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="1677d-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

