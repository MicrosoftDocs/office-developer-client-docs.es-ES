---
title: PROP_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_ID
api_type:
- COM
ms.assetid: 6ddaced5-49bb-41fe-95da-4e3300883bf7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ad4b9d3f7c2ca1766ecca4fe9467fc49098f2212
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820449"
---
# <a name="propid"></a><span data-ttu-id="7a48c-103">PROP_ID</span><span class="sxs-lookup"><span data-stu-id="7a48c-103">PROP_ID</span></span>

  
  
<span data-ttu-id="7a48c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7a48c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7a48c-105">Devuelve el identificador de propiedad de una etiqueta de propiedad especificado.</span><span class="sxs-lookup"><span data-stu-id="7a48c-105">Returns the property identifier of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7a48c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7a48c-106">Header file:</span></span>  <br/> |<span data-ttu-id="7a48c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a48c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7a48c-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="7a48c-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="7a48c-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7a48c-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="7a48c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a48c-110">Parameters</span></span>

 <span data-ttu-id="7a48c-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="7a48c-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="7a48c-112">Etiqueta de la propiedad que contiene el identificador que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="7a48c-112">Property tag that contains the identifier to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a48c-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7a48c-113">Remarks</span></span>

<span data-ttu-id="7a48c-114">Cada etiqueta de la propiedad contiene el tipo de propiedad de la palabra de orden inferior (bits del 0 al 15) y el identificador de propiedad de la palabra de orden superior (bits 16 a 31).</span><span class="sxs-lookup"><span data-stu-id="7a48c-114">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="7a48c-115">La macro **PROP_ID** extrae el identificador de propiedad y la coloca en los bits 0 a 15 del número entero que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="7a48c-115">The **PROP_ID** macro extracts the property identifier and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="7a48c-116">Se establecen los bits restantes del valor devuelto a ceros.</span><span class="sxs-lookup"><span data-stu-id="7a48c-116">The remaining bits of the return value are set to zeros.</span></span> 
  
<span data-ttu-id="7a48c-117">La macro **PROP_ID** , por ejemplo, puede usarse para recuperar un identificador que se pase a [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="7a48c-117">The **PROP_ID** macro can be used, for example, to retrieve an identifier to pass to [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> <span data-ttu-id="7a48c-118">**GetNamesFromIDs** recupera el nombre de propiedad asociado con un identificador para una propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="7a48c-118">**GetNamesFromIDs** retrieves the property name associated with an identifier for a named property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7a48c-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a48c-119">See also</span></span>



[<span data-ttu-id="7a48c-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7a48c-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="7a48c-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="7a48c-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

