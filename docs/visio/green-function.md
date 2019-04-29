---
title: GREEN (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251434
localization_priority: Normal
ms.assetid: eccec432-32d3-15c2-06b3-dd02b6313d4c
description: Devuelve el componente verde de un color.
ms.openlocfilehash: 0412e4519c2964b05d7663805d7773e8dc5deaab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438109"
---
# <a name="green-function"></a><span data-ttu-id="78c36-103">Función GREEN</span><span class="sxs-lookup"><span data-stu-id="78c36-103">GREEN Function</span></span>

<span data-ttu-id="78c36-104">Devuelve el componente verde de un color.</span><span class="sxs-lookup"><span data-stu-id="78c36-104">Returns the green component of a color.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="78c36-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78c36-105">Syntax</span></span>

<span data-ttu-id="78c36-106">VERDE (\* \* *expresión* \* \*)</span><span class="sxs-lookup"><span data-stu-id="78c36-106">GREEN(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="78c36-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="78c36-107">Parameters</span></span>

|<span data-ttu-id="78c36-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="78c36-108">**Name**</span></span>|<span data-ttu-id="78c36-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="78c36-109">**Required/Optional**</span></span>|<span data-ttu-id="78c36-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="78c36-110">**Data Type**</span></span>|<span data-ttu-id="78c36-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="78c36-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="78c36-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="78c36-112">_expression_</span></span> <br/> |<span data-ttu-id="78c36-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="78c36-113">Required</span></span>  <br/> |<span data-ttu-id="78c36-114">**Diferencias**</span><span class="sxs-lookup"><span data-stu-id="78c36-114">**Varies**</span></span> <br/> |<span data-ttu-id="78c36-115">Índice de un color en la tabla de colores del documento, una expresión que da como resultado un color personalizado (como RGB o HSL) o una referencia a una celda que contiene un índice de color o un resultado de color.</span><span class="sxs-lookup"><span data-stu-id="78c36-115">An index of a color in the document's color table, an expression that resolves to a custom color (such as RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="78c36-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78c36-116">Return value</span></span>

<span data-ttu-id="78c36-117">Entero</span><span class="sxs-lookup"><span data-stu-id="78c36-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="78c36-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="78c36-118">Remarks</span></span>

<span data-ttu-id="78c36-119">El valor devuelto es un número entre 0 y 255, ambos incluidos, o una referencia a una celda que da como resultado un índice.</span><span class="sxs-lookup"><span data-stu-id="78c36-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="78c36-120">Si la *expresión* no es válida, devuelve 0 (negro).</span><span class="sxs-lookup"><span data-stu-id="78c36-120">If  *expression*  is invalid, it returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="78c36-121">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="78c36-121">Example 1</span></span>

<span data-ttu-id="78c36-122">VERDE (hoja. 4! FillForegnd</span><span class="sxs-lookup"><span data-stu-id="78c36-122">GREEN(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="78c36-123">Devuelve el componente verde del color de relleno del primer plano en la Hoja.4.</span><span class="sxs-lookup"><span data-stu-id="78c36-123">Returns the green component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="78c36-124">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="78c36-124">Example 2</span></span>

<span data-ttu-id="78c36-125">VERDE (11)</span><span class="sxs-lookup"><span data-stu-id="78c36-125">GREEN(11)</span></span>
  
<span data-ttu-id="78c36-126">Devuelve 128 si el documento utiliza la paleta de colores predeterminada de Visio, en la que el índice 11 está asignado al color amarillo oscuro.</span><span class="sxs-lookup"><span data-stu-id="78c36-126">Returns 128 if the document uses the default Visio color palette, where dark yellow is the color at index 11.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="78c36-127">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="78c36-127">Example 3</span></span>

<span data-ttu-id="78c36-128">GREEN(RGB(10; 20; 30))</span><span class="sxs-lookup"><span data-stu-id="78c36-128">GREEN(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="78c36-129">Devuelve 20.</span><span class="sxs-lookup"><span data-stu-id="78c36-129">Returns 20.</span></span>
  

