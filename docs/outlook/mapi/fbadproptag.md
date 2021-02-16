---
title: FBadPropTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadPropTag
api_type:
- HeaderDef
ms.assetid: 143bd3c6-5a55-4122-8522-9c48473aa781
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9764be2788db8d2649be8708cad4ec67a85af845
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433650"
---
# <a name="fbadproptag"></a><span data-ttu-id="9dd0f-103">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="9dd0f-103">FBadPropTag</span></span>

  
  
<span data-ttu-id="9dd0f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9dd0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9dd0f-105">Valida una etiqueta de propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="9dd0f-105">Validates a specified property tag.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9dd0f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9dd0f-106">Header file:</span></span>  <br/> |<span data-ttu-id="9dd0f-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="9dd0f-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="9dd0f-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="9dd0f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9dd0f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9dd0f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9dd0f-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="9dd0f-110">Called by:</span></span>  <br/> |<span data-ttu-id="9dd0f-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="9dd0f-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="9dd0f-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9dd0f-112">Parameters</span></span>

 <span data-ttu-id="9dd0f-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="9dd0f-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="9dd0f-114">[entrada] Etiqueta de propiedad que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="9dd0f-114">[in] The property tag to be validated.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9dd0f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9dd0f-115">Return value</span></span>

<span data-ttu-id="9dd0f-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="9dd0f-116">TRUE</span></span> 
  
> <span data-ttu-id="9dd0f-117">La etiqueta de propiedad especificada no es una etiqueta de propiedad MAPI válida.</span><span class="sxs-lookup"><span data-stu-id="9dd0f-117">The specified property tag is not a valid MAPI property tag.</span></span> 
    
<span data-ttu-id="9dd0f-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="9dd0f-118">FALSE</span></span> 
  
> <span data-ttu-id="9dd0f-119">La etiqueta de propiedad especificada es una etiqueta de propiedad MAPI válida.</span><span class="sxs-lookup"><span data-stu-id="9dd0f-119">The specified property tag is a valid MAPI property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9dd0f-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9dd0f-120">Remarks</span></span>

<span data-ttu-id="9dd0f-121">La **función FBadPropTag** valida la etiqueta de propiedad especificada en función de las definiciones MAPI.</span><span class="sxs-lookup"><span data-stu-id="9dd0f-121">The **FBadPropTag** function validates the specified property tag based on MAPI definitions.</span></span> <span data-ttu-id="9dd0f-122">Se asegura de que el tipo de propiedad es uno de los tipos definidos por MAPI y que el identificador de propiedad está definido para ser de ese tipo.</span><span class="sxs-lookup"><span data-stu-id="9dd0f-122">It make sures that the property type is one of the types defined by MAPI and that the property identifier is defined to be of that type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9dd0f-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9dd0f-123">See also</span></span>



[<span data-ttu-id="9dd0f-124">FBadProp</span><span class="sxs-lookup"><span data-stu-id="9dd0f-124">FBadProp</span></span>](fbadprop.md)

