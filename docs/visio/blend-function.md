---
title: BLEND (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Mezcla dos colores en la proporción especificada por el parámetro float.
ms.openlocfilehash: 61993cea9eed6583d62004e1c756368b67c7bb33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821653"
---
# <a name="blend-function"></a><span data-ttu-id="a8ad4-103">Función BLEND</span><span class="sxs-lookup"><span data-stu-id="a8ad4-103">BLEND Function</span></span>

<span data-ttu-id="a8ad4-104">Mezcla dos colores en la proporción especificada por el parámetro _float_ .</span><span class="sxs-lookup"><span data-stu-id="a8ad4-104">Blends two colors in the proportion specified by the  _float_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a8ad4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8ad4-105">Syntax</span></span>

<span data-ttu-id="a8ad4-106">BLEND (** *color1* **, ** *color2* **, ** *float [0,1]* **)</span><span class="sxs-lookup"><span data-stu-id="a8ad4-106">BLEND(** *color1* **, ** *color2* **, ** *float[0,1]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a8ad4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8ad4-107">Parameters</span></span>

|<span data-ttu-id="a8ad4-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a8ad4-108">**Name**</span></span>|<span data-ttu-id="a8ad4-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="a8ad4-109">**Required/Optional**</span></span>|<span data-ttu-id="a8ad4-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="a8ad4-110">**Data Type**</span></span>|<span data-ttu-id="a8ad4-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a8ad4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a8ad4-112">_color1_</span><span class="sxs-lookup"><span data-stu-id="a8ad4-112">_color1_</span></span> <br/> |<span data-ttu-id="a8ad4-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a8ad4-113">Required</span></span>  <br/> |<span data-ttu-id="a8ad4-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="a8ad4-114">**Numeric**</span></span> <br/> |<span data-ttu-id="a8ad4-115">Índice de color de Visio o valor RGB del primer color.</span><span class="sxs-lookup"><span data-stu-id="a8ad4-115">The Visio color index or RGB value of the first color.</span></span>  <br/> |
| <span data-ttu-id="a8ad4-116">_color2_</span><span class="sxs-lookup"><span data-stu-id="a8ad4-116">_color2_</span></span> <br/> |<span data-ttu-id="a8ad4-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a8ad4-117">Required</span></span>  <br/> |<span data-ttu-id="a8ad4-118">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="a8ad4-118">**Numeric**</span></span> <br/> |<span data-ttu-id="a8ad4-119">Índice de color de Visio o valor RGB del segundo color.</span><span class="sxs-lookup"><span data-stu-id="a8ad4-119">The Visio color index or RGB value of the second color.</span></span>  <br/> |
| <span data-ttu-id="a8ad4-120">_float [0,1]_</span><span class="sxs-lookup"><span data-stu-id="a8ad4-120">_float[0,1]_</span></span> <br/> |<span data-ttu-id="a8ad4-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a8ad4-121">Required</span></span>  <br/> |<span data-ttu-id="a8ad4-122">**Float**</span><span class="sxs-lookup"><span data-stu-id="a8ad4-122">**Float**</span></span> <br/> |<span data-ttu-id="a8ad4-123">Proporción en la que se va a fusionar _color2_ y _color1_, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a8ad4-123">The proportion in which to blend  _color2_ and  _color1_, respectively.</span></span> <span data-ttu-id="a8ad4-124">Un número real de 0 a 1, inclusive.</span><span class="sxs-lookup"><span data-stu-id="a8ad4-124">A real number from 0 to 1 inclusive.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a8ad4-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8ad4-125">Return value</span></span>

 <span data-ttu-id="a8ad4-126">**RVA**</span><span class="sxs-lookup"><span data-stu-id="a8ad4-126">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8ad4-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a8ad4-127">Remarks</span></span>

<span data-ttu-id="a8ad4-128">El color devuelto viene determinado por las proporciones relativas en las que se va a fusionar _color2_ y _color1_, respectivamente, como especificado por el parámetro _float_ .</span><span class="sxs-lookup"><span data-stu-id="a8ad4-128">The color returned is determined by the relative proportions in which to blend  _color2_ and  _color1_, respectively, as specified by the  _float_ parameter.</span></span> <span data-ttu-id="a8ad4-129">Por ejemplo, si _float_ es 0,25, el color devuelto está compuesta por un 75% de _color1_ y 25% de _color2_.</span><span class="sxs-lookup"><span data-stu-id="a8ad4-129">For example, if  _float_ is 0.25, the color returned is composed 75% of  _color1_ and 25% of  _color2_.</span></span> 
  
<span data-ttu-id="a8ad4-130">Otra forma de tener en cuenta es que el valor _float_ se corresponde con el punto a lo largo del espectro de color desde _color1_ a _color2_.</span><span class="sxs-lookup"><span data-stu-id="a8ad4-130">Another way to think about it is that the  _float_ value corresponds to the point along the color spectrum from  _color1_ to  _color2_.</span></span> <span data-ttu-id="a8ad4-131">Por lo tanto, más pequeños números (más cerca de cero) para fusiones más cerca de _float_ producen a _color1_, mientras que los números más grandes (más cerca de 1) producen fusiones más cerca en _color2_.</span><span class="sxs-lookup"><span data-stu-id="a8ad4-131">Therefore, smaller numbers (closer to zero) for  _float_ produce blends closer to  _color1_, while larger numbers (closer to 1) produce blends closer to  _color2_.</span></span>
  

