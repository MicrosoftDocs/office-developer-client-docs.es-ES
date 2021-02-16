---
title: Celda LineJumpFactorX (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm545
localization_priority: Normal
ms.assetid: 0649672f-f496-ce80-6dc3-3affc9b6f913
description: Determina el tamaño de los saltos de línea en los conectores dinámicos horizontales de la página con respecto al valor de la celda LineToLineX. El valor de esta celda puede estar en el intervalo entre 0 y 10, pero se recomienda utilizar los valores fraccionarios entre 0 y 1.
ms.openlocfilehash: 8698d99021ca64415417de8e946cbd80b586e759
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424997"
---
# <a name="linejumpfactorx-cell-page-layout-section"></a><span data-ttu-id="56286-104">Celda LineJumpFactorX (sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="56286-104">LineJumpFactorX Cell (Page Layout Section)</span></span>

<span data-ttu-id="56286-p102">Determina el tamaño de los saltos de línea en los conectores dinámicos horizontales de la página con respecto al valor de la celda LineToLineX. El valor de esta celda puede estar en el intervalo entre 0 y 10, pero se recomienda utilizar los valores fraccionarios entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="56286-p102">Determines the size of line jumps on horizontal dynamic connectors on the page, relative to the value of the LineToLineX cell. The value of this cell can range from 0 to 10 but fractional values from 0 to 1 are suggested.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="56286-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="56286-107">Remarks</span></span>

<span data-ttu-id="56286-108">También puede establecer el valor de esta celda en la ficha **Diseño y enrutamiento** del cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página** y, a continuación, haga clic en **Diseño y enrutamiento**).</span><span class="sxs-lookup"><span data-stu-id="56286-108">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="56286-109">Para obtener una referencia a la celda LineJumpFactorX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="56286-109">To get a reference to the LineJumpFactorX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="56286-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="56286-110">Cell name:</span></span>  <br/> |<span data-ttu-id="56286-111">LineJumpFactorX</span><span class="sxs-lookup"><span data-stu-id="56286-111">LineJumpFactorX</span></span>  <br/> |
   
<span data-ttu-id="56286-112">Para obtener una referencia desde un programa a la celda LineJumpFactorX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="56286-112">To get a reference to the LineJumpFactorX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="56286-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="56286-113">Section index:</span></span>  <br/> |<span data-ttu-id="56286-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="56286-114">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="56286-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="56286-115">Row index:</span></span>  <br/> |<span data-ttu-id="56286-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="56286-116">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="56286-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="56286-117">Cell index:</span></span>  <br/> |<span data-ttu-id="56286-118">**visPLOJumpFactorX**</span><span class="sxs-lookup"><span data-stu-id="56286-118">**visPLOJumpFactorX**</span></span> <br/> |
   

