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
ms.openlocfilehash: 781d166fe0b81cc2402fde2894cd1d0480a0895f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822468"
---
# <a name="linetoliney-cell-page-layout-section"></a><span data-ttu-id="a35c8-103">Celda LineToLineY (sección Diseño de página)</span><span class="sxs-lookup"><span data-stu-id="a35c8-103">LineToLineY Cell (Page Layout Section)</span></span>

<span data-ttu-id="a35c8-104">Determina el gálibo vertical entre todos los conectores de la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="a35c8-104">Determines the vertical clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a35c8-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a35c8-105">Remarks</span></span>

<span data-ttu-id="a35c8-p101">También puede establecer el valor de esta celda en el cuadro de diálogo **Espaciado del diseño y el enrutamiento**. (En la ficha **Diseño**, haga clic en la flecha de **Configurar página**, haga clic en **Diseño y enrutamiento** y, a continuación, en **Espaciado**).</span><span class="sxs-lookup"><span data-stu-id="a35c8-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="a35c8-108">Para obtener una referencia a la celda LineToLineY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="a35c8-108">To get a reference to the LineToLineY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a35c8-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="a35c8-109">Cell name:</span></span>  <br/> |<span data-ttu-id="a35c8-110">LineToLineY</span><span class="sxs-lookup"><span data-stu-id="a35c8-110">LineToLineY</span></span>  <br/> |
   
<span data-ttu-id="a35c8-111">Para obtener una referencia desde un programa a la celda LineToLineY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a35c8-111">To get a reference to the LineToLineY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a35c8-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="a35c8-112">Section index:</span></span>  <br/> |<span data-ttu-id="a35c8-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a35c8-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a35c8-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="a35c8-114">Row index:</span></span>  <br/> |<span data-ttu-id="a35c8-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="a35c8-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="a35c8-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="a35c8-116">Cell index:</span></span>  <br/> |<span data-ttu-id="a35c8-117">**visPLOLineToLineY**</span><span class="sxs-lookup"><span data-stu-id="a35c8-117">**visPLOLineToLineY**</span></span> <br/> |
   

