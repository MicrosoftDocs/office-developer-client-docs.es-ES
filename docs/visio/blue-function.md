---
title: BLUE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251402
localization_priority: Normal
ms.assetid: da9fb933-4e2c-3e2a-1879-6e70db0cd830
description: Devuelve el componente azul de un color. El valor devuelto es un entero en el rango de 0 a 255, ambos inclusive. La función devuelve el valor 0 para la entrada no válida.
ms.openlocfilehash: 6a86a0ee91054c89f2def95c0e3521508462bdaa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821661"
---
# <a name="blue-function"></a><span data-ttu-id="55eab-105">Función BLUE</span><span class="sxs-lookup"><span data-stu-id="55eab-105">BLUE Function</span></span>

<span data-ttu-id="55eab-106">Devuelve el componente azul de un color.</span><span class="sxs-lookup"><span data-stu-id="55eab-106">Returns the blue component of a color.</span></span> <span data-ttu-id="55eab-107">El valor devuelto es un entero en el rango de 0 a 255, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="55eab-107">The return value is an integer in the range of 0 to 255, inclusive.</span></span> <span data-ttu-id="55eab-108">La función devuelve el valor 0 para la entrada no válida.</span><span class="sxs-lookup"><span data-stu-id="55eab-108">The function returns 0 for invalid input.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="55eab-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55eab-109">Syntax</span></span>

<span data-ttu-id="55eab-110">AZUL (** *expresión* **)</span><span class="sxs-lookup"><span data-stu-id="55eab-110">BLUE(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="55eab-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55eab-111">Parameters</span></span>

|<span data-ttu-id="55eab-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="55eab-112">**Name**</span></span>|<span data-ttu-id="55eab-113">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="55eab-113">**Required/Optional**</span></span>|<span data-ttu-id="55eab-114">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="55eab-114">**Data Type**</span></span>|<span data-ttu-id="55eab-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="55eab-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="55eab-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="55eab-116">_expression_</span></span> <br/> |<span data-ttu-id="55eab-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="55eab-117">Required</span></span>  <br/> |<span data-ttu-id="55eab-118">**String**</span><span class="sxs-lookup"><span data-stu-id="55eab-118">**String**</span></span> <br/> |<span data-ttu-id="55eab-119">Índice de uno de los colores de la tabla de color del documento, una expresión que da como resultado un color personalizado (como RGB o HSL) o una referencia a una celda que contiene un índice de color o un resultado de color.</span><span class="sxs-lookup"><span data-stu-id="55eab-119">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="55eab-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55eab-120">Return value</span></span>

<span data-ttu-id="55eab-121">Integer</span><span class="sxs-lookup"><span data-stu-id="55eab-121">Integer</span></span>
  
## <a name="example-1"></a><span data-ttu-id="55eab-122">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="55eab-122">Example 1</span></span>

<span data-ttu-id="55eab-123">¡AZUL (hoja.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="55eab-123">BLUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="55eab-124">Devuelve el componente azul del color de relleno del primer plano en la Hoja.4.</span><span class="sxs-lookup"><span data-stu-id="55eab-124">Returns the blue component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="55eab-125">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="55eab-125">Example 2</span></span>

<span data-ttu-id="55eab-126">BLUE(13)</span><span class="sxs-lookup"><span data-stu-id="55eab-126">BLUE(13)</span></span>
  
<span data-ttu-id="55eab-127">Devuelve 128 si el documento utiliza la paleta predeterminada de colores de Visio, en la que el índice 13 está asignado al color cian.</span><span class="sxs-lookup"><span data-stu-id="55eab-127">Returns 128 if the document uses the default Visio color palette, where cyan is the color at index 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="55eab-128">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="55eab-128">Example 3</span></span>

<span data-ttu-id="55eab-129">BLUE(RGB(10; 20; 30))</span><span class="sxs-lookup"><span data-stu-id="55eab-129">BLUE(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="55eab-130">Devuelve 30.</span><span class="sxs-lookup"><span data-stu-id="55eab-130">Returns 30.</span></span>
  

