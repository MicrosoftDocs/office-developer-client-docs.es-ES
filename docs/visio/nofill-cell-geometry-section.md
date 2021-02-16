---
title: Celda NoFill (Sección de Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm710
localization_priority: Normal
ms.assetid: 0ba7f6da-681b-b749-fe72-afbca23d7e16
description: Indica si un trazado puede rellenarse.
ms.openlocfilehash: 301f30b644e338ff9e597a7a7d8226b9c8a4462f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415022"
---
# <a name="nofill-cell-geometry-section"></a><span data-ttu-id="e4363-103">Celda NoFill (Sección de Geometría)</span><span class="sxs-lookup"><span data-stu-id="e4363-103">NoFill Cell (Geometry Section)</span></span>

<span data-ttu-id="e4363-104">Indica si un trazado puede rellenarse.</span><span class="sxs-lookup"><span data-stu-id="e4363-104">Indicates whether a path can be filled.</span></span>
  
|<span data-ttu-id="e4363-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e4363-105">**Value**</span></span>|<span data-ttu-id="e4363-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e4363-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e4363-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e4363-107">TRUE</span></span>  <br/> | <span data-ttu-id="e4363-108">El trazado no se rellena aunque otros trazados de la forma estén rellenos.</span><span class="sxs-lookup"><span data-stu-id="e4363-108">The path is not filled even if other paths in the shape are filled.</span></span>  <br/> |
| <span data-ttu-id="e4363-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e4363-109">FALSE</span></span>  <br/> | <span data-ttu-id="e4363-110">El relleno de la forma se aplica al trazado, aunque no esté cerrado.</span><span class="sxs-lookup"><span data-stu-id="e4363-110">The shape's fill applies to the path, even if it isn't closed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4363-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e4363-111">Remarks</span></span>

<span data-ttu-id="e4363-p101">Si establece la trama de relleno de una forma a cero, ninguno de sus trazados se rellena. Esta celda se utiliza para desactivar el relleno de manera selectiva para un trazado dentro de una forma.</span><span class="sxs-lookup"><span data-stu-id="e4363-p101">If you set a shape's fill pattern to none (0), none of its paths are filled. This cell is used to turn the fill off selectively for a path within a shape.</span></span>
  
<span data-ttu-id="e4363-114">Para obtener una referencia a la celda NoFill por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="e4363-114">To get a reference to the NoFill cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e4363-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="e4363-115">Cell name:</span></span>  <br/> | <span data-ttu-id="e4363-116">Geometría  *i*  . NoFill donde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e4363-116">Geometry  *i*  .NoFill            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e4363-117">Para obtener una referencia desde un programa a la celda NoFill por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e4363-117">To get a reference to the NoFill cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e4363-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="e4363-118">Section index:</span></span>  <br/> |<span data-ttu-id="e4363-119">**visSectionFirstComponent**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e4363-119">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e4363-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="e4363-120">Row index:</span></span>  <br/> |<span data-ttu-id="e4363-121">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="e4363-121">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="e4363-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="e4363-122">Cell index:</span></span>  <br/> |<span data-ttu-id="e4363-123">**visCompNoFill**</span><span class="sxs-lookup"><span data-stu-id="e4363-123">**visCompNoFill**</span></span> <br/> |
   

