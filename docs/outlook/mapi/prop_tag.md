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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 9e53c39b713aa782eb387b85667f5ded6193006f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820436"
---
# <a name="proptag"></a><span data-ttu-id="2ebfd-103">PROP_TAG</span><span class="sxs-lookup"><span data-stu-id="2ebfd-103">PROP_TAG</span></span>

<span data-ttu-id="2ebfd-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2ebfd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2ebfd-105">Devuelve una etiqueta de propiedad creada mediante la combinación de un tipo de propiedad especificado y un identificador.</span><span class="sxs-lookup"><span data-stu-id="2ebfd-105">Returns a property tag created by combining a specified property type and identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2ebfd-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="2ebfd-106">Header file:</span></span>  <br/> |<span data-ttu-id="2ebfd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ebfd-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2ebfd-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="2ebfd-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="2ebfd-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2ebfd-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a><span data-ttu-id="2ebfd-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ebfd-110">Parameters</span></span>

<span data-ttu-id="2ebfd-111">_ulPropType_</span><span class="sxs-lookup"><span data-stu-id="2ebfd-111">_ulPropType_</span></span>
  
> <span data-ttu-id="2ebfd-112">Tipo de propiedad para la nueva etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="2ebfd-112">Property type for the new property tag.</span></span>
    
<span data-ttu-id="2ebfd-113">_ulPropID_</span><span class="sxs-lookup"><span data-stu-id="2ebfd-113">_ulPropID_</span></span>
  
> <span data-ttu-id="2ebfd-114">Identificador de la propiedad para la nueva etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="2ebfd-114">Property identifier for the new property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2ebfd-115">Notas</span><span class="sxs-lookup"><span data-stu-id="2ebfd-115">Remarks</span></span>

<span data-ttu-id="2ebfd-116">El **propiedades\_etiqueta** macro crea una etiqueta de propiedad para una propiedad de tipo _ulPropType_ y el identificador que se especifica en _ulPropID_.</span><span class="sxs-lookup"><span data-stu-id="2ebfd-116">The **PROP\_TAG** macro creates a property tag for a property of type  _ulPropType_ and the identifier that is specified in  _ulPropID_.</span></span> <span data-ttu-id="2ebfd-117">Por ejemplo, se puede crear una etiqueta de propiedad para un identificador de entrada mediante la macro **PROP_TAG** como sigue:</span><span class="sxs-lookup"><span data-stu-id="2ebfd-117">For example, a property tag for an entry identifier can be created by using the **PROP_TAG** macro as follows:</span></span> 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

<span data-ttu-id="2ebfd-118">Los 16 bits de orden inferior de la etiqueta de propiedad devuelto contienen el tipo de propiedad, PT_BINARY, y los 16 bits de orden superior contienen el identificador de propiedad, 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="2ebfd-118">The low-order 16 bits of the returned property tag contain the property type, PT_BINARY, and the high-order 16 bits contain the property identifier, 0xFFFF.</span></span>
  
<span data-ttu-id="2ebfd-119">Para obtener más información acerca de las etiquetas de propiedad, vea [Etiquetas de propiedad MAPI](mapi-property-tags.md).</span><span class="sxs-lookup"><span data-stu-id="2ebfd-119">For more information about property tags, see [MAPI Property Tags](mapi-property-tags.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2ebfd-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="2ebfd-120">See also</span></span>

- [<span data-ttu-id="2ebfd-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2ebfd-121">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="2ebfd-122">Macros relacionadas con las estructuras</span><span class="sxs-lookup"><span data-stu-id="2ebfd-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

