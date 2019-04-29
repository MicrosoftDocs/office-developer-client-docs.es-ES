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
# <a name="fbadproptag"></a><span data-ttu-id="1d652-103">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="1d652-103">FBadPropTag</span></span>

  
  
<span data-ttu-id="1d652-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d652-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d652-105">Valida una etiqueta de propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="1d652-105">Validates a specified property tag.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1d652-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1d652-106">Header file:</span></span>  <br/> |<span data-ttu-id="1d652-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="1d652-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="1d652-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="1d652-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1d652-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1d652-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1d652-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="1d652-110">Called by:</span></span>  <br/> |<span data-ttu-id="1d652-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="1d652-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="1d652-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d652-112">Parameters</span></span>

 <span data-ttu-id="1d652-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="1d652-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="1d652-114">a Etiqueta de propiedad que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="1d652-114">[in] The property tag to be validated.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1d652-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d652-115">Return value</span></span>

<span data-ttu-id="1d652-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="1d652-116">TRUE</span></span> 
  
> <span data-ttu-id="1d652-117">La etiqueta de propiedad especificada no es una etiqueta de propiedad MAPI válida.</span><span class="sxs-lookup"><span data-stu-id="1d652-117">The specified property tag is not a valid MAPI property tag.</span></span> 
    
<span data-ttu-id="1d652-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="1d652-118">FALSE</span></span> 
  
> <span data-ttu-id="1d652-119">La etiqueta de propiedad especificada es una etiqueta de propiedad MAPI válida.</span><span class="sxs-lookup"><span data-stu-id="1d652-119">The specified property tag is a valid MAPI property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1d652-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1d652-120">Remarks</span></span>

<span data-ttu-id="1d652-121">La función **FBadPropTag** valida la etiqueta de propiedad especificada basándose en las definiciones de MAPI.</span><span class="sxs-lookup"><span data-stu-id="1d652-121">The **FBadPropTag** function validates the specified property tag based on MAPI definitions.</span></span> <span data-ttu-id="1d652-122">Asegura que el tipo de propiedad es uno de los tipos definidos por MAPI y que el identificador de la propiedad se define para que sea de ese tipo.</span><span class="sxs-lookup"><span data-stu-id="1d652-122">It make sures that the property type is one of the types defined by MAPI and that the property identifier is defined to be of that type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1d652-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="1d652-123">See also</span></span>



[<span data-ttu-id="1d652-124">FBadProp</span><span class="sxs-lookup"><span data-stu-id="1d652-124">FBadProp</span></span>](fbadprop.md)

