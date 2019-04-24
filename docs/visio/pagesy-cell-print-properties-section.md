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
ms.openlocfilehash: 43d4081439525c516d3da28b6c0e46e9273d85c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339980"
---
# <a name="pagesy-cell-print-properties-section"></a><span data-ttu-id="21338-103">Celda PagesY (Sección de propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="21338-103">PagesY Cell (Print Properties Section)</span></span>

<span data-ttu-id="21338-104">Determina el número de páginas impresas al que ajustar verticalmente la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="21338-104">Determines the number of printer pages on which to fit the drawing page vertically.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="21338-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="21338-105">Remarks</span></span>

<span data-ttu-id="21338-106">Este valor se utiliza sólo cuando la celda OnPage tiene el valor TRUE.</span><span class="sxs-lookup"><span data-stu-id="21338-106">This value is used only when the OnPage cell is set to TRUE.</span></span> 
  
<span data-ttu-id="21338-107">Para obtener una referencia a la celda PagesY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="21338-107">To get a reference to the PagesY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="21338-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="21338-108">Cell name:</span></span>  <br/> | <span data-ttu-id="21338-109">PagesY</span><span class="sxs-lookup"><span data-stu-id="21338-109">PagesY</span></span>  <br/> |
   
<span data-ttu-id="21338-110">Para obtener una referencia desde un programa a la celda PagesY por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="21338-110">To get a reference to the PagesY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="21338-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="21338-111">Section index:</span></span>  <br/> |<span data-ttu-id="21338-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="21338-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="21338-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="21338-113">Row index:</span></span>  <br/> |<span data-ttu-id="21338-114">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="21338-114">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="21338-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="21338-115">Cell index:</span></span>  <br/> |<span data-ttu-id="21338-116">**visPrintPropertiesPagesY**</span><span class="sxs-lookup"><span data-stu-id="21338-116">**visPrintPropertiesPagesY**</span></span> <br/> |
   

