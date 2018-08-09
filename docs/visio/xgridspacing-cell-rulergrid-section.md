---
title: Celda XGridSpacing (sección Regla y cuadrícula)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1160
localization_priority: Normal
ms.assetid: e07dd983-7588-6317-944c-46da2bb65b31
description: Especifica la distancia entre las líneas horizontales de una cuadrícula fija (XGridDensity = 0).
ms.openlocfilehash: 5f461d02dae1574fe2b186b43166ef14d8251df2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823565"
---
# <a name="xgridspacing-cell-ruler-amp-grid-section"></a><span data-ttu-id="2189a-103">Celda XGridSpacing (sección Regla y cuadrícula)</span><span class="sxs-lookup"><span data-stu-id="2189a-103">XGridSpacing Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="2189a-104">Especifica la distancia entre las líneas horizontales de una cuadrícula fija (XGridDensity = 0).</span><span class="sxs-lookup"><span data-stu-id="2189a-104">Specifies the distance between horizontal lines in a fixed grid (XGridDensity = 0).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2189a-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2189a-105">Remarks</span></span>

<span data-ttu-id="2189a-106">Esta celda corresponde a la horizontal **Espaciado mínimo** de opción en la **regla &amp; cuadrícula** cuadro de diálogo (en la ficha **Ver** , haga clic en la flecha de **Mostrar** ).</span><span class="sxs-lookup"><span data-stu-id="2189a-106">This cell corresponds to the horizontal **Minimum spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="2189a-107">Para obtener una referencia a la celda XGridSpacing por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="2189a-107">To get a reference to the XGridSpacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2189a-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="2189a-108">Cell name:</span></span>  <br/> |<span data-ttu-id="2189a-109">XGridSpacing</span><span class="sxs-lookup"><span data-stu-id="2189a-109">XGridSpacing</span></span>  <br/> |
   
<span data-ttu-id="2189a-110">Para obtener una referencia desde un programa a la celda XGridSpacing por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2189a-110">To get a reference to the XGridSpacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2189a-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="2189a-111">Section index:</span></span>  <br/> |<span data-ttu-id="2189a-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2189a-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="2189a-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="2189a-113">Row index:</span></span>  <br/> |<span data-ttu-id="2189a-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="2189a-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="2189a-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="2189a-115">Cell index:</span></span>  <br/> |<span data-ttu-id="2189a-116">**visXGridSpacing**</span><span class="sxs-lookup"><span data-stu-id="2189a-116">**visXGridSpacing**</span></span> <br/> |
   

