---
title: Celda SketchAmount (sección de propiedades de efecto adicionales)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Determina la cantidad de distorsión para un efecto de boceto, como un número entero entre 0 y 25.
ms.openlocfilehash: d5ae954f2eab48722c48c9bc4b3f640403dbb3ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823256"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a><span data-ttu-id="c0243-103">Celda SketchAmount (sección de propiedades de efecto adicionales)</span><span class="sxs-lookup"><span data-stu-id="c0243-103">SketchAmount Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="c0243-104">Determina la cantidad de distorsión para un efecto de boceto, como un número entero entre 0 y 25.</span><span class="sxs-lookup"><span data-stu-id="c0243-104">Determines the amount of distortion for a sketch effect, as an integer between 0 and 25.</span></span> 
  
|<span data-ttu-id="c0243-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c0243-105">**Value**</span></span>|<span data-ttu-id="c0243-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c0243-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c0243-107">0</span><span class="sxs-lookup"><span data-stu-id="c0243-107">0</span></span>  <br/> |<span data-ttu-id="c0243-108">La forma no tiene ningún efecto de boceto que se ha aplicado.</span><span class="sxs-lookup"><span data-stu-id="c0243-108">The shape has no sketch effect applied to it.</span></span>  <br/> |
|<span data-ttu-id="c0243-109">1-25</span><span class="sxs-lookup"><span data-stu-id="c0243-109">1-25</span></span>  <br/> |<span data-ttu-id="c0243-110">La forma tiene distorsión de esbozo que se ha aplicado, donde un valor de 1 es la mayoría distorsión y 25 es el menor.</span><span class="sxs-lookup"><span data-stu-id="c0243-110">The shape has sketch distortion applied to it, where a value of 1 is the most distortion and 25 is the least.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0243-111">Notas</span><span class="sxs-lookup"><span data-stu-id="c0243-111">Remarks</span></span>

<span data-ttu-id="c0243-112">Para obtener una referencia a la celda **SketchAmount** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="c0243-112">To get a reference to the **SketchAmount** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0243-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c0243-113">Cell name:</span></span>  <br/> | <span data-ttu-id="c0243-114">SketchAmount</span><span class="sxs-lookup"><span data-stu-id="c0243-114">SketchAmount</span></span>  <br/> |
   
<span data-ttu-id="c0243-115">Para obtener una referencia a la celda **SketchAmount** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c0243-115">To get a reference to the **SketchAmount** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0243-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c0243-116">Section index:</span></span>  <br/> |<span data-ttu-id="c0243-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c0243-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c0243-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c0243-118">Row index:</span></span>  <br/> |<span data-ttu-id="c0243-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="c0243-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="c0243-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c0243-120">Cell index:</span></span>  <br/> |<span data-ttu-id="c0243-121">**visSketchAmount**</span><span class="sxs-lookup"><span data-stu-id="c0243-121">**visSketchAmount**</span></span> <br/> |
   

