---
title: Celda NoQuickDrag (sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80004
localization_priority: Normal
ms.assetid: 8491f459-9de2-8e75-5532-7d3bd0986734
description: Determina si una forma se puede seleccionar o arrastrar cuando el usuario hace clic en el área rellena definida por la sección Geometry.
ms.openlocfilehash: d60268685d93ae88abb2840f62b093db1e688c2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417724"
---
# <a name="noquickdrag-cell-geometry-section"></a><span data-ttu-id="0be9c-103">Celda NoQuickDrag (sección de geometría)</span><span class="sxs-lookup"><span data-stu-id="0be9c-103">NoQuickDrag Cell (Geometry Section)</span></span>

<span data-ttu-id="0be9c-104">Determina si una forma se puede seleccionar o arrastrar cuando el usuario hace clic en el área rellena definida por la sección Geometry.</span><span class="sxs-lookup"><span data-stu-id="0be9c-104">Determines whether a shape can be selected or dragged when the user clicks the filled area defined by the Geometry section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0be9c-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0be9c-105">Remarks</span></span>

<span data-ttu-id="0be9c-106">Para obtener una referencia a la celda NoQuickDrag por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="0be9c-106">To get a reference to the NoQuickDrag cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0be9c-107">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="0be9c-107">Cell name:</span></span>  <br/> |<span data-ttu-id="0be9c-108">Geometría *i* . NoQuickDrag, donde \* i \*-<1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0be9c-108">Geometry  *i*  .NoQuickDrag, where  \* i \*  - <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0be9c-109">Para obtener una referencia desde un programa a la celda NoQuickDrag por su índice, use la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="0be9c-109">To get a reference to the NoQuickDrag cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0be9c-110">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="0be9c-110">Section index:</span></span>  <br/> |<span data-ttu-id="0be9c-111">**visSectionFirstComponent** +  *i* , donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0be9c-111">**visSectionFirstComponent** +  *i*  , where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="0be9c-112">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="0be9c-112">Row index:</span></span>  <br/> |<span data-ttu-id="0be9c-113">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="0be9c-113">**visRowComponent**</span></span> <br/> |
|<span data-ttu-id="0be9c-114">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="0be9c-114">Cell index:</span></span>  <br/> |<span data-ttu-id="0be9c-115">**visCompNoQuickDrag**</span><span class="sxs-lookup"><span data-stu-id="0be9c-115">**visCompNoQuickDrag**</span></span> <br/> |
   

