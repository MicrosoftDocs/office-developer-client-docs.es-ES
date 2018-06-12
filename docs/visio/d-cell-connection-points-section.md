---
title: Celda D (Sección de puntos de conexión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm205
localization_priority: Normal
ms.assetid: 28b18e8d-fecf-a798-813e-c1a310002244
description: Celda de borrador que se puede utilizar para escribir o probar fórmulas.
ms.openlocfilehash: 21c81c7a0a64c3016d8cff3b33d83ce785dc24eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821904"
---
# <a name="d-cell-connection-points-section"></a><span data-ttu-id="3ab2e-103">Celda D (Sección de puntos de conexión)</span><span class="sxs-lookup"><span data-stu-id="3ab2e-103">D Cell (Connection Points Section)</span></span>

<span data-ttu-id="3ab2e-104">Celda de borrador que se puede utilizar para escribir o probar fórmulas.</span><span class="sxs-lookup"><span data-stu-id="3ab2e-104">A scratch cell that you can use for entering or testing formulas.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3ab2e-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3ab2e-105">Remarks</span></span>

<span data-ttu-id="3ab2e-106">Para obtener acceso a la celda D, haga clic en una fila y, a continuación, haga clic en **Cambiar tipo de fila** en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="3ab2e-106">To access the D cell, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  
<span data-ttu-id="3ab2e-107">Para obtener una referencia a la celda D por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="3ab2e-107">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3ab2e-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="3ab2e-108">Cell name:</span></span>  <br/> | <span data-ttu-id="3ab2e-109">Connections.D [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="3ab2e-109">Connections.D[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="3ab2e-110">Para obtener una referencia a la celda D por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3ab2e-110">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3ab2e-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="3ab2e-111">Section index:</span></span>  <br/> |<span data-ttu-id="3ab2e-112">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="3ab2e-112">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="3ab2e-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="3ab2e-113">Row index:</span></span>  <br/> |<span data-ttu-id="3ab2e-114">**visRowConnectionPts** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3ab2e-114">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3ab2e-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="3ab2e-115">Cell index:</span></span>  <br/> |<span data-ttu-id="3ab2e-116">**visCnnctD**</span><span class="sxs-lookup"><span data-stu-id="3ab2e-116">**visCnnctD**</span></span> <br/> |
   

