---
title: PROP_TAG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TAG
api_type:
- COM
ms.assetid: d8c9d18c-4043-41f3-8501-8be8e3a2c9ac
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7ab4e4e9e51849037a91a071f16294cfdf10870c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425886"
---
# <a name="prop_tag"></a><span data-ttu-id="db1e5-103">PROP_TAG</span><span class="sxs-lookup"><span data-stu-id="db1e5-103">PROP_TAG</span></span>

<span data-ttu-id="db1e5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db1e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db1e5-105">Devuelve una etiqueta de propiedad creada mediante la combinación de un identificador y un tipo de propiedad especificados.</span><span class="sxs-lookup"><span data-stu-id="db1e5-105">Returns a property tag created by combining a specified property type and identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db1e5-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="db1e5-106">Header file:</span></span>  <br/> |<span data-ttu-id="db1e5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="db1e5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="db1e5-108">Estructura relacionada:</span><span class="sxs-lookup"><span data-stu-id="db1e5-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="db1e5-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="db1e5-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a><span data-ttu-id="db1e5-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db1e5-110">Parameters</span></span>

<span data-ttu-id="db1e5-111">_ulPropType_</span><span class="sxs-lookup"><span data-stu-id="db1e5-111">_ulPropType_</span></span>
  
> <span data-ttu-id="db1e5-112">Tipo de propiedad de la nueva etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="db1e5-112">Property type for the new property tag.</span></span>
    
<span data-ttu-id="db1e5-113">_ulPropID_</span><span class="sxs-lookup"><span data-stu-id="db1e5-113">_ulPropID_</span></span>
  
> <span data-ttu-id="db1e5-114">Identificador de propiedad de la nueva etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="db1e5-114">Property identifier for the new property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="db1e5-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="db1e5-115">Remarks</span></span>

<span data-ttu-id="db1e5-116">La macro **\_ PROP TAG** crea una etiqueta de propiedad para una propiedad de tipo  _ulPropType_ y el identificador especificado en  _ulPropID_.</span><span class="sxs-lookup"><span data-stu-id="db1e5-116">The **PROP\_TAG** macro creates a property tag for a property of type  _ulPropType_ and the identifier that is specified in  _ulPropID_.</span></span> <span data-ttu-id="db1e5-117">Por ejemplo, una etiqueta de propiedad para un identificador de entrada se puede crear mediante la macro **PROP_TAG** siguiente:</span><span class="sxs-lookup"><span data-stu-id="db1e5-117">For example, a property tag for an entry identifier can be created by using the **PROP_TAG** macro as follows:</span></span> 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

<span data-ttu-id="db1e5-118">Los 16 bits de orden bajo de la etiqueta de propiedad devuelta contienen el tipo de propiedad, PT_BINARY y los 16 bits de orden alto contienen el identificador de propiedad, 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="db1e5-118">The low-order 16 bits of the returned property tag contain the property type, PT_BINARY, and the high-order 16 bits contain the property identifier, 0xFFFF.</span></span>
  
<span data-ttu-id="db1e5-119">Para obtener más información acerca de las etiquetas de propiedad, vea [etiquetas de propiedad MAPI](mapi-property-tags.md).</span><span class="sxs-lookup"><span data-stu-id="db1e5-119">For more information about property tags, see [MAPI Property Tags](mapi-property-tags.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="db1e5-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="db1e5-120">See also</span></span>

- [<span data-ttu-id="db1e5-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="db1e5-121">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="db1e5-122">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="db1e5-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

