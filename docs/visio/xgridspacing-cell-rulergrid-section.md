---
title: Celda XGridSpacing (sección &amp; regla y cuadrícula)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1160
localization_priority: Normal
ms.assetid: e07dd983-7588-6317-944c-46da2bb65b31
description: Especifica la distancia entre las líneas horizontales de una cuadrícula fija (XGridDensity = 0).
ms.openlocfilehash: 05b68a9721dbfc9c03402d384d976c42ef05b134
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435078"
---
# <a name="xgridspacing-cell-ruler-amp-grid-section"></a><span data-ttu-id="4c164-103">Celda XGridSpacing (sección &amp; regla y cuadrícula)</span><span class="sxs-lookup"><span data-stu-id="4c164-103">XGridSpacing Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="4c164-104">Especifica la distancia entre las líneas horizontales de una cuadrícula fija (XGridDensity = 0).</span><span class="sxs-lookup"><span data-stu-id="4c164-104">Specifies the distance between horizontal lines in a fixed grid (XGridDensity = 0).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4c164-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4c164-105">Remarks</span></span>

<span data-ttu-id="4c164-106">Esta celda corresponde a la opción **espaciaDo mínimo** horizontal del cuadro de diálogo **regla &amp; y cuadrícula** (en la ficha **Ver** , haga clic en la flecha de **Mostrar** ).</span><span class="sxs-lookup"><span data-stu-id="4c164-106">This cell corresponds to the horizontal **Minimum spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="4c164-107">Para obtener una referencia a la celda XGridSpacing por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="4c164-107">To get a reference to the XGridSpacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c164-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="4c164-108">Cell name:</span></span>  <br/> |<span data-ttu-id="4c164-109">XGridSpacing</span><span class="sxs-lookup"><span data-stu-id="4c164-109">XGridSpacing</span></span>  <br/> |
   
<span data-ttu-id="4c164-110">Para obtener una referencia desde un programa a la celda XGridSpacing por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4c164-110">To get a reference to the XGridSpacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c164-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="4c164-111">Section index:</span></span>  <br/> |<span data-ttu-id="4c164-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4c164-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4c164-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="4c164-113">Row index:</span></span>  <br/> |<span data-ttu-id="4c164-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="4c164-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="4c164-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="4c164-115">Cell index:</span></span>  <br/> |<span data-ttu-id="4c164-116">**visXGridSpacing**</span><span class="sxs-lookup"><span data-stu-id="4c164-116">**visXGridSpacing**</span></span> <br/> |
   

