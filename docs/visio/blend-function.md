---
title: BLEND (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Fusiona dos colores en la proporción especificada por el parámetro float.
ms.openlocfilehash: 0a231954370416be201183026424c79942204e12
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303300"
---
# <a name="blend-function"></a><span data-ttu-id="5eabe-103">Función BLEND</span><span class="sxs-lookup"><span data-stu-id="5eabe-103">BLEND Function</span></span>

<span data-ttu-id="5eabe-104">Fusiona dos colores en la proporción especificada por el parámetro _float_ .</span><span class="sxs-lookup"><span data-stu-id="5eabe-104">Blends two colors in the proportion specified by the  _float_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5eabe-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5eabe-105">Syntax</span></span>

<span data-ttu-id="5eabe-106">BLEND (\* \* *color1* \* \*, \* \* *color2* \* \*, \* \* *flotante [0, 1]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="5eabe-106">BLEND(\*\* *color1* \*\*, \*\* *color2* \*\*, \*\* *float[0,1]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5eabe-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5eabe-107">Parameters</span></span>

|<span data-ttu-id="5eabe-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5eabe-108">**Name**</span></span>|<span data-ttu-id="5eabe-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="5eabe-109">**Required/Optional**</span></span>|<span data-ttu-id="5eabe-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="5eabe-110">**Data Type**</span></span>|<span data-ttu-id="5eabe-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5eabe-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5eabe-112">_color1_</span><span class="sxs-lookup"><span data-stu-id="5eabe-112">_color1_</span></span> <br/> |<span data-ttu-id="5eabe-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5eabe-113">Required</span></span>  <br/> |<span data-ttu-id="5eabe-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="5eabe-114">**Numeric**</span></span> <br/> |<span data-ttu-id="5eabe-115">Índice de color de Visio o valor RGB del primer color.</span><span class="sxs-lookup"><span data-stu-id="5eabe-115">The Visio color index or RGB value of the first color.</span></span>  <br/> |
| <span data-ttu-id="5eabe-116">_color2_</span><span class="sxs-lookup"><span data-stu-id="5eabe-116">_color2_</span></span> <br/> |<span data-ttu-id="5eabe-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5eabe-117">Required</span></span>  <br/> |<span data-ttu-id="5eabe-118">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="5eabe-118">**Numeric**</span></span> <br/> |<span data-ttu-id="5eabe-119">Índice de color de Visio o valor RGB del segundo color.</span><span class="sxs-lookup"><span data-stu-id="5eabe-119">The Visio color index or RGB value of the second color.</span></span>  <br/> |
| <span data-ttu-id="5eabe-120">_punto flotante [0, 1]_</span><span class="sxs-lookup"><span data-stu-id="5eabe-120">_float[0,1]_</span></span> <br/> |<span data-ttu-id="5eabe-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5eabe-121">Required</span></span>  <br/> |<span data-ttu-id="5eabe-122">**Float**</span><span class="sxs-lookup"><span data-stu-id="5eabe-122">**Float**</span></span> <br/> |<span data-ttu-id="5eabe-123">La proporción en la que se mezclan _color2_ y _color1_, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5eabe-123">The proportion in which to blend  _color2_ and  _color1_, respectively.</span></span> <span data-ttu-id="5eabe-124">Número real entre 0 y 1, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="5eabe-124">A real number from 0 to 1 inclusive.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5eabe-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5eabe-125">Return value</span></span>

 <span data-ttu-id="5eabe-126">**RVA**</span><span class="sxs-lookup"><span data-stu-id="5eabe-126">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5eabe-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5eabe-127">Remarks</span></span>

<span data-ttu-id="5eabe-128">El color devuelto está determinado por las proporciones relativas en las que se combinan _color2_ y _color1_, respectivamente, según lo especificado por el parámetro _float_ .</span><span class="sxs-lookup"><span data-stu-id="5eabe-128">The color returned is determined by the relative proportions in which to blend  _color2_ and  _color1_, respectively, as specified by the  _float_ parameter.</span></span> <span data-ttu-id="5eabe-129">Por ejemplo, si _float_ es 0,25, el color devuelto está compuesto 75% de _color1_ y el 25% de _color2_.</span><span class="sxs-lookup"><span data-stu-id="5eabe-129">For example, if  _float_ is 0.25, the color returned is composed 75% of  _color1_ and 25% of  _color2_.</span></span> 
  
<span data-ttu-id="5eabe-130">Otra forma de pensar en esto es que el valor _float_ se corresponde con el punto del espectro de colores desde _color1_ hasta _color2_.</span><span class="sxs-lookup"><span data-stu-id="5eabe-130">Another way to think about it is that the  _float_ value corresponds to the point along the color spectrum from  _color1_ to  _color2_.</span></span> <span data-ttu-id="5eabe-131">Por lo tanto, los números más pequeños (más cercanos a cero) para las mezclas de alimentos de _flota_ más cerca de _color1_, mientras que los números más grandes (más cercanos a 1) producen fusiones más cercanas a _color2_.</span><span class="sxs-lookup"><span data-stu-id="5eabe-131">Therefore, smaller numbers (closer to zero) for  _float_ produce blends closer to  _color1_, while larger numbers (closer to 1) produce blends closer to  _color2_.</span></span>
  

