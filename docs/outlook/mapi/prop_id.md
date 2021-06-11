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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409135"
---
# <a name="prop_id"></a><span data-ttu-id="70e3e-103">PROP_ID</span><span class="sxs-lookup"><span data-stu-id="70e3e-103">PROP_ID</span></span>

  
  
<span data-ttu-id="70e3e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70e3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70e3e-105">Devuelve el identificador de propiedad de una etiqueta de propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="70e3e-105">Returns the property identifier of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70e3e-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="70e3e-106">Header file:</span></span>  <br/> |<span data-ttu-id="70e3e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="70e3e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="70e3e-108">Estructura relacionada:</span><span class="sxs-lookup"><span data-stu-id="70e3e-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="70e3e-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="70e3e-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="70e3e-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="70e3e-110">Parameters</span></span>

 <span data-ttu-id="70e3e-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="70e3e-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="70e3e-112">Etiqueta de propiedad que contiene el identificador que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="70e3e-112">Property tag that contains the identifier to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="70e3e-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="70e3e-113">Remarks</span></span>

<span data-ttu-id="70e3e-114">Cada etiqueta de propiedad contiene el tipo de propiedad en la palabra de orden bajo (bits 0 a 15) y el identificador de propiedad en la palabra de orden alto (bits 16 a 31).</span><span class="sxs-lookup"><span data-stu-id="70e3e-114">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="70e3e-115">La **PROP_ID** extrae el identificador de propiedad y lo coloca en los bits 0 a 15 del entero que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="70e3e-115">The **PROP_ID** macro extracts the property identifier and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="70e3e-116">Los bits restantes del valor devuelto se establecen en ceros.</span><span class="sxs-lookup"><span data-stu-id="70e3e-116">The remaining bits of the return value are set to zeros.</span></span> 
  
<span data-ttu-id="70e3e-117">La **PROP_ID** puede usarse, por ejemplo, para recuperar un identificador para pasarlo a [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="70e3e-117">The **PROP_ID** macro can be used, for example, to retrieve an identifier to pass to [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> <span data-ttu-id="70e3e-118">**GetNamesFromIDs** recupera el nombre de propiedad asociado a un identificador de una propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="70e3e-118">**GetNamesFromIDs** retrieves the property name associated with an identifier for a named property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="70e3e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="70e3e-119">See also</span></span>



[<span data-ttu-id="70e3e-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="70e3e-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="70e3e-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="70e3e-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

