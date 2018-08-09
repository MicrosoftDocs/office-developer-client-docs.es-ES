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
ms.openlocfilehash: e9495eef837a61fa9b7ecb2b242fdabc5df30080
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823457"
---
# <a name="txtheight-cell-text-transform-section"></a><span data-ttu-id="a9387-104">Celda TxtHeight (sección Transformación de texto)</span><span class="sxs-lookup"><span data-stu-id="a9387-104">TxtHeight Cell (Text Transform Section)</span></span>

<span data-ttu-id="a9387-p102">Determina el alto del bloque de texto. La fórmula predeterminada es:</span><span class="sxs-lookup"><span data-stu-id="a9387-p102">Determines the height of the text block. The default formula is:</span></span>
  
<span data-ttu-id="a9387-107">= Alto \* 1</span><span class="sxs-lookup"><span data-stu-id="a9387-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a9387-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a9387-108">Remarks</span></span>

<span data-ttu-id="a9387-109">Para obtener una referencia a la celda TxtHeight por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="a9387-109">To get a reference to the TxtHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a9387-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="a9387-110">Cell name:</span></span>  <br/> | <span data-ttu-id="a9387-111">TxtHeight</span><span class="sxs-lookup"><span data-stu-id="a9387-111">TxtHeight</span></span>  <br/> |
   
<span data-ttu-id="a9387-112">Para obtener una referencia desde un programa a la celda TxtHeight por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a9387-112">To get a reference to the TxtHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a9387-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="a9387-113">Section index:</span></span>  <br/> |<span data-ttu-id="a9387-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a9387-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a9387-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="a9387-115">Row index:</span></span>  <br/> |<span data-ttu-id="a9387-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="a9387-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="a9387-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="a9387-117">Cell index:</span></span>  <br/> |<span data-ttu-id="a9387-118">**visXFormHeight**</span><span class="sxs-lookup"><span data-stu-id="a9387-118">**visXFormHeight**</span></span> <br/> |
   

