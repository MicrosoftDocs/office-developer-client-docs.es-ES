---
title: Celda TxtHeight (Sección de transformación de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1025
localization_priority: Normal
ms.assetid: cfa3ecc6-61a8-506c-ba1d-b5e1f757d44f
description: 'Determina el alto del bloque de texto. La fórmula predeterminada es:'
ms.openlocfilehash: 8ad17cdf1deca6c4aa81f3388d7c112b4e179e2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409310"
---
# <a name="txtheight-cell-text-transform-section"></a><span data-ttu-id="e8642-104">Celda TxtHeight (Sección de transformación de texto)</span><span class="sxs-lookup"><span data-stu-id="e8642-104">TxtHeight Cell (Text Transform Section)</span></span>

<span data-ttu-id="e8642-105">Determina el alto del bloque de texto.</span><span class="sxs-lookup"><span data-stu-id="e8642-105">Determines the height of the text block.</span></span> <span data-ttu-id="e8642-106">La fórmula predeterminada es:</span><span class="sxs-lookup"><span data-stu-id="e8642-106">The default formula is:</span></span>
  
<span data-ttu-id="e8642-107">= Altura \* 1</span><span class="sxs-lookup"><span data-stu-id="e8642-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e8642-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8642-108">Remarks</span></span>

<span data-ttu-id="e8642-109">Para obtener una referencia a la celda TxtHeight por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="e8642-109">To get a reference to the TxtHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e8642-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="e8642-110">Cell name:</span></span>  <br/> | <span data-ttu-id="e8642-111">TxtHeight</span><span class="sxs-lookup"><span data-stu-id="e8642-111">TxtHeight</span></span>  <br/> |
   
<span data-ttu-id="e8642-112">Para obtener una referencia desde un programa a la celda TxtHeight por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e8642-112">To get a reference to the TxtHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e8642-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="e8642-113">Section index:</span></span>  <br/> |<span data-ttu-id="e8642-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e8642-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e8642-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="e8642-115">Row index:</span></span>  <br/> |<span data-ttu-id="e8642-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="e8642-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="e8642-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="e8642-117">Cell index:</span></span>  <br/> |<span data-ttu-id="e8642-118">**visXFormHeight**</span><span class="sxs-lookup"><span data-stu-id="e8642-118">**visXFormHeight**</span></span> <br/> |
   

