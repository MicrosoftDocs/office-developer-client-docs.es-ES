---
title: Celda AvenueSizeX (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm65
localization_priority: Normal
ms.assetid: 86fe25ed-590d-b2f0-5dfe-9746a19c6b04
description: Determina la cantidad de espacio horizontal entre las formas de la página de dibujo al establecer formas mediante el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en Re-Layout Página y, a continuación, haga clic en Más opciones de diseño).
ms.openlocfilehash: 28eea2589e34c7793e89e01495eb519b987553a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411648"
---
# <a name="avenuesizex-cell-page-layout-section"></a><span data-ttu-id="b1b00-103">Celda AvenueSizeX (Sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="b1b00-103">AvenueSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="b1b00-104">Determina la cantidad de espacio horizontal entre las formas de la página de dibujo al  establecer formas  mediante el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en Volver a diseñar página y, a continuación, haga clic en \*\* Más opciones de diseño \*\*). </span><span class="sxs-lookup"><span data-stu-id="b1b00-104">Determines the amount of horizontal space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click \*\* More Layout Options \*\*).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b1b00-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b1b00-105">Remarks</span></span>

<span data-ttu-id="b1b00-106">También puede establecer este valor en el cuadro de diálogo **Espaciado del diseño y el enrutamiento** (en la ficha **Diseño**, haga clic en la flecha del grupo **Configurar página**, haga clic en la pestaña **Diseño y enrutamiento** y, a continuación, en **Espaciado**).</span><span class="sxs-lookup"><span data-stu-id="b1b00-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="b1b00-p101">La cuadrícula dinámica emplea la configuración de la celda AvenueSizeX cuando solo hay una forma disponible para calcular el espacio horizontal. Para usar la cuadrícula dinámica, en la ficha **Ver**, en el grupo **Ayudas visuales**, seleccione **Cuadrícula dinámica**.</span><span class="sxs-lookup"><span data-stu-id="b1b00-p101">The dynamic grid uses the setting in the AvenueSizeX cell when only one shape is available for calculating horizontal spacing. To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="b1b00-109">Para obtener una referencia a la celda AvenueSizeX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="b1b00-109">To get a reference to the AvenueSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b1b00-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b1b00-110">Cell name:</span></span>  <br/> | <span data-ttu-id="b1b00-111">AvenueSizeY</span><span class="sxs-lookup"><span data-stu-id="b1b00-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="b1b00-112">Para obtener una referencia desde un programa a la celda AvenueSizeX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b1b00-112">To get a reference to the AvenueSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b1b00-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b1b00-113">Section index:</span></span>  <br/> |<span data-ttu-id="b1b00-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b1b00-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b1b00-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b1b00-115">Row index:</span></span>  <br/> |<span data-ttu-id="b1b00-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="b1b00-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="b1b00-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b1b00-117">Cell index:</span></span>  <br/> |<span data-ttu-id="b1b00-118">**visPLOAvenueSizeX**</span><span class="sxs-lookup"><span data-stu-id="b1b00-118">**visPLOAvenueSizeX**</span></span> <br/> |
   

