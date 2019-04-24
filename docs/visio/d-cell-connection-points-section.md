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
ms.openlocfilehash: e7bd61b8bc7a1a3b765af738681d958e2c83ba05
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345090"
---
# <a name="d-cell-connection-points-section"></a><span data-ttu-id="821c8-103">Celda D (Sección de puntos de conexión)</span><span class="sxs-lookup"><span data-stu-id="821c8-103">D Cell (Connection Points Section)</span></span>

<span data-ttu-id="821c8-104">Celda de borrador que se puede utilizar para escribir o probar fórmulas.</span><span class="sxs-lookup"><span data-stu-id="821c8-104">A scratch cell that you can use for entering or testing formulas.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="821c8-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="821c8-105">Remarks</span></span>

<span data-ttu-id="821c8-106">Para obtener acceso a la celda D, haga clic con el botón secundario en una fila y, a continuación, haga clic en **Cambiar tipo de fila** en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="821c8-106">To access the D cell, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  
<span data-ttu-id="821c8-107">Para obtener una referencia a la celda D por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="821c8-107">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="821c8-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="821c8-108">Cell name:</span></span>  <br/> | <span data-ttu-id="821c8-109">Connections. D [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="821c8-109">Connections.D[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="821c8-110">Para obtener una referencia desde un programa a la celda D por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="821c8-110">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="821c8-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="821c8-111">Section index:</span></span>  <br/> |<span data-ttu-id="821c8-112">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="821c8-112">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="821c8-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="821c8-113">Row index:</span></span>  <br/> |<span data-ttu-id="821c8-114">**visRowConnectionPts** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="821c8-114">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="821c8-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="821c8-115">Cell index:</span></span>  <br/> |<span data-ttu-id="821c8-116">**visCnnctD**</span><span class="sxs-lookup"><span data-stu-id="821c8-116">**visCnnctD**</span></span> <br/> |
   

