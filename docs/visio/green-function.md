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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360210"
---
# <a name="green-function"></a><span data-ttu-id="acbbc-103">Función GREEN</span><span class="sxs-lookup"><span data-stu-id="acbbc-103">GREEN Function</span></span>

<span data-ttu-id="acbbc-104">Devuelve el componente verde de un color.</span><span class="sxs-lookup"><span data-stu-id="acbbc-104">Returns the green component of a color.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="acbbc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="acbbc-105">Syntax</span></span>

<span data-ttu-id="acbbc-106">VERDE (\* \* *expresión* \* \*)</span><span class="sxs-lookup"><span data-stu-id="acbbc-106">GREEN(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="acbbc-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="acbbc-107">Parameters</span></span>

|<span data-ttu-id="acbbc-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="acbbc-108">**Name**</span></span>|<span data-ttu-id="acbbc-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="acbbc-109">**Required/Optional**</span></span>|<span data-ttu-id="acbbc-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="acbbc-110">**Data Type**</span></span>|<span data-ttu-id="acbbc-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="acbbc-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="acbbc-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="acbbc-112">_expression_</span></span> <br/> |<span data-ttu-id="acbbc-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="acbbc-113">Required</span></span>  <br/> |<span data-ttu-id="acbbc-114">**Diferencias**</span><span class="sxs-lookup"><span data-stu-id="acbbc-114">**Varies**</span></span> <br/> |<span data-ttu-id="acbbc-115">Índice de un color en la tabla de colores del documento, una expresión que da como resultado un color personalizado (como RGB o HSL) o una referencia a una celda que contiene un índice de color o un resultado de color.</span><span class="sxs-lookup"><span data-stu-id="acbbc-115">An index of a color in the document's color table, an expression that resolves to a custom color (such as RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="acbbc-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="acbbc-116">Return value</span></span>

<span data-ttu-id="acbbc-117">Entero</span><span class="sxs-lookup"><span data-stu-id="acbbc-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="acbbc-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="acbbc-118">Remarks</span></span>

<span data-ttu-id="acbbc-119">El valor devuelto es un número entre 0 y 255, ambos incluidos, o una referencia a una celda que da como resultado un índice.</span><span class="sxs-lookup"><span data-stu-id="acbbc-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="acbbc-120">Si la *expresión* no es válida, devuelve 0 (negro).</span><span class="sxs-lookup"><span data-stu-id="acbbc-120">If  *expression*  is invalid, it returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="acbbc-121">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="acbbc-121">Example 1</span></span>

<span data-ttu-id="acbbc-122">VERDE (hoja. 4! FillForegnd</span><span class="sxs-lookup"><span data-stu-id="acbbc-122">GREEN(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="acbbc-123">Devuelve el componente verde del color de relleno del primer plano en la Hoja.4.</span><span class="sxs-lookup"><span data-stu-id="acbbc-123">Returns the green component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="acbbc-124">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="acbbc-124">Example 2</span></span>

<span data-ttu-id="acbbc-125">VERDE (11)</span><span class="sxs-lookup"><span data-stu-id="acbbc-125">GREEN(11)</span></span>
  
<span data-ttu-id="acbbc-126">Devuelve 128 si el documento utiliza la paleta de colores predeterminada de Visio, en la que el índice 11 está asignado al color amarillo oscuro.</span><span class="sxs-lookup"><span data-stu-id="acbbc-126">Returns 128 if the document uses the default Visio color palette, where dark yellow is the color at index 11.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="acbbc-127">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="acbbc-127">Example 3</span></span>

<span data-ttu-id="acbbc-128">GREEN(RGB(10; 20; 30))</span><span class="sxs-lookup"><span data-stu-id="acbbc-128">GREEN(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="acbbc-129">Devuelve 20.</span><span class="sxs-lookup"><span data-stu-id="acbbc-129">Returns 20.</span></span>
  

