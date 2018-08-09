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
ms.openlocfilehash: b7755f2ec067003e47d358a9736c6d7d96ede267
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820450"
---
# <a name="ppropfindprop"></a><span data-ttu-id="7dc22-103">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="7dc22-103">PpropFindProp</span></span>

  
  
<span data-ttu-id="7dc22-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7dc22-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7dc22-105">Establecer las búsquedas para una propiedad especificada en una propiedad.</span><span class="sxs-lookup"><span data-stu-id="7dc22-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7dc22-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7dc22-106">Header file:</span></span>  <br/> |<span data-ttu-id="7dc22-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7dc22-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7dc22-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="7dc22-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7dc22-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7dc22-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7dc22-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="7dc22-110">Called by:</span></span>  <br/> |<span data-ttu-id="7dc22-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="7dc22-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="7dc22-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7dc22-112">Parameters</span></span>

 <span data-ttu-id="7dc22-113">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="7dc22-113">_rgprop_</span></span>
  
> <span data-ttu-id="7dc22-114">[entrada] Matriz de estructuras [SPropValue](spropvalue.md) que definen las propiedades que se desea buscar.</span><span class="sxs-lookup"><span data-stu-id="7dc22-114">[in] Array of [SPropValue](spropvalue.md) structures that define the properties to be searched.</span></span> 
    
 <span data-ttu-id="7dc22-115">_cprop_</span><span class="sxs-lookup"><span data-stu-id="7dc22-115">_cprop_</span></span>
  
> <span data-ttu-id="7dc22-116">[entrada] Recuento de propiedades en el conjunto de propiedades indicada por el parámetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="7dc22-116">[in] Count of properties in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="7dc22-117">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="7dc22-117">_ulPropTag_</span></span>
  
> <span data-ttu-id="7dc22-118">[entrada] Etiqueta de propiedad de la propiedad Buscar en el conjunto de propiedades indicado por el parámetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="7dc22-118">[in] Property tag for the property to search for in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7dc22-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7dc22-119">Return value</span></span>

 <span data-ttu-id="7dc22-120">**PpropFindProp** devuelve una estructura [SPropValue](spropvalue.md) definición de la propiedad que coincide con la etiqueta de propiedad de entrada, o NULL si no hay ninguna coincidencia.</span><span class="sxs-lookup"><span data-stu-id="7dc22-120">**PpropFindProp** returns an [SPropValue](spropvalue.md) structure defining the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7dc22-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7dc22-121">Remarks</span></span>

<span data-ttu-id="7dc22-122">Si la etiqueta de propiedad determinada indica una propiedad de tipo PT_UNSPECIFIED, la función **PpropFindProp** busca a una coincidencia sólo para el identificador de la propiedad en la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="7dc22-122">If the given property tag indicates a property of type PT_UNSPECIFIED, the **PpropFindProp** function finds a match only for the property identifier in the tag.</span></span> <span data-ttu-id="7dc22-123">De lo contrario, busca a una coincidencia para la etiqueta de propiedad completa, incluido el tipo de propiedad y devuelve la propiedad identificada.</span><span class="sxs-lookup"><span data-stu-id="7dc22-123">Otherwise, it finds a match for the entire property tag, including the property type, and returns the property identified.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7dc22-124">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7dc22-124">MFCMAPI reference</span></span>

<span data-ttu-id="7dc22-125">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="7dc22-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7dc22-126">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="7dc22-126">**File**</span></span>|<span data-ttu-id="7dc22-127">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="7dc22-127">**Function**</span></span>|<span data-ttu-id="7dc22-128">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="7dc22-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7dc22-129">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="7dc22-129">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="7dc22-130">CContentsTableListCtrl::BuildDataItem</span><span class="sxs-lookup"><span data-stu-id="7dc22-130">CContentsTableListCtrl::BuildDataItem</span></span>  <br/> |<span data-ttu-id="7dc22-131">MFCMAPI usa el método **PpropFindProp** para buscar establecer propiedades en una propiedad que se agrega a la lista.</span><span class="sxs-lookup"><span data-stu-id="7dc22-131">MFCMAPI uses the **PpropFindProp** method to find properties in a property set being added to the list.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7dc22-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="7dc22-132">See also</span></span>



[<span data-ttu-id="7dc22-133">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="7dc22-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

