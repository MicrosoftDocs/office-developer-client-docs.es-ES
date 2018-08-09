---
title: Celda CenterX (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60030
localization_priority: Normal
ms.assetid: 890e2537-66a5-2863-c78d-320b42565ea7
description: Determina si la página de dibujo está centrada horizontalmente en la página de la impresora.
ms.openlocfilehash: a12b60f7d183a27d938bd18a1f571ef01af455d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821755"
---
# <a name="centerx-cell-print-properties-section"></a><span data-ttu-id="59f31-103">Celda CenterX (sección Propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="59f31-103">CenterX Cell (Print Properties Section)</span></span>

<span data-ttu-id="59f31-104">Determina si la página de dibujo está centrada horizontalmente en la página de la impresora.</span><span class="sxs-lookup"><span data-stu-id="59f31-104">Determines whether the drawing page is centered horizontally on the printer page.</span></span> 
  
|<span data-ttu-id="59f31-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="59f31-105">**Value**</span></span>|<span data-ttu-id="59f31-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="59f31-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="59f31-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="59f31-107">TRUE</span></span>  <br/> | <span data-ttu-id="59f31-108">La página de dibujo se centra horizontalmente en la página de la impresora.</span><span class="sxs-lookup"><span data-stu-id="59f31-108">Center the drawing page horizontally on the printer page.</span></span>  <br/> |
| <span data-ttu-id="59f31-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="59f31-109">FALSE</span></span>  <br/> | <span data-ttu-id="59f31-110">La página de dibujo no se centra horizontalmente en la página de la impresora (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="59f31-110">Do not center the drawing page horizontally on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59f31-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="59f31-111">Remarks</span></span>

<span data-ttu-id="59f31-p101">De forma predeterminada, las páginas de dibujo están alineadas a la parte superior y a la izquierda de la página de la impresora. Si se establece el valor de las celdas CenterX y CenterY en TRUE, la página de dibujo se colocará en el centro de la página de la impresora (o páginas cuando sea necesario aplicar mosaico).</span><span class="sxs-lookup"><span data-stu-id="59f31-p101">By default, drawing pages are justified to the top and left of the printer page. Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="59f31-114">Para obtener una referencia a la celda CenterX por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="59f31-114">To get a reference to the CenterX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="59f31-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="59f31-115">Cell name:</span></span>  <br/> | <span data-ttu-id="59f31-116">CenterX</span><span class="sxs-lookup"><span data-stu-id="59f31-116">CenterX</span></span>  <br/> |
   
<span data-ttu-id="59f31-117">Para obtener una referencia desde un programa a la celda CenterX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="59f31-117">To get a reference to the CenterX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="59f31-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="59f31-118">Section index:</span></span>  <br/> |<span data-ttu-id="59f31-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="59f31-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="59f31-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="59f31-120">Row index:</span></span>  <br/> |<span data-ttu-id="59f31-121">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="59f31-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="59f31-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="59f31-122">Cell index:</span></span>  <br/> |<span data-ttu-id="59f31-123">**visPrintPropertiesCenterX**</span><span class="sxs-lookup"><span data-stu-id="59f31-123">**visPrintPropertiesCenterX**</span></span> <br/> |
   

