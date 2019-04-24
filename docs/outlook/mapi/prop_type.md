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
ms.openlocfilehash: 0c33633c4decd697cf241f8b7c27360f776a1ade
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332763"
---
# <a name="proptype"></a><span data-ttu-id="7b31f-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="7b31f-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="7b31f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b31f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b31f-105">Devuelve el tipo de propiedad de una etiqueta de propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="7b31f-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7b31f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7b31f-106">Header file:</span></span>  <br/> |<span data-ttu-id="7b31f-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7b31f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7b31f-108">Estructura relacionada:</span><span class="sxs-lookup"><span data-stu-id="7b31f-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="7b31f-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7b31f-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="7b31f-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="7b31f-110">Parameters</span></span>

 <span data-ttu-id="7b31f-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="7b31f-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="7b31f-112">Etiqueta de propiedad que contiene el tipo de propiedad que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="7b31f-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7b31f-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7b31f-113">Remarks</span></span>

<span data-ttu-id="7b31f-114">La macro **PROP_TYPE** se puede usar para determinar el tipo de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="7b31f-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="7b31f-115">Por ejemplo, llamar a PROP_TYPE\*\*\*\* (método ([PidTagEntryId](pidtagentryid-canonical-property.md))) da como resultado el valor PT_BINARY que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="7b31f-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="7b31f-116">Cada etiqueta de propiedad contiene el tipo de propiedad en la palabra de orden inferior (bits del 0 al 15) y el identificador de la propiedad en la palabra de orden superior (bits 16 a 31).</span><span class="sxs-lookup"><span data-stu-id="7b31f-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="7b31f-117">La macro **PROP_TYPE** extrae el tipo de propiedad y lo coloca en los bits del 0 al 15 del entero que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="7b31f-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="7b31f-118">Los bits restantes del valor devuelto se establecen en ceros.</span><span class="sxs-lookup"><span data-stu-id="7b31f-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7b31f-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b31f-119">See also</span></span>



[<span data-ttu-id="7b31f-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7b31f-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="7b31f-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="7b31f-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

