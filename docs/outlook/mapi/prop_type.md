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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412838"
---
# <a name="prop_type"></a><span data-ttu-id="01d2c-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="01d2c-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="01d2c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01d2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01d2c-105">Devuelve el tipo de propiedad de una etiqueta de propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="01d2c-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="01d2c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="01d2c-106">Header file:</span></span>  <br/> |<span data-ttu-id="01d2c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="01d2c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="01d2c-108">Estructura relacionada:</span><span class="sxs-lookup"><span data-stu-id="01d2c-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="01d2c-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="01d2c-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="01d2c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01d2c-110">Parameters</span></span>

 <span data-ttu-id="01d2c-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="01d2c-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="01d2c-112">Etiqueta de propiedad que contiene el tipo de propiedad que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="01d2c-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="01d2c-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="01d2c-113">Remarks</span></span>

<span data-ttu-id="01d2c-114">La **PROP_TYPE** macro puede usarse para determinar el tipo de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="01d2c-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="01d2c-115">Por ejemplo, al llamar PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) se devuelve el valor PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="01d2c-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="01d2c-116">Cada etiqueta de propiedad contiene el tipo de propiedad en la palabra de orden bajo (bits 0 a 15) y el identificador de propiedad en la palabra de orden alto (bits 16 a 31).</span><span class="sxs-lookup"><span data-stu-id="01d2c-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="01d2c-117">La **PROP_TYPE** macro extrae el tipo de propiedad y la coloca en bits del 0 al 15 del entero que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="01d2c-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="01d2c-118">Los bits restantes del valor devuelto se establecen en ceros.</span><span class="sxs-lookup"><span data-stu-id="01d2c-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="01d2c-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="01d2c-119">See also</span></span>



[<span data-ttu-id="01d2c-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="01d2c-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="01d2c-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="01d2c-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

