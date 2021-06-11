---
title: PpropFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PpropFindProp
api_type:
- HeaderDef
ms.assetid: f23dd6f4-915b-4fe8-ab3f-6d625c7d6061
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 97021128f92af0486af1ba3125c7843eaa357648
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406342"
---
# <a name="ppropfindprop"></a><span data-ttu-id="72d20-103">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="72d20-103">PpropFindProp</span></span>

  
  
<span data-ttu-id="72d20-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72d20-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72d20-105">Busca una propiedad especificada en un conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="72d20-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="72d20-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="72d20-106">Header file:</span></span>  <br/> |<span data-ttu-id="72d20-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="72d20-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="72d20-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="72d20-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="72d20-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="72d20-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="72d20-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="72d20-110">Called by:</span></span>  <br/> |<span data-ttu-id="72d20-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="72d20-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="72d20-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="72d20-112">Parameters</span></span>

 <span data-ttu-id="72d20-113">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="72d20-113">_rgprop_</span></span>
  
> <span data-ttu-id="72d20-114">[in] Matriz de [estructuras SPropValue](spropvalue.md) que definen las propiedades que se buscarán.</span><span class="sxs-lookup"><span data-stu-id="72d20-114">[in] Array of [SPropValue](spropvalue.md) structures that define the properties to be searched.</span></span> 
    
 <span data-ttu-id="72d20-115">_cprop_</span><span class="sxs-lookup"><span data-stu-id="72d20-115">_cprop_</span></span>
  
> <span data-ttu-id="72d20-116">[in] Recuento de propiedades en el conjunto de propiedades indicado por el _parámetro rgprop._</span><span class="sxs-lookup"><span data-stu-id="72d20-116">[in] Count of properties in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="72d20-117">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="72d20-117">_ulPropTag_</span></span>
  
> <span data-ttu-id="72d20-118">[in] Etiqueta de propiedad para la propiedad que se debe buscar en el conjunto de propiedades indicado por el _parámetro rgprop._</span><span class="sxs-lookup"><span data-stu-id="72d20-118">[in] Property tag for the property to search for in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="72d20-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72d20-119">Return value</span></span>

 <span data-ttu-id="72d20-120">**PpropFindProp devuelve** una estructura [SPropValue](spropvalue.md) que define la propiedad que coincide con la etiqueta de propiedad de entrada o NULL si no hay coincidencia.</span><span class="sxs-lookup"><span data-stu-id="72d20-120">**PpropFindProp** returns an [SPropValue](spropvalue.md) structure defining the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="72d20-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="72d20-121">Remarks</span></span>

<span data-ttu-id="72d20-122">Si la etiqueta de propiedad determinada indica una propiedad de tipo PT_UNSPECIFIED, la función **PpropFindProp** solo encuentra una coincidencia para el identificador de propiedad de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="72d20-122">If the given property tag indicates a property of type PT_UNSPECIFIED, the **PpropFindProp** function finds a match only for the property identifier in the tag.</span></span> <span data-ttu-id="72d20-123">De lo contrario, busca una coincidencia para toda la etiqueta de propiedad, incluido el tipo de propiedad, y devuelve la propiedad identificada.</span><span class="sxs-lookup"><span data-stu-id="72d20-123">Otherwise, it finds a match for the entire property tag, including the property type, and returns the property identified.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="72d20-124">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="72d20-124">MFCMAPI reference</span></span>

<span data-ttu-id="72d20-125">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="72d20-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="72d20-126">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="72d20-126">**File**</span></span>|<span data-ttu-id="72d20-127">**Función**</span><span class="sxs-lookup"><span data-stu-id="72d20-127">**Function**</span></span>|<span data-ttu-id="72d20-128">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="72d20-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="72d20-129">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="72d20-129">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="72d20-130">CContentsTableListCtrl::BuildDataItem</span><span class="sxs-lookup"><span data-stu-id="72d20-130">CContentsTableListCtrl::BuildDataItem</span></span>  <br/> |<span data-ttu-id="72d20-131">MFCMAPI usa el **método PpropFindProp** para buscar propiedades en un conjunto de propiedades que se va a agregar a la lista.</span><span class="sxs-lookup"><span data-stu-id="72d20-131">MFCMAPI uses the **PpropFindProp** method to find properties in a property set being added to the list.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="72d20-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="72d20-132">See also</span></span>



[<span data-ttu-id="72d20-133">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="72d20-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

