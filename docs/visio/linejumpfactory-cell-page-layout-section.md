---
title: Celda LineJumpFactorY (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm550
localization_priority: Normal
ms.assetid: 5a14be0d-9e3c-23c4-7782-bda5470d1243
description: Determina el tamaño de los saltos de línea en los conectores dinámicos verticales de la página con respecto al valor de la celda LineToLineY. El valor de esta celda puede estar en el intervalo entre 0 y 10, pero se recomienda utilizar los valores fraccionarios entre 0 y 1.
ms.openlocfilehash: 36712c1558ff2f50309dc31e8f918061180c8fa4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316460"
---
# <a name="linejumpfactory-cell-page-layout-section"></a><span data-ttu-id="91df0-104">Celda LineJumpFactorY (sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="91df0-104">LineJumpFactorY Cell (Page Layout Section)</span></span>

<span data-ttu-id="91df0-p102">Determina el tamaño de los saltos de línea en los conectores dinámicos verticales de la página con respecto al valor de la celda LineToLineY. El valor de esta celda puede estar en el intervalo entre 0 y 10, pero se recomienda utilizar los valores fraccionarios entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="91df0-p102">Determines the size of line jumps on vertical dynamic connectors on the page, relative to the value of the LineToLineY cell. The value of this cell can range from 0 to 10 but fractional values from 0 to 1 are suggested.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="91df0-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="91df0-107">Remarks</span></span>

<span data-ttu-id="91df0-108">También puede establecer el valor de esta celda en la ficha **Diseño y enrutamiento** del cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página** y, a continuación, haga clic en **Diseño y enrutamiento**).</span><span class="sxs-lookup"><span data-stu-id="91df0-108">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="91df0-109">Para obtener una referencia a la celda LineJumpFactorY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="91df0-109">To get a reference to the LineJumpFactorY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="91df0-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="91df0-110">Cell name:</span></span>  <br/> |<span data-ttu-id="91df0-111">LineJumpFactorY</span><span class="sxs-lookup"><span data-stu-id="91df0-111">LineJumpFactorY</span></span>  <br/> |
   
<span data-ttu-id="91df0-112">Para obtener una referencia desde un programa a la celda LineJumpFactorY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="91df0-112">To get a reference to the LineJumpFactorY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="91df0-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="91df0-113">Section index:</span></span>  <br/> |<span data-ttu-id="91df0-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="91df0-114">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="91df0-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="91df0-115">Row index:</span></span>  <br/> |<span data-ttu-id="91df0-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="91df0-116">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="91df0-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="91df0-117">Cell index:</span></span>  <br/> |<span data-ttu-id="91df0-118">**visPLOJumpFactorY**</span><span class="sxs-lookup"><span data-stu-id="91df0-118">**visPLOJumpFactorY**</span></span> <br/> |
   

