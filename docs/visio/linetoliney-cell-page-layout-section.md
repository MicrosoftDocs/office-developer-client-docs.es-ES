---
title: Celda LineToLineY (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm570
localization_priority: Normal
ms.assetid: db9a8232-25c5-7087-2ae9-50470d0cf16e
description: Determina el gálibo vertical entre todos los conectores de la página de dibujo.
ms.openlocfilehash: e98c3e05ffb1739f9b2739ce4e0ee8012afe2266
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358971"
---
# <a name="linetoliney-cell-page-layout-section"></a><span data-ttu-id="bfc99-103">Celda LineToLineY (Sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="bfc99-103">LineToLineY Cell (Page Layout Section)</span></span>

<span data-ttu-id="bfc99-104">Determina el gálibo vertical entre todos los conectores de la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="bfc99-104">Determines the vertical clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bfc99-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bfc99-105">Remarks</span></span>

<span data-ttu-id="bfc99-p101">También puede establecer el valor de esta celda en el cuadro de diálogo **Espaciado del diseño y el enrutamiento**. (En la ficha **Diseño**, haga clic en la flecha de **Configurar página**, haga clic en **Diseño y enrutamiento** y, a continuación, en **Espaciado**).</span><span class="sxs-lookup"><span data-stu-id="bfc99-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="bfc99-108">Para obtener una referencia a la celda LineToLineY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="bfc99-108">To get a reference to the LineToLineY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bfc99-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="bfc99-109">Cell name:</span></span>  <br/> |<span data-ttu-id="bfc99-110">LineToLineY</span><span class="sxs-lookup"><span data-stu-id="bfc99-110">LineToLineY</span></span>  <br/> |
   
<span data-ttu-id="bfc99-111">Para obtener una referencia desde un programa a la celda LineToLineY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="bfc99-111">To get a reference to the LineToLineY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bfc99-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="bfc99-112">Section index:</span></span>  <br/> |<span data-ttu-id="bfc99-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bfc99-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bfc99-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="bfc99-114">Row index:</span></span>  <br/> |<span data-ttu-id="bfc99-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="bfc99-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="bfc99-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="bfc99-116">Cell index:</span></span>  <br/> |<span data-ttu-id="bfc99-117">**visPLOLineToLineY**</span><span class="sxs-lookup"><span data-stu-id="bfc99-117">**visPLOLineToLineY**</span></span> <br/> |
   

