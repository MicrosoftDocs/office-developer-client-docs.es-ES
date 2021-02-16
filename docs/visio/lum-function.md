---
title: LUM (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251460
localization_priority: Normal
ms.assetid: 38e6bba7-1bf2-3d31-0912-707002454f5d
description: Devuelve el valor del componente de luminosidad de un color.
ms.openlocfilehash: 17fa43f8e2cd7422428f92724e351436233c2d62
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419341"
---
# <a name="lum-function"></a><span data-ttu-id="65c0e-103">Función LUM</span><span class="sxs-lookup"><span data-stu-id="65c0e-103">LUM Function</span></span>

<span data-ttu-id="65c0e-104">Devuelve el valor del componente de luminosidad de un color.</span><span class="sxs-lookup"><span data-stu-id="65c0e-104">Returns the value of a color's luminosity component.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="65c0e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65c0e-105">Syntax</span></span>

<span data-ttu-id="65c0e-106">LUM(\*\* *expression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="65c0e-106">LUM(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="65c0e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65c0e-107">Parameters</span></span>

|<span data-ttu-id="65c0e-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="65c0e-108">**Name**</span></span>|<span data-ttu-id="65c0e-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="65c0e-109">**Required/Optional**</span></span>|<span data-ttu-id="65c0e-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="65c0e-110">**Data Type**</span></span>|<span data-ttu-id="65c0e-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65c0e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="65c0e-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="65c0e-112">_expression_</span></span> <br/> |<span data-ttu-id="65c0e-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="65c0e-113">Required</span></span>  <br/> |<span data-ttu-id="65c0e-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="65c0e-114">**Numeric**</span></span> <br/> |<span data-ttu-id="65c0e-115">Índice de un color en la tabla de colores del documento o una referencia a una celda que contiene un índice de color.</span><span class="sxs-lookup"><span data-stu-id="65c0e-115">The index of a color in the document's color table, or a reference to a cell that contains a color index.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="65c0e-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65c0e-116">Return value</span></span>

<span data-ttu-id="65c0e-117">Número</span><span class="sxs-lookup"><span data-stu-id="65c0e-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="65c0e-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="65c0e-118">Remarks</span></span>

<span data-ttu-id="65c0e-p101">El valor devuelto es un número en el intervalo de 0 a 240, ambos incluidos. La función devuelve 0 para la entrada no válida.</span><span class="sxs-lookup"><span data-stu-id="65c0e-p101">The return value is a number in the range 0 to 240, inclusive. The function returns 0 for invalid input.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="65c0e-121">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="65c0e-121">Example 1</span></span>

<span data-ttu-id="65c0e-122">LUM(Sheet.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="65c0e-122">LUM(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="65c0e-123">Devuelve la luminosidad del color de relleno del primer plano en la Hoja.4.</span><span class="sxs-lookup"><span data-stu-id="65c0e-123">Returns the luminosity of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="65c0e-124">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="65c0e-124">Example 2</span></span>

<span data-ttu-id="65c0e-125">LUM(6)</span><span class="sxs-lookup"><span data-stu-id="65c0e-125">LUM(6)</span></span>
  
<span data-ttu-id="65c0e-126">Devuelve 120 si el documento utiliza la paleta de colores predeterminada de Visio, en la que el índice 6 está asignado al color magenta.</span><span class="sxs-lookup"><span data-stu-id="65c0e-126">Returns 120 if the document uses the default Visio color palette, where magenta is the color at index 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="65c0e-127">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="65c0e-127">Example 3</span></span>

<span data-ttu-id="65c0e-128">LUM(HSL(10; 20; 30))</span><span class="sxs-lookup"><span data-stu-id="65c0e-128">LUM(HSL(10, 20, 30))</span></span>
  
<span data-ttu-id="65c0e-129">Devuelve 30.</span><span class="sxs-lookup"><span data-stu-id="65c0e-129">Returns 30.</span></span>
  

