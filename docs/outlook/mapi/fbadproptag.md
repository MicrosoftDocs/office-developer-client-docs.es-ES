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
ms.openlocfilehash: 943dab0141581adc32c184b0042a063a4ec05c3e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582885"
---
# <a name="fbadproptag"></a><span data-ttu-id="bfa45-103">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="bfa45-103">FBadPropTag</span></span>

  
  
<span data-ttu-id="bfa45-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfa45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfa45-105">Valida una etiqueta de propiedad especificado.</span><span class="sxs-lookup"><span data-stu-id="bfa45-105">Validates a specified property tag.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bfa45-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="bfa45-106">Header file:</span></span>  <br/> |<span data-ttu-id="bfa45-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="bfa45-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="bfa45-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="bfa45-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bfa45-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bfa45-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bfa45-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="bfa45-110">Called by:</span></span>  <br/> |<span data-ttu-id="bfa45-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="bfa45-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="bfa45-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bfa45-112">Parameters</span></span>

 <span data-ttu-id="bfa45-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="bfa45-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="bfa45-114">[entrada] La etiqueta de propiedad que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="bfa45-114">[in] The property tag to be validated.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bfa45-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bfa45-115">Return value</span></span>

<span data-ttu-id="bfa45-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="bfa45-116">TRUE</span></span> 
  
> <span data-ttu-id="bfa45-117">La etiqueta de propiedad especificado no es una etiqueta de propiedad MAPI válida.</span><span class="sxs-lookup"><span data-stu-id="bfa45-117">The specified property tag is not a valid MAPI property tag.</span></span> 
    
<span data-ttu-id="bfa45-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="bfa45-118">FALSE</span></span> 
  
> <span data-ttu-id="bfa45-119">La etiqueta de la propiedad especificada es una etiqueta de propiedad MAPI válida.</span><span class="sxs-lookup"><span data-stu-id="bfa45-119">The specified property tag is a valid MAPI property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bfa45-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bfa45-120">Remarks</span></span>

<span data-ttu-id="bfa45-121">La función **FBadPropTag** valida la etiqueta de propiedad especificado en función de las definiciones de MAPI.</span><span class="sxs-lookup"><span data-stu-id="bfa45-121">The **FBadPropTag** function validates the specified property tag based on MAPI definitions.</span></span> <span data-ttu-id="bfa45-122">Asegúrese de que el tipo de propiedad es uno de los tipos definidos por MAPI y que se define el identificador de la propiedad para que sea de ese tipo de sures.</span><span class="sxs-lookup"><span data-stu-id="bfa45-122">It make sures that the property type is one of the types defined by MAPI and that the property identifier is defined to be of that type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bfa45-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfa45-123">See also</span></span>



[<span data-ttu-id="bfa45-124">FBadProp</span><span class="sxs-lookup"><span data-stu-id="bfa45-124">FBadProp</span></span>](fbadprop.md)

