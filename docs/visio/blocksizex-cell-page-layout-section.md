---
title: Celda BlockSizeX (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm105
localization_priority: Normal
ms.assetid: 253aac17-077e-48e0-39a8-a3abd5d4a257
description: Determina el tamaño del bloque horizontal, el área en la que cada una de las formas debe caber en la página de dibujo al diseñar formas mediante el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en Re-Layout Página y, a continuación, haga clic en Más opciones de diseño).
ms.openlocfilehash: 8e4cee4b2059d9b8f2fe77c2d4902e67246eac2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424192"
---
# <a name="blocksizex-cell-page-layout-section"></a><span data-ttu-id="0f1e0-103">Celda BlockSizeX (Sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="0f1e0-103">BlockSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="0f1e0-104">Determina el tamaño del bloque horizontal, el área en la que cada una de las formas debe caber  en la  página de dibujo al diseñar formas mediante el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en Volver a diseñar página **y,** a continuación, haga clic en Más opciones de diseño **).** </span><span class="sxs-lookup"><span data-stu-id="0f1e0-104">Determines the horizontal block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0f1e0-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0f1e0-105">Remarks</span></span>

<span data-ttu-id="0f1e0-106">También puede establecer este valor en el cuadro de diálogo **Espaciado del diseño y el enrutamiento** (en la ficha **Diseño**, haga clic en la flecha del grupo **Configurar página**, haga clic en la pestaña **Diseño y enrutamiento** y, a continuación, en **Espaciado**).</span><span class="sxs-lookup"><span data-stu-id="0f1e0-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="0f1e0-107">Para obtener una referencia a la celda BlockSizeX por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="0f1e0-107">To get a reference to the BlockSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0f1e0-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="0f1e0-108">Cell name:</span></span>  <br/> |<span data-ttu-id="0f1e0-109">BlockSizeX</span><span class="sxs-lookup"><span data-stu-id="0f1e0-109">BlockSizeX</span></span>  <br/> |
   
<span data-ttu-id="0f1e0-110">Para obtener una referencia desde un programa a la celda BlockSizeX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="0f1e0-110">To get a reference to the BlockSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0f1e0-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="0f1e0-111">Section index:</span></span>  <br/> |<span data-ttu-id="0f1e0-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0f1e0-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0f1e0-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="0f1e0-113">Row index:</span></span>  <br/> |<span data-ttu-id="0f1e0-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="0f1e0-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="0f1e0-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="0f1e0-115">Cell index:</span></span>  <br/> |<span data-ttu-id="0f1e0-116">**visPLOBlockSizeX**</span><span class="sxs-lookup"><span data-stu-id="0f1e0-116">**visPLOBlockSizeX**</span></span> <br/> |
   

