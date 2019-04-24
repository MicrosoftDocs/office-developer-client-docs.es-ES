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
ms.openlocfilehash: 228ea91969b35a1608dd6b3378b751312aa9c665
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328577"
---
# <a name="propid"></a><span data-ttu-id="43536-103">PROP_ID</span><span class="sxs-lookup"><span data-stu-id="43536-103">PROP_ID</span></span>

  
  
<span data-ttu-id="43536-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43536-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43536-105">Devuelve el identificador de la propiedad de una etiqueta de propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="43536-105">Returns the property identifier of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43536-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="43536-106">Header file:</span></span>  <br/> |<span data-ttu-id="43536-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="43536-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="43536-108">Estructura relacionada:</span><span class="sxs-lookup"><span data-stu-id="43536-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="43536-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="43536-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="43536-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="43536-110">Parameters</span></span>

 <span data-ttu-id="43536-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="43536-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="43536-112">Etiqueta de propiedad que contiene el identificador que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="43536-112">Property tag that contains the identifier to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="43536-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="43536-113">Remarks</span></span>

<span data-ttu-id="43536-114">Cada etiqueta de propiedad contiene el tipo de propiedad en la palabra de orden inferior (bits del 0 al 15) y el identificador de la propiedad en la palabra de orden superior (bits 16 a 31).</span><span class="sxs-lookup"><span data-stu-id="43536-114">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="43536-115">La macro **PROP_ID** extrae el identificador de la propiedad y lo coloca en los bits del 0 al 15 del entero que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="43536-115">The **PROP_ID** macro extracts the property identifier and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="43536-116">Los bits restantes del valor devuelto se establecen en ceros.</span><span class="sxs-lookup"><span data-stu-id="43536-116">The remaining bits of the return value are set to zeros.</span></span> 
  
<span data-ttu-id="43536-117">Se puede usar la macro **PROP_ID** , por ejemplo, para recuperar un identificador para pasar a [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="43536-117">The **PROP_ID** macro can be used, for example, to retrieve an identifier to pass to [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> <span data-ttu-id="43536-118">**GetNamesFromIDs** recupera el nombre de propiedad asociado a un identificador para una propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="43536-118">**GetNamesFromIDs** retrieves the property name associated with an identifier for a named property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="43536-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="43536-119">See also</span></span>



[<span data-ttu-id="43536-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="43536-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="43536-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="43536-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

