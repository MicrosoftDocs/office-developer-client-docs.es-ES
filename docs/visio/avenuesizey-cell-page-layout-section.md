---
title: Celda AvenueSizeY (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm70
localization_priority: Normal
ms.assetid: 9ff2893c-afe5-505e-0b55-48ec1de08a5f
description: Determina la cantidad de espacio vertical entre las formas en la página de dibujo cuando se diseñan formas mediante el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en página de diseño de Re y, a continuación, haga clic en más opciones de diseño).
ms.openlocfilehash: af4089a3b215efaf49b8a45929ca94799fffcba5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821553"
---
# <a name="avenuesizey-cell-page-layout-section"></a><span data-ttu-id="3a77a-103">Celda AvenueSizeY (sección Diseño de página)</span><span class="sxs-lookup"><span data-stu-id="3a77a-103">AvenueSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="3a77a-104">Determina la cantidad de espacio vertical entre las formas en la página de dibujo cuando se diseñan formas mediante el cuadro de diálogo **Configurar diseño** (en la ficha **Diseño** , en el grupo **Diseño** , haga clic en página de **Diseño de Re** y, a continuación, haga clic en **más Opciones de diseño**).</span><span class="sxs-lookup"><span data-stu-id="3a77a-104">Determines the amount of vertical space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3a77a-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3a77a-105">Remarks</span></span>

<span data-ttu-id="3a77a-106">También puede establecer este valor en el cuadro de diálogo **Espaciado del diseño y el enrutamiento** (en la ficha **Diseño**, haga clic en la flecha en el grupo **Configurar página**, haga clic en la pestaña **Diseño y enrutamiento** y, a continuación, en **Espaciado**).</span><span class="sxs-lookup"><span data-stu-id="3a77a-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="3a77a-p101">La cuadrícula dinámica emplea la configuración de la celda AvenueSizeY cuando solo hay una forma disponible para calcular el espacio vertical. Para usar la cuadrícula dinámica, en la ficha **Ajustar y pegar**, en el grupo **Herramientas**, seleccione **Cuadrícula dinámica**.</span><span class="sxs-lookup"><span data-stu-id="3a77a-p101">The dynamic grid uses the setting in the AvenueSizeY cell when only one shape is available for calculating vertical spacing. To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="3a77a-109">Para obtener una referencia a la celda AvenueSizeY por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="3a77a-109">To get a reference to the AvenueSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3a77a-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="3a77a-110">Cell name:</span></span>  <br/> | <span data-ttu-id="3a77a-111">AvenueSizeY</span><span class="sxs-lookup"><span data-stu-id="3a77a-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="3a77a-112">Para obtener una referencia desde un programa a la celda AvenueSizeY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3a77a-112">To get a reference to the AvenueSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3a77a-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="3a77a-113">Section index:</span></span>  <br/> |<span data-ttu-id="3a77a-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3a77a-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3a77a-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="3a77a-115">Row index:</span></span>  <br/> |<span data-ttu-id="3a77a-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="3a77a-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="3a77a-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="3a77a-117">Cell index:</span></span>  <br/> |<span data-ttu-id="3a77a-118">**visPLOAvenueSizeY**</span><span class="sxs-lookup"><span data-stu-id="3a77a-118">**visPLOAvenueSizeY**</span></span> <br/> |
   

