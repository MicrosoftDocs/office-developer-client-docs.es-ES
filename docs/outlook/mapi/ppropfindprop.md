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
ms.openlocfilehash: f720160193613bbbb4bbd447f78c14e6e5378eb8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565658"
---
# <a name="ppropfindprop"></a><span data-ttu-id="82756-103">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="82756-103">PpropFindProp</span></span>

  
  
<span data-ttu-id="82756-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82756-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82756-105">Establecer las búsquedas para una propiedad especificada en una propiedad.</span><span class="sxs-lookup"><span data-stu-id="82756-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="82756-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="82756-106">Header file:</span></span>  <br/> |<span data-ttu-id="82756-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="82756-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="82756-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="82756-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="82756-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="82756-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="82756-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="82756-110">Called by:</span></span>  <br/> |<span data-ttu-id="82756-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="82756-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="82756-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82756-112">Parameters</span></span>

 <span data-ttu-id="82756-113">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="82756-113">_rgprop_</span></span>
  
> <span data-ttu-id="82756-114">[entrada] Matriz de estructuras [SPropValue](spropvalue.md) que definen las propiedades que se desea buscar.</span><span class="sxs-lookup"><span data-stu-id="82756-114">[in] Array of [SPropValue](spropvalue.md) structures that define the properties to be searched.</span></span> 
    
 <span data-ttu-id="82756-115">_cprop_</span><span class="sxs-lookup"><span data-stu-id="82756-115">_cprop_</span></span>
  
> <span data-ttu-id="82756-116">[entrada] Recuento de propiedades en el conjunto de propiedades indicada por el parámetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="82756-116">[in] Count of properties in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="82756-117">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="82756-117">_ulPropTag_</span></span>
  
> <span data-ttu-id="82756-118">[entrada] Etiqueta de propiedad de la propiedad Buscar en el conjunto de propiedades indicado por el parámetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="82756-118">[in] Property tag for the property to search for in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="82756-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82756-119">Return value</span></span>

 <span data-ttu-id="82756-120">**PpropFindProp** devuelve una estructura [SPropValue](spropvalue.md) definición de la propiedad que coincide con la etiqueta de propiedad de entrada, o NULL si no hay ninguna coincidencia.</span><span class="sxs-lookup"><span data-stu-id="82756-120">**PpropFindProp** returns an [SPropValue](spropvalue.md) structure defining the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="82756-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="82756-121">Remarks</span></span>

<span data-ttu-id="82756-122">Si la etiqueta de propiedad determinada indica una propiedad de tipo PT_UNSPECIFIED, la función **PpropFindProp** busca a una coincidencia sólo para el identificador de la propiedad en la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="82756-122">If the given property tag indicates a property of type PT_UNSPECIFIED, the **PpropFindProp** function finds a match only for the property identifier in the tag.</span></span> <span data-ttu-id="82756-123">De lo contrario, busca a una coincidencia para la etiqueta de propiedad completa, incluido el tipo de propiedad y devuelve la propiedad identificada.</span><span class="sxs-lookup"><span data-stu-id="82756-123">Otherwise, it finds a match for the entire property tag, including the property type, and returns the property identified.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="82756-124">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="82756-124">MFCMAPI reference</span></span>

<span data-ttu-id="82756-125">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="82756-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="82756-126">**File**</span><span class="sxs-lookup"><span data-stu-id="82756-126">**File**</span></span>|<span data-ttu-id="82756-127">**Función**</span><span class="sxs-lookup"><span data-stu-id="82756-127">**Function**</span></span>|<span data-ttu-id="82756-128">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="82756-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="82756-129">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="82756-129">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="82756-130">CContentsTableListCtrl::BuildDataItem</span><span class="sxs-lookup"><span data-stu-id="82756-130">CContentsTableListCtrl::BuildDataItem</span></span>  <br/> |<span data-ttu-id="82756-131">MFCMAPI usa el método **PpropFindProp** para buscar establecer propiedades en una propiedad que se agrega a la lista.</span><span class="sxs-lookup"><span data-stu-id="82756-131">MFCMAPI uses the **PpropFindProp** method to find properties in a property set being added to the list.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82756-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="82756-132">See also</span></span>



[<span data-ttu-id="82756-133">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="82756-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

