---
title: Celda NoSnap (Sección de Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm740
localization_priority: Normal
ms.assetid: 0e6c8621-868c-9eac-926b-3049f18023b0
description: Determina si otras formas se ajustan a un trazado.
ms.openlocfilehash: 111f3773cb1df9033ed5a7b0b146d40ce6b26df0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822687"
---
# <a name="nosnap-cell-geometry-section"></a><span data-ttu-id="0f7a5-103">Celda NoSnap (sección Geometría)</span><span class="sxs-lookup"><span data-stu-id="0f7a5-103">NoSnap Cell (Geometry Section)</span></span>

<span data-ttu-id="0f7a5-104">Determina si otras formas se ajustan a un trazado.</span><span class="sxs-lookup"><span data-stu-id="0f7a5-104">Determines whether other shapes snap to a path.</span></span>
  
|<span data-ttu-id="0f7a5-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0f7a5-105">**Value**</span></span>|<span data-ttu-id="0f7a5-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0f7a5-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="0f7a5-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="0f7a5-107">TRUE</span></span>  <br/> | <span data-ttu-id="0f7a5-108">No se permite que otras formas se ajusten a este trazado.</span><span class="sxs-lookup"><span data-stu-id="0f7a5-108">Do not allow other shapes to snap to this path.</span></span>  <br/> |
| <span data-ttu-id="0f7a5-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="0f7a5-109">FALSE</span></span>  <br/> | <span data-ttu-id="0f7a5-110">Se permite que otras formas se ajusten a este trazado.</span><span class="sxs-lookup"><span data-stu-id="0f7a5-110">Allow other shapes to snap to this path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f7a5-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0f7a5-111">Remarks</span></span>

<span data-ttu-id="0f7a5-112">Para obtener una referencia a la celda NoSnap por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="0f7a5-112">To get a reference to the NoSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0f7a5-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="0f7a5-113">Cell name:</span></span>  <br/> | <span data-ttu-id="0f7a5-114">Geometría *i* . NoSnap donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0f7a5-114">Geometry  *i*  .NoSnap            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0f7a5-115">Para obtener una referencia desde un programa a la celda NoSnap por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="0f7a5-115">To get a reference to the NoSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0f7a5-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="0f7a5-116">Section index:</span></span>  <br/> |<span data-ttu-id="0f7a5-117">**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0f7a5-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0f7a5-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="0f7a5-118">Row index:</span></span>  <br/> |<span data-ttu-id="0f7a5-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="0f7a5-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="0f7a5-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="0f7a5-120">Cell index:</span></span>  <br/> |<span data-ttu-id="0f7a5-121">**visCompNoSnap**</span><span class="sxs-lookup"><span data-stu-id="0f7a5-121">**visCompNoSnap**</span></span> <br/> |
   

