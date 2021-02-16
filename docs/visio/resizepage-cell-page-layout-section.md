---
title: Celda ResizePage (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm850
localization_priority: Normal
ms.assetid: d63fe874-1027-3436-dbc1-73e722bce22e
description: Determina si se debe agrandar la página para acomodar el dibujo después de diseñar las formas mediante el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en Redistribuir página y, a continuación, en Más opciones de diseño).
ms.openlocfilehash: 8d0001ce35808f8c5f11068ed78865ce992af5cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438095"
---
# <a name="resizepage-cell-page-layout-section"></a><span data-ttu-id="ea0ca-103">Celda ResizePage (Sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="ea0ca-103">ResizePage Cell (Page Layout Section)</span></span>

<span data-ttu-id="ea0ca-104">Determina si se va a ampliar la página para incluir  el dibujo después de  diseñar las formas mediante  el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en Volver a diseñar página y, a continuación, haga clic en Más opciones de diseño **).** </span><span class="sxs-lookup"><span data-stu-id="ea0ca-104">Determines whether to enlarge the page to enclose the drawing after laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="ea0ca-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ea0ca-105">**Value**</span></span>|<span data-ttu-id="ea0ca-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ea0ca-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ea0ca-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ea0ca-107">TRUE</span></span>  <br/> | <span data-ttu-id="ea0ca-108">Se agranda la página.</span><span class="sxs-lookup"><span data-stu-id="ea0ca-108">Enlarge the page.</span></span>  <br/> |
| <span data-ttu-id="ea0ca-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ea0ca-109">FALSE</span></span>  <br/> | <span data-ttu-id="ea0ca-110">No se agranda la página.</span><span class="sxs-lookup"><span data-stu-id="ea0ca-110">Do not enlarge the page.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea0ca-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ea0ca-111">Remarks</span></span>

<span data-ttu-id="ea0ca-112">Para obtener una referencia a la celda ResizePage por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="ea0ca-112">To get a reference to the ResizePage cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ea0ca-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="ea0ca-113">Cell name:</span></span>  <br/> | <span data-ttu-id="ea0ca-114">ResizePage</span><span class="sxs-lookup"><span data-stu-id="ea0ca-114">ResizePage</span></span>  <br/> |
   
<span data-ttu-id="ea0ca-115">Para obtener una referencia desde un programa a la celda ResizePage por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ea0ca-115">To get a reference to the ResizePage cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ea0ca-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="ea0ca-116">Section index:</span></span>  <br/> |<span data-ttu-id="ea0ca-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ea0ca-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ea0ca-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="ea0ca-118">Row index:</span></span>  <br/> |<span data-ttu-id="ea0ca-119">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="ea0ca-119">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="ea0ca-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="ea0ca-120">Cell index:</span></span>  <br/> |<span data-ttu-id="ea0ca-121">**visPLOResizePage**</span><span class="sxs-lookup"><span data-stu-id="ea0ca-121">**visPLOResizePage**</span></span> <br/> |
   

