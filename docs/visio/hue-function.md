---
title: HUE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251440
localization_priority: Normal
ms.assetid: 0f5c6097-eef5-5f58-e2ef-2c348e42dc9a
description: Devuelve el valor del componente Hue de un color.
ms.openlocfilehash: 39fdd160f5cd792e95930a3e7c7cea3c37ed16c1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329914"
---
# <a name="hue-function"></a><span data-ttu-id="f8947-103">Función HUE</span><span class="sxs-lookup"><span data-stu-id="f8947-103">HUE Function</span></span>

<span data-ttu-id="f8947-104">Devuelve el valor del componente Hue de un color.</span><span class="sxs-lookup"><span data-stu-id="f8947-104">Returns the value of a color's hue component.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f8947-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8947-105">Syntax</span></span>

<span data-ttu-id="f8947-106">MATIZ (\* \* *expresión* \* \*)</span><span class="sxs-lookup"><span data-stu-id="f8947-106">HUE(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f8947-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8947-107">Parameters</span></span>

|<span data-ttu-id="f8947-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f8947-108">**Name**</span></span>|<span data-ttu-id="f8947-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="f8947-109">**Required/Optional**</span></span>|<span data-ttu-id="f8947-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="f8947-110">**Data Type**</span></span>|<span data-ttu-id="f8947-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f8947-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f8947-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="f8947-112">_expression_</span></span> <br/> |<span data-ttu-id="f8947-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f8947-113">Required</span></span>  <br/> |<span data-ttu-id="f8947-114">**String**</span><span class="sxs-lookup"><span data-stu-id="f8947-114">**String**</span></span> <br/> |<span data-ttu-id="f8947-115">Expresión que da como resultado un color.</span><span class="sxs-lookup"><span data-stu-id="f8947-115">An expression that evaluates to a color.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f8947-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8947-116">Return value</span></span>

<span data-ttu-id="f8947-117">Número</span><span class="sxs-lookup"><span data-stu-id="f8947-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f8947-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f8947-118">Remarks</span></span>

<span data-ttu-id="f8947-p101">El valor obtenido es un número en el intervalo de 0 a 239, ambos incluidos. La entrada es el índice de uno de los colores de la tabla de color del documento, una expresión que da como resultado un color personalizado (como RGB o HSL) o una referencia a una celda que contiene un índice de color o un resultado de color. La función devuelve 0 si la entrada no es válida.</span><span class="sxs-lookup"><span data-stu-id="f8947-p101">The return value is a number in the range 0 to 239, inclusive. The input is an index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result. The function returns 0 for invalid input.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="f8947-122">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="f8947-122">Example 1</span></span>

<span data-ttu-id="f8947-123">MATIZ (hoja. 4! FillForegnd</span><span class="sxs-lookup"><span data-stu-id="f8947-123">HUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="f8947-124">Devuelve el matiz del color de relleno en primer plano de la Hoja.4.</span><span class="sxs-lookup"><span data-stu-id="f8947-124">Returns the hue of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f8947-125">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="f8947-125">Example 2</span></span>

<span data-ttu-id="f8947-126">MATIZ (7)</span><span class="sxs-lookup"><span data-stu-id="f8947-126">HUE(7)</span></span>
  
<span data-ttu-id="f8947-127">Devuelve 120 si el documento utiliza la paleta de colores predeterminada de Microsoft Visio, en la que el índice 7 está asignado al color cian.</span><span class="sxs-lookup"><span data-stu-id="f8947-127">Returns 120 if the document uses the default Microsoft Visio color palette, where cyan is the color at index 7.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="f8947-128">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="f8947-128">Example 3</span></span>

<span data-ttu-id="f8947-129">HUE(HSL(10; 20; 30) )</span><span class="sxs-lookup"><span data-stu-id="f8947-129">HUE(HSL(10, 20, 30) )</span></span>
  
<span data-ttu-id="f8947-130">Devuelve 10.</span><span class="sxs-lookup"><span data-stu-id="f8947-130">Returns 10.</span></span>
  

