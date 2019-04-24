---
title: Celda SketchAmount (sección Propiedades del efecto adicional)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Determina la cantidad de distorsión de un efecto de boceto, como un entero entre 0 y 25.
ms.openlocfilehash: fd9ee3390d05f24d81d9c6677160155b0f0f0d35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314773"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a><span data-ttu-id="1873a-103">Celda SketchAmount (sección Propiedades del efecto adicional)</span><span class="sxs-lookup"><span data-stu-id="1873a-103">SketchAmount Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="1873a-104">Determina la cantidad de distorsión de un efecto de boceto, como un entero entre 0 y 25.</span><span class="sxs-lookup"><span data-stu-id="1873a-104">Determines the amount of distortion for a sketch effect, as an integer between 0 and 25.</span></span> 
  
|<span data-ttu-id="1873a-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="1873a-105">**Value**</span></span>|<span data-ttu-id="1873a-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1873a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1873a-107">comprendi</span><span class="sxs-lookup"><span data-stu-id="1873a-107">0</span></span>  <br/> |<span data-ttu-id="1873a-108">La forma no tiene ningún efecto de boceto aplicado.</span><span class="sxs-lookup"><span data-stu-id="1873a-108">The shape has no sketch effect applied to it.</span></span>  <br/> |
|<span data-ttu-id="1873a-109">1-25</span><span class="sxs-lookup"><span data-stu-id="1873a-109">1-25</span></span>  <br/> |<span data-ttu-id="1873a-110">La forma tiene distorsión de boceto aplicada, donde un valor de 1 es la mayor distorsión y 25 es el mínimo.</span><span class="sxs-lookup"><span data-stu-id="1873a-110">The shape has sketch distortion applied to it, where a value of 1 is the most distortion and 25 is the least.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1873a-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1873a-111">Remarks</span></span>

<span data-ttu-id="1873a-112">Para obtener una referencia a la celda **SketchAmount** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="1873a-112">To get a reference to the **SketchAmount** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1873a-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="1873a-113">Cell name:</span></span>  <br/> | <span data-ttu-id="1873a-114">SketchAmount</span><span class="sxs-lookup"><span data-stu-id="1873a-114">SketchAmount</span></span>  <br/> |
   
<span data-ttu-id="1873a-115">Para obtener una referencia desde un programa a la celda **SketchAmount** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1873a-115">To get a reference to the **SketchAmount** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1873a-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="1873a-116">Section index:</span></span>  <br/> |<span data-ttu-id="1873a-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1873a-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1873a-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="1873a-118">Row index:</span></span>  <br/> |<span data-ttu-id="1873a-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="1873a-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="1873a-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="1873a-120">Cell index:</span></span>  <br/> |<span data-ttu-id="1873a-121">**visSketchAmount**</span><span class="sxs-lookup"><span data-stu-id="1873a-121">**visSketchAmount**</span></span> <br/> |
   

