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
ms.openlocfilehash: ea56996ad56bb4ce93d103a75eba2c29e6059a87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328045"
---
# <a name="fpropcontainsprop"></a><span data-ttu-id="e058e-103">FPropContainsProp</span><span class="sxs-lookup"><span data-stu-id="e058e-103">FPropContainsProp</span></span>

<span data-ttu-id="e058e-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e058e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e058e-105">Compara dos valores de propiedad, generalmente cadenas o matrices binarias, para ver si uno contiene el otro.</span><span class="sxs-lookup"><span data-stu-id="e058e-105">Compares two property values, generally strings or binary arrays, to see if one contains the other.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e058e-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e058e-106">Header file:</span></span>  <br/> |<span data-ttu-id="e058e-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="e058e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e058e-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="e058e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e058e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e058e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e058e-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e058e-110">Called by:</span></span>  <br/> |<span data-ttu-id="e058e-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="e058e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a><span data-ttu-id="e058e-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e058e-112">Parameters</span></span>

<span data-ttu-id="e058e-113">_lpSPropValueDst_</span><span class="sxs-lookup"><span data-stu-id="e058e-113">_lpSPropValueDst_</span></span>
  
> <span data-ttu-id="e058e-114">a Puntero a una estructura [SPropValue](spropvalue.md) que define el valor de la propiedad que puede contener la cadena de búsqueda a la que apunta el parámetro _lpSPropValueSrc_ .</span><span class="sxs-lookup"><span data-stu-id="e058e-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property value that might contain the search string pointed to by the  _lpSPropValueSrc_ parameter.</span></span> 
    
<span data-ttu-id="e058e-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="e058e-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="e058e-116">a Puntero a una estructura **SPropValue** que define la cadena de búsqueda que **FPropContainsProp** busca en el valor de propiedad al que apunta el parámetro _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="e058e-116">[in] Pointer to an **SPropValue** structure defining the search string that **FPropContainsProp** is seeking in the property value pointed to by the  _lpSPropValueDst_ parameter.</span></span> 
    
<span data-ttu-id="e058e-117">_ulFuzzyLevel_</span><span class="sxs-lookup"><span data-stu-id="e058e-117">_ulFuzzyLevel_</span></span>
  
> <span data-ttu-id="e058e-118">a Opciones que definen el nivel de precisión que se debe usar en la comparación.</span><span class="sxs-lookup"><span data-stu-id="e058e-118">[in] Option settings defining the level of preciseness to use in the comparison.</span></span> 

  - <span data-ttu-id="e058e-119">Los **16 bits inferiores** se aplican a las propiedades del tipo PT_BINARY y PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="e058e-119">The **lower 16 bits** apply to properties of type PT_BINARY and PT_STRING8.</span></span> <span data-ttu-id="e058e-120">Se deben establecer exactamente en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="e058e-120">They must be set to exactly one of the following values:</span></span>
      
    - <span data-ttu-id="e058e-121">FL_FULLSTRING: la cadena de búsqueda _lpSPropValueSrc_ debe ser igual al valor de propiedad identificado por _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="e058e-121">FL_FULLSTRING: The  _lpSPropValueSrc_ search string must be equal to the property value identified by  _lpSPropValueDst_.</span></span>
        
    - <span data-ttu-id="e058e-122">FL_PREFIX: la cadena de búsqueda _lpSPropValueSrc_ debe aparecer al principio del valor de la propiedad identificado por _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="e058e-122">FL_PREFIX: The  _lpSPropValueSrc_ search string must appear at the beginning of the property value identified by  _lpSPropValueDst_.</span></span> <span data-ttu-id="e058e-123">Los dos valores deben compararse solamente hasta la longitud de la cadena de búsqueda indicada por _lpSPropValueSrc_.</span><span class="sxs-lookup"><span data-stu-id="e058e-123">The two values should be compared only up to the length of the search string indicated by  _lpSPropValueSrc_.</span></span> 
        
    - <span data-ttu-id="e058e-124">FL_SUBSTRING: la cadena de búsqueda _lpSPropValueSrc_ debe estar contenida en cualquier parte del valor de propiedad identificado por _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="e058e-124">FL_SUBSTRING: The  _lpSPropValueSrc_ search string must be contained anywhere in the property value identified by  _lpSPropValueDst_.</span></span> 
      
  - <span data-ttu-id="e058e-125">Los **16 bits superiores** solo se aplican a las propiedades de tipo PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="e058e-125">The **upper 16 bits** apply only to properties of type PT_STRING8.</span></span> <span data-ttu-id="e058e-126">Se pueden establecer en cualquier combinación de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="e058e-126">They can be set to the following values in any combination:</span></span>
    
    - <span data-ttu-id="e058e-127">FL_IGNORECASE: la comparación debe realizarse sin considerar la distinción entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e058e-127">FL_IGNORECASE: The comparison should be made without considering case sensitivity.</span></span> 
        
    - <span data-ttu-id="e058e-128">FL_IGNORENONSPACE: la comparación debe omitir los caracteres sin espaciado definidos en Unicode, como las marcas diacríticas.</span><span class="sxs-lookup"><span data-stu-id="e058e-128">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined nonspacing characters such as diacritical marks.</span></span> 
        
    - <span data-ttu-id="e058e-129">FL_LOOSE: la comparación debe indicar una coincidencia siempre que sea posible, ignorando la distinción entre mayúsculas y minúsculas y los caracteres sin espaciado.</span><span class="sxs-lookup"><span data-stu-id="e058e-129">FL_LOOSE: The comparison should indicate a match whenever possible, ignoring case sensitivity and nonspacing characters.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e058e-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e058e-130">Return value</span></span>

<span data-ttu-id="e058e-131">TRUE</span><span class="sxs-lookup"><span data-stu-id="e058e-131">TRUE</span></span> 
  
> <span data-ttu-id="e058e-132">Todos los parámetros son válidos y la cadena de búsqueda _lpSPropValueSrc_ se encuentra como se especifica en el valor de la propiedad _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="e058e-132">The parameters are all valid and the  _lpSPropValueSrc_ search string is contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
<span data-ttu-id="e058e-133">FALSE</span><span class="sxs-lookup"><span data-stu-id="e058e-133">FALSE</span></span> 
  
> <span data-ttu-id="e058e-134">Los valores de propiedad que se comparan no son del tipo PT_STRING8 o PT_BINARY, los valores de propiedad son de tipos diferentes o la cadena de búsqueda _lpSPropValueSrc_ no está incluida como se especifica en el valor de la propiedad _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="e058e-134">The property values being compared are not of type PT_STRING8 or PT_BINARY, the property values are of different types, or the  _lpSPropValueSrc_ search string is not contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e058e-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e058e-135">Remarks</span></span>

<span data-ttu-id="e058e-136">El método de comparación depende de los tipos de propiedad especificados en las definiciones de propiedad [SPropValue](spropvalue.md) y de la heurística de nivel aproximada proporcionada en el parámetro _ulFuzzyLevel_ .</span><span class="sxs-lookup"><span data-stu-id="e058e-136">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions and the fuzzy level heuristic provided in the  _ulFuzzyLevel_ parameter.</span></span> <span data-ttu-id="e058e-137">Las funciones [FPropCompareProp](fpropcompareprop.md) y **FPropContainsProp** se pueden usar para preparar restricciones para la generación de una tabla.</span><span class="sxs-lookup"><span data-stu-id="e058e-137">The [FPropCompareProp](fpropcompareprop.md) and **FPropContainsProp** functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="e058e-138">Los 16 bits superiores de _ulFuzzyLevel_ se omiten para el tipo de propiedad PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="e058e-138">The upper 16 bits of  _ulFuzzyLevel_ are ignored for property type PT_BINARY.</span></span> <span data-ttu-id="e058e-139">Si la configuración de _ulFuzzyLevel_ falta o no es válida, se realiza una coincidencia exacta de cadena completa.</span><span class="sxs-lookup"><span data-stu-id="e058e-139">If the settings in  _ulFuzzyLevel_ are missing or invalid, a full-string exact match is performed.</span></span> <span data-ttu-id="e058e-140">Para obtener más información acerca de la contención de propiedades, vea la estructura [SContentRestriction](scontentrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="e058e-140">For more information about property containment, see the [SContentRestriction](scontentrestriction.md) structure.</span></span> 
  

