---
title: Celda XGridOrigin (sección &amp; regla y cuadrícula)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1155
localization_priority: Normal
ms.assetid: 2b1a8902-b1d4-c3d9-8c9f-1a28fddacc59
description: Especifica la coordenada horizontal del origen de la cuadrícula.
ms.openlocfilehash: ee58ea7d950dd7e422f8a60a13bac8aa4ed353a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322312"
---
# <a name="xgridorigin-cell-ruler-amp-grid-section"></a><span data-ttu-id="c5cea-103">Celda XGridOrigin (sección &amp; regla y cuadrícula)</span><span class="sxs-lookup"><span data-stu-id="c5cea-103">XGridOrigin Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="c5cea-104">Especifica la coordenada horizontal del origen de la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="c5cea-104">Specifies the horizontal coordinate of the grid origin.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c5cea-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c5cea-105">Remarks</span></span>

<span data-ttu-id="c5cea-106">Esta celda corresponde a la opción **origen** de la cuadrícula horizontal del cuadro de diálogo **regla &amp; y cuadrícula** (en la ficha **Ver** , haga clic en la flecha de **Mostrar** .</span><span class="sxs-lookup"><span data-stu-id="c5cea-106">This cell corresponds to the horizontal **Grid origin** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow.</span></span> 
  
<span data-ttu-id="c5cea-107">Para obtener una referencia a la celda XGridOrigin por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="c5cea-107">To get a reference to the XGridOrigin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c5cea-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c5cea-108">Cell name:</span></span>  <br/> |<span data-ttu-id="c5cea-109">XGridOrigin</span><span class="sxs-lookup"><span data-stu-id="c5cea-109">XGridOrigin</span></span>  <br/> |
   
<span data-ttu-id="c5cea-110">Para obtener una referencia desde un programa a la celda XGridOrigin por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c5cea-110">To get a reference to the XGridOrigin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c5cea-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c5cea-111">Section index:</span></span>  <br/> |<span data-ttu-id="c5cea-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c5cea-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c5cea-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c5cea-113">Row index:</span></span>  <br/> |<span data-ttu-id="c5cea-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="c5cea-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="c5cea-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c5cea-115">Cell index:</span></span>  <br/> |<span data-ttu-id="c5cea-116">**visXGridOrigin**</span><span class="sxs-lookup"><span data-stu-id="c5cea-116">**visXGridOrigin**</span></span> <br/> |
   

