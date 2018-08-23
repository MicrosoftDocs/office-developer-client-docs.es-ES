---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c4a201411e2232a3e5fdcd97dcbc9460f657b12a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578097"
---
# <a name="lpvalfindprop"></a><span data-ttu-id="19980-103">LpValFindProp</span><span class="sxs-lookup"><span data-stu-id="19980-103">LpValFindProp</span></span>

  
  
<span data-ttu-id="19980-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19980-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19980-105">Establecer las búsquedas para una propiedad especificada en una propiedad.</span><span class="sxs-lookup"><span data-stu-id="19980-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="19980-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="19980-106">Header file:</span></span>  <br/> |<span data-ttu-id="19980-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="19980-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="19980-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="19980-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="19980-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="19980-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="19980-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="19980-110">Called by:</span></span>  <br/> |<span data-ttu-id="19980-111">Las aplicaciones de cliente y los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="19980-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="19980-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19980-112">Parameters</span></span>

 <span data-ttu-id="19980-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="19980-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="19980-114">[entrada] Etiqueta de la propiedad Buscar en el conjunto de propiedades, indicado por el parámetro _lpPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="19980-114">[in] Tag for the property to search for in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="19980-115">_cValues_</span><span class="sxs-lookup"><span data-stu-id="19980-115">_cValues_</span></span>
  
> <span data-ttu-id="19980-116">[entrada] Recuento de propiedades en el conjunto de propiedades, indicada por el parámetro _lpPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="19980-116">[in] Count of properties in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="19980-117">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="19980-117">_lpPropArray_</span></span>
  
> <span data-ttu-id="19980-118">[entrada] Matriz de estructuras **SPropValue** que define las propiedades que se desea buscar.</span><span class="sxs-lookup"><span data-stu-id="19980-118">[in] Array of **SPropValue** structures that defines the properties to be searched.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="19980-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19980-119">Return value</span></span>

<span data-ttu-id="19980-120">La función **LpValFindProp** devuelve una estructura **SPropValue** que define la propiedad que coincide con la etiqueta de propiedad de entrada, o NULL si no hay ninguna coincidencia.</span><span class="sxs-lookup"><span data-stu-id="19980-120">The **LpValFindProp** function returns an **SPropValue** structure that defines the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="19980-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="19980-121">Remarks</span></span>

<span data-ttu-id="19980-122">La función **LpValFindProp** es idéntica a **PpropFindProp**.</span><span class="sxs-lookup"><span data-stu-id="19980-122">The **LpValFindProp** function is identical to **PpropFindProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="19980-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="19980-123">See also</span></span>



[<span data-ttu-id="19980-124">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="19980-124">PpropFindProp</span></span>](ppropfindprop.md)
  
[<span data-ttu-id="19980-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="19980-125">SPropValue</span></span>](spropvalue.md)

