---
title: Celda LockRotate (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm655
localization_priority: Normal
ms.assetid: 2d97b31d-9008-307d-273a-1726007eeb34
description: Bloquea las formas bidimensionales para que no se puedan girar con los controladores de rotación ni con los comandos Girar 90 a la izquierda o Girar 90 a la derecha.
ms.openlocfilehash: 36da1868e4f974bd19d00e86e31bea96eb8ad5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404676"
---
# <a name="lockrotate-cell-protection-section"></a><span data-ttu-id="d8cb4-103">Celda LockRotate (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="d8cb4-103">LockRotate Cell (Protection Section)</span></span>

<span data-ttu-id="d8cb4-104">Bloquea las formas bidimensionales para que no se puedan girar con los controladores de rotación ni con los comandos **Girar 90 a la izquierda** o **Girar 90 a la derecha**.</span><span class="sxs-lookup"><span data-stu-id="d8cb4-104">Locks 2-D shapes against being rotated with the rotation handle or the **Rotate Left 90°** or **Rotate Right 90°** command.</span></span> 
  
|<span data-ttu-id="d8cb4-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d8cb4-105">**Value**</span></span>|<span data-ttu-id="d8cb4-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d8cb4-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d8cb4-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d8cb4-107">TRUE</span></span>  <br/> | <span data-ttu-id="d8cb4-108">La forma no se puede girar.</span><span class="sxs-lookup"><span data-stu-id="d8cb4-108">Shape cannot be rotated.</span></span>  <br/> |
| <span data-ttu-id="d8cb4-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d8cb4-109">FALSE</span></span>  <br/> | <span data-ttu-id="d8cb4-110">La forma se puede girar (opción predeterminada).</span><span class="sxs-lookup"><span data-stu-id="d8cb4-110">Shape can be rotated (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8cb4-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d8cb4-111">Remarks</span></span>

<span data-ttu-id="d8cb4-p101">La celda LockRotate no impide que las formas unidimensionales se puedan girar al arrastrar un extremo. Para bloquear la rotación de las formas unidimensionales, establezca la celda LockWidth en un valor distinto de cero (TRUE).</span><span class="sxs-lookup"><span data-stu-id="d8cb4-p101">The LockRotate cell does not prevent a 1-D shape from being rotated when an endpoint is dragged. To lock a 1-D shape against rotation, set the LockWidth cell to a non-zero value (TRUE).</span></span>
  
<span data-ttu-id="d8cb4-114">Para obtener una referencia a la celda LockRotate por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="d8cb4-114">To get a reference to the LockRotate cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d8cb4-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="d8cb4-115">Cell name:</span></span>  <br/> | <span data-ttu-id="d8cb4-116">LockRotate</span><span class="sxs-lookup"><span data-stu-id="d8cb4-116">LockRotate</span></span>  <br/> |
   
<span data-ttu-id="d8cb4-117">Para obtener una referencia desde un programa a la celda LockRotate por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d8cb4-117">To get a reference to the LockRotate cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d8cb4-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="d8cb4-118">Section index:</span></span>  <br/> |<span data-ttu-id="d8cb4-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d8cb4-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d8cb4-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="d8cb4-120">Row index:</span></span>  <br/> |<span data-ttu-id="d8cb4-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="d8cb4-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="d8cb4-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="d8cb4-122">Cell index:</span></span>  <br/> |<span data-ttu-id="d8cb4-123">**visLockRotate**</span><span class="sxs-lookup"><span data-stu-id="d8cb4-123">**visLockRotate**</span></span> <br/> |
   

