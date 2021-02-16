---
title: Celda PrintGrid (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033794
localization_priority: Normal
ms.assetid: 0504ff7f-2274-7ae3-1f4b-a3d890dbd79a
description: Especifica si se imprime la cuadrícula al imprimir una página de documento.
ms.openlocfilehash: 9b98999cd02fa6a47ec8564bbd7337ecf8637306
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433209"
---
# <a name="printgrid-cell-print-properties-section"></a><span data-ttu-id="7888e-103">Celda PrintGrid (sección de propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="7888e-103">PrintGrid Cell (Print Properties Section)</span></span>

<span data-ttu-id="7888e-104">Especifica si se imprime la cuadrícula al imprimir una página de documento.</span><span class="sxs-lookup"><span data-stu-id="7888e-104">Specifies whether to print the grid when printing a document page.</span></span>
  
|<span data-ttu-id="7888e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7888e-105">**Value**</span></span>|<span data-ttu-id="7888e-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7888e-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7888e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="7888e-107">TRUE</span></span>  <br/> |<span data-ttu-id="7888e-108">Muestra la cuadrícula al imprimir esta página.</span><span class="sxs-lookup"><span data-stu-id="7888e-108">Show the grid when printing this page.</span></span>  <br/> |
|<span data-ttu-id="7888e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="7888e-109">FALSE</span></span>  <br/> |<span data-ttu-id="7888e-110">No muestra la cuadrícula al imprimir esta página (predeterminado).</span><span class="sxs-lookup"><span data-stu-id="7888e-110">Do not show the grid when printing this page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7888e-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7888e-111">Remarks</span></span>

<span data-ttu-id="7888e-p101">Este valor corresponde a la casilla **Cuadrícula** de la ficha **Configurar impresión** del cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página**). A excepción del color (se imprime en gris), la cuadrícula impresa coincide por completo con la que se ve en la ventana del dibujo de Microsoft Office Visio.</span><span class="sxs-lookup"><span data-stu-id="7888e-p101">This value corresponds to the **Gridlines** check box on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). Other than color (the printed version is gray), the printed grid is identical to the grid you see in the Microsoft Visio drawing window.</span></span> 
  
<span data-ttu-id="7888e-114">Puede elegir si desea imprimir la cuadrícula página por página.</span><span class="sxs-lookup"><span data-stu-id="7888e-114">You can choose whether to print the grid on a page-by-page basis.</span></span> <span data-ttu-id="7888e-115">El estilo de la cuadrícula también se puede definir página por página en  el cuadro de  diálogo Cuadrícula de regla (en la ficha Ver, haga clic en la flecha Mostrar) cuando esté activa una página. **&amp;**</span><span class="sxs-lookup"><span data-stu-id="7888e-115">The style of grid can also be defined on a page-by-page basis in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow) when a page is active.</span></span> 
  
<span data-ttu-id="7888e-116">Para obtener una referencia a la celda PrintGrid por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="7888e-116">To get a reference to the PrintGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7888e-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="7888e-117">Cell name:</span></span>  <br/> |<span data-ttu-id="7888e-118">PrintGrid</span><span class="sxs-lookup"><span data-stu-id="7888e-118">PrintGrid</span></span>  <br/> |
   
<span data-ttu-id="7888e-119">Para obtener una referencia desde un programa a la celda PrintGrid por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7888e-119">To get a reference to the PrintGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7888e-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="7888e-120">Section index:</span></span>  <br/> |<span data-ttu-id="7888e-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7888e-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="7888e-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="7888e-122">Row index:</span></span>  <br/> |<span data-ttu-id="7888e-123">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="7888e-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="7888e-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="7888e-124">Cell index:</span></span>  <br/> |<span data-ttu-id="7888e-125">**visPrintPropertiesPrintGrid**</span><span class="sxs-lookup"><span data-stu-id="7888e-125">**visPrintPropertiesPrintGrid**</span></span> <br/> |
   

