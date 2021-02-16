---
title: Celda PagesX (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60064
localization_priority: Normal
ms.assetid: a10bf4c2-24f4-4c53-39ba-2b8cd5b50d2c
description: Determina el número de páginas impresas al que ajustar horizontalmente la página de dibujo.
ms.openlocfilehash: e912aef2277f5a7d2af5352897654ee986836c48
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438697"
---
# <a name="pagesx-cell-print-properties-section"></a><span data-ttu-id="f5f9a-103">Celda PagesX (Sección de propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="f5f9a-103">PagesX Cell (Print Properties Section)</span></span>

<span data-ttu-id="f5f9a-104">Determina el número de páginas impresas al que ajustar horizontalmente la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="f5f9a-104">Determines the number of printer pages on which to fit the drawing page horizontally.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f5f9a-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f5f9a-105">Remarks</span></span>

<span data-ttu-id="f5f9a-106">Este valor se utiliza sólo cuando la celda OnPage tiene el valor TRUE.</span><span class="sxs-lookup"><span data-stu-id="f5f9a-106">This value is used only when the OnPage cell is set to TRUE.</span></span> 
  
<span data-ttu-id="f5f9a-107">Para obtener una referencia a la celda PagesX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="f5f9a-107">To get a reference to the PagesX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f5f9a-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="f5f9a-108">Cell name:</span></span>  <br/> | <span data-ttu-id="f5f9a-109">PagesX</span><span class="sxs-lookup"><span data-stu-id="f5f9a-109">PagesX</span></span>  <br/> |
   
<span data-ttu-id="f5f9a-110">Para obtener una referencia desde un programa a la celda PagesX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f5f9a-110">To get a reference to the PagesX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f5f9a-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="f5f9a-111">Section index:</span></span>  <br/> |<span data-ttu-id="f5f9a-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f5f9a-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f5f9a-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="f5f9a-113">Row index:</span></span>  <br/> |<span data-ttu-id="f5f9a-114">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="f5f9a-114">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="f5f9a-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="f5f9a-115">Cell index:</span></span>  <br/> |<span data-ttu-id="f5f9a-116">**visPrintPropertiesPagesX**</span><span class="sxs-lookup"><span data-stu-id="f5f9a-116">**visPrintPropertiesPagesX**</span></span> <br/> |
   

