---
title: GUARD (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251435
localization_priority: Normal
ms.assetid: 6c85414c-9fb6-cdc5-f5b6-8eb13c9608af
description: Protege la expresión de eliminar ni cambiar mediante acciones realizadas en la ventana de dibujo, por ejemplo, mover, cambiar de tamaño, agrupar o desagrupar formas.
ms.openlocfilehash: fd5fcfbe11eb054dfa625834640c0280cae96c3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822247"
---
# <a name="guard-function"></a><span data-ttu-id="1b939-103">Función GUARD</span><span class="sxs-lookup"><span data-stu-id="1b939-103">GUARD Function</span></span>

<span data-ttu-id="1b939-104">Protege la *expresión* de eliminar ni cambiar mediante acciones realizadas en la ventana de dibujo, por ejemplo, mover, cambiar de tamaño, agrupar o desagrupar formas.</span><span class="sxs-lookup"><span data-stu-id="1b939-104">Protects  *expression*  from deletion and change by actions performed in the drawing window, for example, moving, sizing, grouping, or ungrouping shapes.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1b939-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b939-105">Syntax</span></span>

<span data-ttu-id="1b939-106">GUARD (** *expresión* **)</span><span class="sxs-lookup"><span data-stu-id="1b939-106">GUARD(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1b939-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b939-107">Parameters</span></span>

|<span data-ttu-id="1b939-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="1b939-108">**Name**</span></span>|<span data-ttu-id="1b939-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="1b939-109">**Required/Optional**</span></span>|<span data-ttu-id="1b939-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="1b939-110">**Data Type**</span></span>|<span data-ttu-id="1b939-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1b939-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1b939-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="1b939-112">_expression_</span></span> <br/> |<span data-ttu-id="1b939-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1b939-113">Required</span></span>  <br/> |<span data-ttu-id="1b939-114">**String**</span><span class="sxs-lookup"><span data-stu-id="1b939-114">**String**</span></span> <br/> |<span data-ttu-id="1b939-115">Combinación de constantes, operadores, funciones y referencias a las celdas de ShapeSheet que da como resultado un valor.</span><span class="sxs-lookup"><span data-stu-id="1b939-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b939-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b939-116">Remarks</span></span>

<span data-ttu-id="1b939-117">Las celdas con que se suele utilizar la función GUARD son Width, Height, PinX y PinY.</span><span class="sxs-lookup"><span data-stu-id="1b939-117">The cells most often affected by the GUARD function are Width, Height, PinX, and PinY.</span></span> 
  
<span data-ttu-id="1b939-p101">Al guardar una fórmula en una celda se impide que pueda cambiar el valor de esa celda como consecuencia de acciones realizadas en la ventana de dibujo. Sin embargo, una acción efectuada en la ventana de dibujo puede afectar a varias celdas, por lo que todas ellas deben estar protegidas por la función GUARD si desea evitar cambios inesperados en la apariencia de la forma.</span><span class="sxs-lookup"><span data-stu-id="1b939-p101">Guarding a formula in any cell prevents that cell's value from being changed by actions in the drawing window. However, one action in the drawing window can affect several cells, and each of these cells must be guarded if you want to prevent unexpected changes to the shape's appearance.</span></span> 
  
## <a name="example"></a><span data-ttu-id="1b939-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1b939-120">Example</span></span>

<span data-ttu-id="1b939-121">GUARD(TEXTWIDTH(TheText) + 1,5 cm)</span><span class="sxs-lookup"><span data-stu-id="1b939-121">GUARD(TEXTWIDTH(TheText) + 0.5 in)</span></span> 
  
<span data-ttu-id="1b939-p102">Al incluir esta expresión en la celda Width de la sección de transformación de forma se impide que la expresión (TEXTWIDTH(TheText) + 1,5 cm) sea sustituida por otro valor al cambiar el ancho de la forma en la ventana de dibujo. TheText es una celda que se desencadena cuando cambia la composición del texto de la forma asociada.</span><span class="sxs-lookup"><span data-stu-id="1b939-p102">This expression in the Width cell of a shape's Shape Transform section prevents the expression (TEXTWIDTH(TheText) + 0.5 in) from being replaced with another value when the shape's width is changed in the drawing window. TheText is a cell that gets triggered when the associated shape's text composition changes.</span></span> 
  
