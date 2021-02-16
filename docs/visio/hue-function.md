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
description: Devuelve el valor del componente de matiz de un color.
ms.openlocfilehash: 39fdd160f5cd792e95930a3e7c7cea3c37ed16c1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439495"
---
# <a name="hue-function"></a><span data-ttu-id="1e32c-103">Función HUE</span><span class="sxs-lookup"><span data-stu-id="1e32c-103">HUE Function</span></span>

<span data-ttu-id="1e32c-104">Devuelve el valor del componente de matiz de un color.</span><span class="sxs-lookup"><span data-stu-id="1e32c-104">Returns the value of a color's hue component.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="1e32c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e32c-105">Syntax</span></span>

<span data-ttu-id="1e32c-106">HUE(\*\* *expression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="1e32c-106">HUE(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1e32c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e32c-107">Parameters</span></span>

|<span data-ttu-id="1e32c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="1e32c-108">**Name**</span></span>|<span data-ttu-id="1e32c-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="1e32c-109">**Required/Optional**</span></span>|<span data-ttu-id="1e32c-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="1e32c-110">**Data Type**</span></span>|<span data-ttu-id="1e32c-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1e32c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1e32c-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="1e32c-112">_expression_</span></span> <br/> |<span data-ttu-id="1e32c-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1e32c-113">Required</span></span>  <br/> |<span data-ttu-id="1e32c-114">**String**</span><span class="sxs-lookup"><span data-stu-id="1e32c-114">**String**</span></span> <br/> |<span data-ttu-id="1e32c-115">Expresión que da como resultado un color.</span><span class="sxs-lookup"><span data-stu-id="1e32c-115">An expression that evaluates to a color.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="1e32c-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e32c-116">Return value</span></span>

<span data-ttu-id="1e32c-117">Número</span><span class="sxs-lookup"><span data-stu-id="1e32c-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1e32c-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1e32c-118">Remarks</span></span>

<span data-ttu-id="1e32c-p101">El valor obtenido es un número en el intervalo de 0 a 239, ambos incluidos. La entrada es el índice de uno de los colores de la tabla de color del documento, una expresión que da como resultado un color personalizado (como RGB o HSL) o una referencia a una celda que contiene un índice de color o un resultado de color. La función devuelve 0 si la entrada no es válida.</span><span class="sxs-lookup"><span data-stu-id="1e32c-p101">The return value is a number in the range 0 to 239, inclusive. The input is an index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result. The function returns 0 for invalid input.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="1e32c-122">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="1e32c-122">Example 1</span></span>

<span data-ttu-id="1e32c-123">HUE(Sheet.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="1e32c-123">HUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="1e32c-124">Devuelve el matiz del color de relleno en primer plano de la Hoja.4.</span><span class="sxs-lookup"><span data-stu-id="1e32c-124">Returns the hue of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="1e32c-125">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="1e32c-125">Example 2</span></span>

<span data-ttu-id="1e32c-126">HUE(7)</span><span class="sxs-lookup"><span data-stu-id="1e32c-126">HUE(7)</span></span>
  
<span data-ttu-id="1e32c-127">Devuelve 120 si el documento utiliza la paleta de colores predeterminada de Microsoft Visio, en la que el índice 7 está asignado al color cian.</span><span class="sxs-lookup"><span data-stu-id="1e32c-127">Returns 120 if the document uses the default Microsoft Visio color palette, where cyan is the color at index 7.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="1e32c-128">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="1e32c-128">Example 3</span></span>

<span data-ttu-id="1e32c-129">HUE(HSL(10; 20; 30) )</span><span class="sxs-lookup"><span data-stu-id="1e32c-129">HUE(HSL(10, 20, 30) )</span></span>
  
<span data-ttu-id="1e32c-130">Devuelve 10.</span><span class="sxs-lookup"><span data-stu-id="1e32c-130">Returns 10.</span></span>
  

