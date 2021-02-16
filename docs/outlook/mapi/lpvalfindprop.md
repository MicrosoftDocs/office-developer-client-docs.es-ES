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
ms.openlocfilehash: fa1588d4a58824b57c132fc8e66a0abd6e9acd0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419642"
---
# <a name="lpvalfindprop"></a><span data-ttu-id="b56e4-103">LpValFindProp</span><span class="sxs-lookup"><span data-stu-id="b56e4-103">LpValFindProp</span></span>

  
  
<span data-ttu-id="b56e4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b56e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b56e4-105">Busca una propiedad especificada en un conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="b56e4-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b56e4-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b56e4-106">Header file:</span></span>  <br/> |<span data-ttu-id="b56e4-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b56e4-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b56e4-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="b56e4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b56e4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b56e4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b56e4-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="b56e4-110">Called by:</span></span>  <br/> |<span data-ttu-id="b56e4-111">Aplicaciones cliente y proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="b56e4-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="b56e4-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b56e4-112">Parameters</span></span>

 <span data-ttu-id="b56e4-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="b56e4-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="b56e4-114">[entrada] Etiqueta de la propiedad que se buscará en el conjunto de propiedades, indicada por el _parámetro lpPropArray._</span><span class="sxs-lookup"><span data-stu-id="b56e4-114">[in] Tag for the property to search for in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="b56e4-115">_cValues_</span><span class="sxs-lookup"><span data-stu-id="b56e4-115">_cValues_</span></span>
  
> <span data-ttu-id="b56e4-116">[entrada] Número de propiedades del conjunto de propiedades, indicado por el _parámetro lpPropArray._</span><span class="sxs-lookup"><span data-stu-id="b56e4-116">[in] Count of properties in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="b56e4-117">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="b56e4-117">_lpPropArray_</span></span>
  
> <span data-ttu-id="b56e4-118">[entrada] Matriz de **estructuras SPropValue** que define las propiedades que se buscarán.</span><span class="sxs-lookup"><span data-stu-id="b56e4-118">[in] Array of **SPropValue** structures that defines the properties to be searched.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b56e4-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b56e4-119">Return value</span></span>

<span data-ttu-id="b56e4-120">La **función LpValFindProp** devuelve una estructura **SPropValue** que define la propiedad que coincide con la etiqueta de propiedad de entrada, o NULL si no hay ninguna coincidencia.</span><span class="sxs-lookup"><span data-stu-id="b56e4-120">The **LpValFindProp** function returns an **SPropValue** structure that defines the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b56e4-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b56e4-121">Remarks</span></span>

<span data-ttu-id="b56e4-122">La **función LpValFindProp** es idéntica a **PpropFindProp**.</span><span class="sxs-lookup"><span data-stu-id="b56e4-122">The **LpValFindProp** function is identical to **PpropFindProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b56e4-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b56e4-123">See also</span></span>



[<span data-ttu-id="b56e4-124">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="b56e4-124">PpropFindProp</span></span>](ppropfindprop.md)
  
[<span data-ttu-id="b56e4-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b56e4-125">SPropValue</span></span>](spropvalue.md)

