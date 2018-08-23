---
title: FPropContainsProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropContainsProp
api_type:
- COM
ms.assetid: 43da5b59-7691-49aa-b83c-753d43bfd8fd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b08d3af8c61d8ced31e822bb787d49ad90b4df54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571678"
---
# <a name="fpropcontainsprop"></a><span data-ttu-id="e0722-103">FPropContainsProp</span><span class="sxs-lookup"><span data-stu-id="e0722-103">FPropContainsProp</span></span>

<span data-ttu-id="e0722-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0722-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0722-105">Compara dos valores de propiedad, por lo general cadenas o matrices binario, para ver si contiene uno del otro.</span><span class="sxs-lookup"><span data-stu-id="e0722-105">Compares two property values, generally strings or binary arrays, to see if one contains the other.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e0722-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e0722-106">Header file:</span></span>  <br/> |<span data-ttu-id="e0722-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e0722-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e0722-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="e0722-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e0722-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e0722-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e0722-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e0722-110">Called by:</span></span>  <br/> |<span data-ttu-id="e0722-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="e0722-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a><span data-ttu-id="e0722-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0722-112">Parameters</span></span>

<span data-ttu-id="e0722-113">_lpSPropValueDst_</span><span class="sxs-lookup"><span data-stu-id="e0722-113">_lpSPropValueDst_</span></span>
  
> <span data-ttu-id="e0722-114">[entrada] Puntero a una estructura [SPropValue](spropvalue.md) definir el valor de la propiedad que es posible que contienen la cadena de búsqueda que señala el parámetro _lpSPropValueSrc_ .</span><span class="sxs-lookup"><span data-stu-id="e0722-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property value that might contain the search string pointed to by the  _lpSPropValueSrc_ parameter.</span></span> 
    
<span data-ttu-id="e0722-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="e0722-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="e0722-116">[entrada] Puntero a una estructura **SPropValue** definición de la cadena de búsqueda que busca **FPropContainsProp** en el valor de la propiedad indicada por el parámetro _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="e0722-116">[in] Pointer to an **SPropValue** structure defining the search string that **FPropContainsProp** is seeking in the property value pointed to by the  _lpSPropValueDst_ parameter.</span></span> 
    
<span data-ttu-id="e0722-117">_ulFuzzyLevel_</span><span class="sxs-lookup"><span data-stu-id="e0722-117">_ulFuzzyLevel_</span></span>
  
> <span data-ttu-id="e0722-118">[entrada] Configuración de opción definir el nivel de precisión para usar en la comparación.</span><span class="sxs-lookup"><span data-stu-id="e0722-118">[in] Option settings defining the level of preciseness to use in the comparison.</span></span> 

  - <span data-ttu-id="e0722-119">Los **16 bits inferiores** se aplican a las propiedades de tipo PT_BINARY y PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="e0722-119">The **lower 16 bits** apply to properties of type PT_BINARY and PT_STRING8.</span></span> <span data-ttu-id="e0722-120">Debe establecer en exactamente uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="e0722-120">They must be set to exactly one of the following values:</span></span>
      
    - <span data-ttu-id="e0722-121">FL_FULLSTRING: La cadena de búsqueda _lpSPropValueSrc_ debe ser igual que el valor de la propiedad identificado por _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="e0722-121">FL_FULLSTRING: The  _lpSPropValueSrc_ search string must be equal to the property value identified by  _lpSPropValueDst_.</span></span>
        
    - <span data-ttu-id="e0722-122">FL_PREFIX: La cadena de búsqueda _lpSPropValueSrc_ debe aparecer al principio del valor de la propiedad identificado por _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="e0722-122">FL_PREFIX: The  _lpSPropValueSrc_ search string must appear at the beginning of the property value identified by  _lpSPropValueDst_.</span></span> <span data-ttu-id="e0722-123">Los dos valores se deben comparar sólo hasta la longitud de la cadena de búsqueda indicada por _lpSPropValueSrc_.</span><span class="sxs-lookup"><span data-stu-id="e0722-123">The two values should be compared only up to the length of the search string indicated by  _lpSPropValueSrc_.</span></span> 
        
    - <span data-ttu-id="e0722-124">FL_SUBSTRING: La cadena de búsqueda _lpSPropValueSrc_ debe estar incluida en cualquier lugar en el valor de la propiedad identificado por _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="e0722-124">FL_SUBSTRING: The  _lpSPropValueSrc_ search string must be contained anywhere in the property value identified by  _lpSPropValueDst_.</span></span> 
      
  - <span data-ttu-id="e0722-125">Los **16 bits superiores** se aplican sólo a las propiedades de tipo PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="e0722-125">The **upper 16 bits** apply only to properties of type PT_STRING8.</span></span> <span data-ttu-id="e0722-126">Se pueden establecer en los valores siguientes en cualquier combinación:</span><span class="sxs-lookup"><span data-stu-id="e0722-126">They can be set to the following values in any combination:</span></span>
    
    - <span data-ttu-id="e0722-127">FL_IGNORECASE: La comparación debe realizarse sin tener en cuenta entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e0722-127">FL_IGNORECASE: The comparison should be made without considering case sensitivity.</span></span> 
        
    - <span data-ttu-id="e0722-128">FL_IGNORENONSPACE: La comparación debe omitir caracteres sin espacios definidos por el Unicode como marcas diacríticas.</span><span class="sxs-lookup"><span data-stu-id="e0722-128">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined nonspacing characters such as diacritical marks.</span></span> 
        
    - <span data-ttu-id="e0722-129">FL_LOOSE: La comparación debería indicar una coincidencia siempre que sea posible, mayúsculas de minúsculas sensibilidad y caracteres sin espacios.</span><span class="sxs-lookup"><span data-stu-id="e0722-129">FL_LOOSE: The comparison should indicate a match whenever possible, ignoring case sensitivity and nonspacing characters.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e0722-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0722-130">Return value</span></span>

<span data-ttu-id="e0722-131">TRUE</span><span class="sxs-lookup"><span data-stu-id="e0722-131">TRUE</span></span> 
  
> <span data-ttu-id="e0722-132">Los parámetros son válidos y se encuentra la cadena de búsqueda _lpSPropValueSrc_ como se especifica en el valor de la propiedad _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="e0722-132">The parameters are all valid and the  _lpSPropValueSrc_ search string is contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
<span data-ttu-id="e0722-133">FALSE</span><span class="sxs-lookup"><span data-stu-id="e0722-133">FALSE</span></span> 
  
> <span data-ttu-id="e0722-134">Los valores de propiedad que se comparan no son de tipo PT_STRING8 o PT_BINARY, los valores de propiedad son de tipos diferentes, o no se encuentra la cadena de búsqueda _lpSPropValueSrc_ como se especifica en el valor de la propiedad _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="e0722-134">The property values being compared are not of type PT_STRING8 or PT_BINARY, the property values are of different types, or the  _lpSPropValueSrc_ search string is not contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e0722-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e0722-135">Remarks</span></span>

<span data-ttu-id="e0722-136">El método de comparación depende de los tipos de propiedad especificados en las definiciones de propiedad [SPropValue](spropvalue.md) y la heurística nivel aproximada proporcionada en el parámetro _ulFuzzyLevel_ .</span><span class="sxs-lookup"><span data-stu-id="e0722-136">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions and the fuzzy level heuristic provided in the  _ulFuzzyLevel_ parameter.</span></span> <span data-ttu-id="e0722-137">Las funciones [FPropCompareProp](fpropcompareprop.md) y **FPropContainsProp** se pueden usar para preparar las restricciones para generar una tabla.</span><span class="sxs-lookup"><span data-stu-id="e0722-137">The [FPropCompareProp](fpropcompareprop.md) and **FPropContainsProp** functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="e0722-138">Se omiten los 16 bits superiores de _ulFuzzyLevel_ para el tipo de propiedad PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="e0722-138">The upper 16 bits of  _ulFuzzyLevel_ are ignored for property type PT_BINARY.</span></span> <span data-ttu-id="e0722-139">Si la configuración de _ulFuzzyLevel_ está falta o no es válido, se realiza una coincidencia exacta de la cadena completa.</span><span class="sxs-lookup"><span data-stu-id="e0722-139">If the settings in  _ulFuzzyLevel_ are missing or invalid, a full-string exact match is performed.</span></span> <span data-ttu-id="e0722-140">Para obtener más información acerca de la contención de propiedad, vea la estructura [SContentRestriction](scontentrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="e0722-140">For more information about property containment, see the [SContentRestriction](scontentrestriction.md) structure.</span></span> 
  

