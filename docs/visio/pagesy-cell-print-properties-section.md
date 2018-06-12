---
title: Celda PagesY (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033790
localization_priority: Normal
ms.assetid: 396a0f3e-dbbb-3f5b-3c5d-f7dd454a765f
description: Determina el número de páginas impresas al que ajustar verticalmente la página de dibujo.
ms.openlocfilehash: 1663fac8efdf06599d1e3c00d5eb0d00ec52e476
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822720"
---
# <a name="pagesy-cell-print-properties-section"></a><span data-ttu-id="c73af-103">Celda PagesY (Sección de propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="c73af-103">PagesY Cell (Print Properties Section)</span></span>

<span data-ttu-id="c73af-104">Determina el número de páginas impresas al que ajustar verticalmente la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="c73af-104">Determines the number of printer pages on which to fit the drawing page vertically.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c73af-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c73af-105">Remarks</span></span>

<span data-ttu-id="c73af-106">Este valor se utiliza sólo cuando la celda OnPage tiene el valor TRUE.</span><span class="sxs-lookup"><span data-stu-id="c73af-106">This value is used only when the OnPage cell is set to TRUE.</span></span> 
  
<span data-ttu-id="c73af-107">Para obtener una referencia a la celda PagesY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="c73af-107">To get a reference to the PagesY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c73af-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c73af-108">Cell name:</span></span>  <br/> | <span data-ttu-id="c73af-109">PagesY</span><span class="sxs-lookup"><span data-stu-id="c73af-109">PagesY</span></span>  <br/> |
   
<span data-ttu-id="c73af-110">Para obtener una referencia a la celda PagesY por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c73af-110">To get a reference to the PagesY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c73af-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c73af-111">Section index:</span></span>  <br/> |<span data-ttu-id="c73af-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c73af-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c73af-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c73af-113">Row index:</span></span>  <br/> |<span data-ttu-id="c73af-114">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="c73af-114">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="c73af-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c73af-115">Cell index:</span></span>  <br/> |<span data-ttu-id="c73af-116">**visPrintPropertiesPagesY**</span><span class="sxs-lookup"><span data-stu-id="c73af-116">**visPrintPropertiesPagesY**</span></span> <br/> |
   

