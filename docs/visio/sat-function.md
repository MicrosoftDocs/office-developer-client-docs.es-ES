---
title: SAT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251494
localization_priority: Normal
ms.assetid: 407817fb-9e4a-d2ca-6125-2440d2a417c6
description: Devuelve el valor del componente de saturación de un color.
ms.openlocfilehash: 54f3fa68c567c2a32e8cfd37c406387cd6973ce3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823099"
---
# <a name="sat-function"></a><span data-ttu-id="ff072-103">Función SAT</span><span class="sxs-lookup"><span data-stu-id="ff072-103">SAT Function</span></span>

<span data-ttu-id="ff072-104">Devuelve el valor del componente de saturación de un color.</span><span class="sxs-lookup"><span data-stu-id="ff072-104">Returns the value of a color's saturation component.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ff072-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff072-105">Syntax</span></span>

<span data-ttu-id="ff072-106">SAT (** *expresión* **)</span><span class="sxs-lookup"><span data-stu-id="ff072-106">SAT(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ff072-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff072-107">Parameters</span></span>

|<span data-ttu-id="ff072-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ff072-108">**Name**</span></span>|<span data-ttu-id="ff072-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="ff072-109">**Required/Optional**</span></span>|<span data-ttu-id="ff072-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="ff072-110">**Data Type**</span></span>|<span data-ttu-id="ff072-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ff072-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ff072-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="ff072-112">_expression_</span></span> <br/> |<span data-ttu-id="ff072-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ff072-113">Required</span></span>  <br/> |<span data-ttu-id="ff072-114">**Varies**</span><span class="sxs-lookup"><span data-stu-id="ff072-114">**Varies**</span></span> <br/> |<span data-ttu-id="ff072-115">Índice de uno de los colores de la tabla de color del documento, una expresión que da como resultado un color personalizado (como RGB o HSL) o una referencia a una celda que contiene un índice de color o un resultado de color.</span><span class="sxs-lookup"><span data-stu-id="ff072-115">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ff072-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff072-116">Return value</span></span>

<span data-ttu-id="ff072-117">Numeric</span><span class="sxs-lookup"><span data-stu-id="ff072-117">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ff072-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff072-118">Remarks</span></span>

<span data-ttu-id="ff072-p101">El valor devuelto es un número en el intervalo de 0 a 240, ambos incluidos. La función devuelve 0 para la entrada no válida.</span><span class="sxs-lookup"><span data-stu-id="ff072-p101">The return value is a number in the range 0 to 240, inclusive. The function returns 0 for invalid input.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="ff072-121">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="ff072-121">Example 1</span></span>

<span data-ttu-id="ff072-122">¡SAT (hoja.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="ff072-122">SAT(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="ff072-123">Devuelve la saturación del color de relleno en primer plano de la Hoja.4.</span><span class="sxs-lookup"><span data-stu-id="ff072-123">Returns the saturation of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ff072-124">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="ff072-124">Example 2</span></span>

<span data-ttu-id="ff072-125">SAT(8)</span><span class="sxs-lookup"><span data-stu-id="ff072-125">SAT(8)</span></span>
  
<span data-ttu-id="ff072-126">Devuelve 240 si el documento utiliza la paleta de colores predeterminada de Visio, en la que el índice 8 está asignado al color rojo oscuro.</span><span class="sxs-lookup"><span data-stu-id="ff072-126">Returns 240 if the document uses the default Visio color palette, where dark red is the color at index 8.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ff072-127">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="ff072-127">Example 3</span></span>

<span data-ttu-id="ff072-128">SAT(HSL(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="ff072-128">SAT(HSL(10, 20, 30))</span></span>
  
<span data-ttu-id="ff072-129">Devuelve 20.</span><span class="sxs-lookup"><span data-stu-id="ff072-129">Returns 20.</span></span>
  

