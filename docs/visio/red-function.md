---
title: RED (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251487
localization_priority: Normal
ms.assetid: a95fd86d-ebc1-66b6-e7d9-9c8ea84d23ab
description: Devuelve el componente rojo de un color.
ms.openlocfilehash: e8c6115ac0441b25ce8333485828e8ef0f615459
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359986"
---
# <a name="red-function"></a><span data-ttu-id="83e09-103">Función RED</span><span class="sxs-lookup"><span data-stu-id="83e09-103">RED Function</span></span>

<span data-ttu-id="83e09-104">Devuelve el componente rojo de un color.</span><span class="sxs-lookup"><span data-stu-id="83e09-104">Returns the red component of a color.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="83e09-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83e09-105">Syntax</span></span>

<span data-ttu-id="83e09-106">RED (\* \* *expresión* \* \*)</span><span class="sxs-lookup"><span data-stu-id="83e09-106">RED(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="83e09-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83e09-107">Parameters</span></span>

|<span data-ttu-id="83e09-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="83e09-108">**Name**</span></span>|<span data-ttu-id="83e09-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="83e09-109">**Required/Optional**</span></span>|<span data-ttu-id="83e09-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="83e09-110">**Data Type**</span></span>|<span data-ttu-id="83e09-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="83e09-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="83e09-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="83e09-112">_expression_</span></span> <br/> |<span data-ttu-id="83e09-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="83e09-113">Required</span></span>  <br/> |<span data-ttu-id="83e09-114">**Diferencias**</span><span class="sxs-lookup"><span data-stu-id="83e09-114">**Varies**</span></span> <br/> |<span data-ttu-id="83e09-115">Índice de uno de los colores de la tabla de color del documento, una expresión que da como resultado un color personalizado (como RGB o HSL) o una referencia a una celda que contiene un índice de color o un resultado de color.</span><span class="sxs-lookup"><span data-stu-id="83e09-115">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="83e09-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83e09-116">Return value</span></span>

<span data-ttu-id="83e09-117">Número</span><span class="sxs-lookup"><span data-stu-id="83e09-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="83e09-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="83e09-118">Remarks</span></span>

<span data-ttu-id="83e09-119">El valor devuelto es un número entre 0 y 255, ambos incluidos, o una referencia a una celda que da como resultado un índice.</span><span class="sxs-lookup"><span data-stu-id="83e09-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="83e09-120">Si la _expresión_ no es válida, esta función devuelve 0 (negro).</span><span class="sxs-lookup"><span data-stu-id="83e09-120">If  _expression_ is invalid, this function returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="83e09-121">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="83e09-121">Example 1</span></span>

<span data-ttu-id="83e09-122">ROJO (22)</span><span class="sxs-lookup"><span data-stu-id="83e09-122">RED(22)</span></span>
  
<span data-ttu-id="83e09-123">Devuelve 51 si el documento utiliza la paleta de colores predeterminada de Microsoft Office Visio, en la que el índice 22 está asignado al color gris oscuro.</span><span class="sxs-lookup"><span data-stu-id="83e09-123">Returns 51 if the document uses the default Microsoft Office Visio color palette, where dark gray is the color at index 22.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="83e09-124">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="83e09-124">Example 2</span></span>

<span data-ttu-id="83e09-125">ROJO (Char. color)</span><span class="sxs-lookup"><span data-stu-id="83e09-125">RED(Char.Color)</span></span>
  
<span data-ttu-id="83e09-126">Devuelve el valor del componente rojo del color actual de fuente.</span><span class="sxs-lookup"><span data-stu-id="83e09-126">Returns the value of the red component of the current font color.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="83e09-127">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="83e09-127">Example 3</span></span>

<span data-ttu-id="83e09-128">RED(RGB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="83e09-128">RED(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="83e09-129">Devuelve 10.</span><span class="sxs-lookup"><span data-stu-id="83e09-129">Returns 10.</span></span>
  

