---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: d7601eb50818fa6f39384a6b024215fc4917e83a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818035"
---
# <a name="lpvalfindprop"></a><span data-ttu-id="21aef-103">LpValFindProp</span><span class="sxs-lookup"><span data-stu-id="21aef-103">LpValFindProp</span></span>

  
  
<span data-ttu-id="21aef-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="21aef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="21aef-105">Establecer las búsquedas para una propiedad especificada en una propiedad.</span><span class="sxs-lookup"><span data-stu-id="21aef-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="21aef-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="21aef-106">Header file:</span></span>  <br/> |<span data-ttu-id="21aef-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="21aef-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="21aef-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="21aef-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="21aef-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="21aef-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="21aef-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="21aef-110">Called by:</span></span>  <br/> |<span data-ttu-id="21aef-111">Las aplicaciones de cliente y los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="21aef-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="21aef-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21aef-112">Parameters</span></span>

 <span data-ttu-id="21aef-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="21aef-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="21aef-114">[entrada] Etiqueta de la propiedad Buscar en el conjunto de propiedades, indicado por el parámetro _lpPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="21aef-114">[in] Tag for the property to search for in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="21aef-115">_cValues_</span><span class="sxs-lookup"><span data-stu-id="21aef-115">_cValues_</span></span>
  
> <span data-ttu-id="21aef-116">[entrada] Recuento de propiedades en el conjunto de propiedades, indicada por el parámetro _lpPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="21aef-116">[in] Count of properties in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="21aef-117">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="21aef-117">_lpPropArray_</span></span>
  
> <span data-ttu-id="21aef-118">[entrada] Matriz de estructuras **SPropValue** que define las propiedades que se desea buscar.</span><span class="sxs-lookup"><span data-stu-id="21aef-118">[in] Array of **SPropValue** structures that defines the properties to be searched.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="21aef-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21aef-119">Return value</span></span>

<span data-ttu-id="21aef-120">La función **LpValFindProp** devuelve una estructura **SPropValue** que define la propiedad que coincide con la etiqueta de propiedad de entrada, o NULL si no hay ninguna coincidencia.</span><span class="sxs-lookup"><span data-stu-id="21aef-120">The **LpValFindProp** function returns an **SPropValue** structure that defines the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="21aef-121">Notas</span><span class="sxs-lookup"><span data-stu-id="21aef-121">Remarks</span></span>

<span data-ttu-id="21aef-122">La función **LpValFindProp** es idéntica a **PpropFindProp**.</span><span class="sxs-lookup"><span data-stu-id="21aef-122">The **LpValFindProp** function is identical to **PpropFindProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="21aef-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="21aef-123">See also</span></span>



[<span data-ttu-id="21aef-124">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="21aef-124">PpropFindProp</span></span>](ppropfindprop.md)
  
[<span data-ttu-id="21aef-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="21aef-125">SPropValue</span></span>](spropvalue.md)

