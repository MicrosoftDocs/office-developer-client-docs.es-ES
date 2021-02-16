---
title: BLEND (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Combina dos colores en la proporción especificada por el parámetro float.
ms.openlocfilehash: 0a231954370416be201183026424c79942204e12
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432789"
---
# <a name="blend-function"></a><span data-ttu-id="426de-103">Función BLEND</span><span class="sxs-lookup"><span data-stu-id="426de-103">BLEND Function</span></span>

<span data-ttu-id="426de-104">Combina dos colores en la proporción especificada por el _parámetro float._</span><span class="sxs-lookup"><span data-stu-id="426de-104">Blends two colors in the proportion specified by the  _float_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="426de-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="426de-105">Syntax</span></span>

<span data-ttu-id="426de-106">BLEND(\*\* *color1* \*\*, \*\* *color2* \*\*, \*\* *float[0,1]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="426de-106">BLEND(\*\* *color1* \*\*, \*\* *color2* \*\*, \*\* *float[0,1]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="426de-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="426de-107">Parameters</span></span>

|<span data-ttu-id="426de-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="426de-108">**Name**</span></span>|<span data-ttu-id="426de-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="426de-109">**Required/Optional**</span></span>|<span data-ttu-id="426de-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="426de-110">**Data Type**</span></span>|<span data-ttu-id="426de-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="426de-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="426de-112">_color1_</span><span class="sxs-lookup"><span data-stu-id="426de-112">_color1_</span></span> <br/> |<span data-ttu-id="426de-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="426de-113">Required</span></span>  <br/> |<span data-ttu-id="426de-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="426de-114">**Numeric**</span></span> <br/> |<span data-ttu-id="426de-115">Índice de color de Visio o valor RGB del primer color.</span><span class="sxs-lookup"><span data-stu-id="426de-115">The Visio color index or RGB value of the first color.</span></span>  <br/> |
| <span data-ttu-id="426de-116">_color2_</span><span class="sxs-lookup"><span data-stu-id="426de-116">_color2_</span></span> <br/> |<span data-ttu-id="426de-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="426de-117">Required</span></span>  <br/> |<span data-ttu-id="426de-118">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="426de-118">**Numeric**</span></span> <br/> |<span data-ttu-id="426de-119">Índice de color de Visio o valor RGB del segundo color.</span><span class="sxs-lookup"><span data-stu-id="426de-119">The Visio color index or RGB value of the second color.</span></span>  <br/> |
| <span data-ttu-id="426de-120">_float[0,1]_</span><span class="sxs-lookup"><span data-stu-id="426de-120">_float[0,1]_</span></span> <br/> |<span data-ttu-id="426de-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="426de-121">Required</span></span>  <br/> |<span data-ttu-id="426de-122">**Float**</span><span class="sxs-lookup"><span data-stu-id="426de-122">**Float**</span></span> <br/> |<span data-ttu-id="426de-123">Proporción en la que se combinan  _color2_ y  _color1,_ respectivamente.</span><span class="sxs-lookup"><span data-stu-id="426de-123">The proportion in which to blend  _color2_ and  _color1_, respectively.</span></span> <span data-ttu-id="426de-124">Número real entre 0 y 1, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="426de-124">A real number from 0 to 1 inclusive.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="426de-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="426de-125">Return value</span></span>

 <span data-ttu-id="426de-126">**RVA**</span><span class="sxs-lookup"><span data-stu-id="426de-126">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="426de-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="426de-127">Remarks</span></span>

<span data-ttu-id="426de-128">El color devuelto está determinado por las proporciones relativas en las que se combinan _color2_ y _color1,_ respectivamente, según lo especificado por el _parámetro float._</span><span class="sxs-lookup"><span data-stu-id="426de-128">The color returned is determined by the relative proportions in which to blend  _color2_ and  _color1_, respectively, as specified by the  _float_ parameter.</span></span> <span data-ttu-id="426de-129">Por ejemplo, si  _float_ es 0,25, el color devuelto se compone del 75 % del  _color1_ y el 25 % del  _color2_.</span><span class="sxs-lookup"><span data-stu-id="426de-129">For example, if  _float_ is 0.25, the color returned is composed 75% of  _color1_ and 25% of  _color2_.</span></span> 
  
<span data-ttu-id="426de-130">Otra forma de pensarlo es que el valor  _flotante_ corresponde al punto a lo largo del espectro de colores de  _color1_  _a color2_.</span><span class="sxs-lookup"><span data-stu-id="426de-130">Another way to think about it is that the  _float_ value corresponds to the point along the color spectrum from  _color1_ to  _color2_.</span></span> <span data-ttu-id="426de-131">Por lo tanto, los números  más pequeños (más cercanos a cero) para los resultados flotantes se fusionan más cerca del _color1,_ mientras que los números más grandes (más cercanos a 1) producen mezclas más cercanas a _color2_.</span><span class="sxs-lookup"><span data-stu-id="426de-131">Therefore, smaller numbers (closer to zero) for  _float_ produce blends closer to  _color1_, while larger numbers (closer to 1) produce blends closer to  _color2_.</span></span>
  

