---
title: Celda TxtWidth (Sección de transformación de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251270
localization_priority: Normal
ms.assetid: e2215c67-25fa-1d75-9cce-f126bb8760a1
description: 'Determina el ancho del bloque de texto. La fórmula predeterminada es:'
ms.openlocfilehash: 806307166035ebc2f8e20e7025d5ecb03c4d6e79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426096"
---
# <a name="txtwidth-cell-text-transform-section"></a><span data-ttu-id="b8c6d-104">Celda TxtWidth (Sección de transformación de texto)</span><span class="sxs-lookup"><span data-stu-id="b8c6d-104">TxtWidth Cell (Text Transform Section)</span></span>

<span data-ttu-id="b8c6d-105">Determina el ancho del bloque de texto.</span><span class="sxs-lookup"><span data-stu-id="b8c6d-105">Determines the width of the text block.</span></span> <span data-ttu-id="b8c6d-106">La fórmula predeterminada es:</span><span class="sxs-lookup"><span data-stu-id="b8c6d-106">The default formula is:</span></span>
  
<span data-ttu-id="b8c6d-107">= Ancho \* 1</span><span class="sxs-lookup"><span data-stu-id="b8c6d-107">= Width \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b8c6d-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b8c6d-108">Remarks</span></span>

<span data-ttu-id="b8c6d-109">Para obtener una referencia a la celda TxtWidth por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="b8c6d-109">To get a reference to the TxtWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b8c6d-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b8c6d-110">Cell name:</span></span>  <br/> | <span data-ttu-id="b8c6d-111">TxtWidth</span><span class="sxs-lookup"><span data-stu-id="b8c6d-111">TxtWidth</span></span>  <br/> |
   
<span data-ttu-id="b8c6d-112">Para obtener una referencia desde un programa a la celda TxtWidth por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b8c6d-112">To get a reference to the TxtWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b8c6d-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b8c6d-113">Section index:</span></span>  <br/> |<span data-ttu-id="b8c6d-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b8c6d-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b8c6d-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b8c6d-115">Row index:</span></span>  <br/> |<span data-ttu-id="b8c6d-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="b8c6d-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="b8c6d-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b8c6d-117">Cell index:</span></span>  <br/> |<span data-ttu-id="b8c6d-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="b8c6d-118">**visXFormWidth**</span></span> <br/> |
   

