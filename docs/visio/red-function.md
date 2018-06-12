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
ms.openlocfilehash: 801ebb64564df81f72c41cb720fe53f0f1b4c10d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822900"
---
# <a name="red-function"></a><span data-ttu-id="c1176-103">RED (función)</span><span class="sxs-lookup"><span data-stu-id="c1176-103">RED Function</span></span>

<span data-ttu-id="c1176-104">Devuelve el componente rojo de un color.</span><span class="sxs-lookup"><span data-stu-id="c1176-104">Returns the red component of a color.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c1176-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1176-105">Syntax</span></span>

<span data-ttu-id="c1176-106">ROJO (** *expresión* **)</span><span class="sxs-lookup"><span data-stu-id="c1176-106">RED(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c1176-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1176-107">Parameters</span></span>

|<span data-ttu-id="c1176-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c1176-108">**Name**</span></span>|<span data-ttu-id="c1176-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="c1176-109">**Required/Optional**</span></span>|<span data-ttu-id="c1176-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="c1176-110">**Data Type**</span></span>|<span data-ttu-id="c1176-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1176-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c1176-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="c1176-112">_expression_</span></span> <br/> |<span data-ttu-id="c1176-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c1176-113">Required</span></span>  <br/> |<span data-ttu-id="c1176-114">**Varía**</span><span class="sxs-lookup"><span data-stu-id="c1176-114">**Varies**</span></span> <br/> |<span data-ttu-id="c1176-115">Índice de uno de los colores de la tabla de color del documento, una expresión que da como resultado un color personalizado (como RGB o HSL) o una referencia a una celda que contiene un índice de color o un resultado de color.</span><span class="sxs-lookup"><span data-stu-id="c1176-115">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c1176-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1176-116">Return value</span></span>

<span data-ttu-id="c1176-117">Number</span><span class="sxs-lookup"><span data-stu-id="c1176-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c1176-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1176-118">Remarks</span></span>

<span data-ttu-id="c1176-119">El valor devuelto es un número en el rango de 0 a 255, ambos incluidos, o una referencia de celda que se resuelve en un índice.</span><span class="sxs-lookup"><span data-stu-id="c1176-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="c1176-120">Si la _expresión_ no es válido, esta función devuelve 0 (negro).</span><span class="sxs-lookup"><span data-stu-id="c1176-120">If  _expression_ is invalid, this function returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="c1176-121">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="c1176-121">Example 1</span></span>

<span data-ttu-id="c1176-122">RED(22)</span><span class="sxs-lookup"><span data-stu-id="c1176-122">RED(22)</span></span>
  
<span data-ttu-id="c1176-123">Devuelve 51 si el documento utiliza la paleta de colores predeterminada de Microsoft Office Visio, en la que el índice 22 está asignado al color gris oscuro.</span><span class="sxs-lookup"><span data-stu-id="c1176-123">Returns 51 if the document uses the default Microsoft Office Visio color palette, where dark gray is the color at index 22.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c1176-124">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="c1176-124">Example 2</span></span>

<span data-ttu-id="c1176-125">RED(Char.color)</span><span class="sxs-lookup"><span data-stu-id="c1176-125">RED(Char.Color)</span></span>
  
<span data-ttu-id="c1176-126">Devuelve el valor del componente rojo del color actual de fuente.</span><span class="sxs-lookup"><span data-stu-id="c1176-126">Returns the value of the red component of the current font color.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="c1176-127">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="c1176-127">Example 3</span></span>

<span data-ttu-id="c1176-128">RED(RGB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="c1176-128">RED(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="c1176-129">Devuelve 10.</span><span class="sxs-lookup"><span data-stu-id="c1176-129">Returns 10.</span></span>
  

