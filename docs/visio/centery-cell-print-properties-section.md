---
title: Celda CenterY (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033792
localization_priority: Normal
ms.assetid: 7ce0bf66-dc8b-9646-7b04-50c969ecd67a
description: Determina si la página de dibujo está centrada verticalmente en la página de la impresora.
ms.openlocfilehash: 2fde1d6301d7b9de4540cd12f21e5af01d7a6239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821774"
---
# <a name="centery-cell-print-properties-section"></a><span data-ttu-id="1ed5f-103">Celda CenterY (Sección de propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="1ed5f-103">CenterY Cell (Print Properties Section)</span></span>

<span data-ttu-id="1ed5f-104">Determina si la página de dibujo está centrada verticalmente en la página de la impresora.</span><span class="sxs-lookup"><span data-stu-id="1ed5f-104">Determines whether the drawing page is centered vertically on the printer page.</span></span> 
  
|<span data-ttu-id="1ed5f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1ed5f-105">**Value**</span></span>|<span data-ttu-id="1ed5f-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ed5f-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="1ed5f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="1ed5f-107">TRUE</span></span>  <br/> | <span data-ttu-id="1ed5f-108">La página de dibujo se centra verticalmente en la página de la impresora.</span><span class="sxs-lookup"><span data-stu-id="1ed5f-108">Center the drawing page vertically on the printer page.</span></span>  <br/> |
| <span data-ttu-id="1ed5f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="1ed5f-109">FALSE</span></span>  <br/> | <span data-ttu-id="1ed5f-110">La página de dibujo no se centra verticalmente en la página de la impresora (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="1ed5f-110">Do not center the drawing page vertically on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ed5f-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1ed5f-111">Remarks</span></span>

<span data-ttu-id="1ed5f-p101">De forma predeterminada, las páginas de dibujo están alineadas a la parte superior y a la izquierda de la página de la impresora. Si se establece el valor de las celdas CenterX y CenterY en TRUE, la página de dibujo se colocará en el centro de la página de la impresora (o páginas cuando sea necesario aplicar mosaico).</span><span class="sxs-lookup"><span data-stu-id="1ed5f-p101">By default, drawing pages are justified to the top and left of the printer page. Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="1ed5f-114">Para obtener una referencia a la celda CenterY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="1ed5f-114">To get a reference to the CenterY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1ed5f-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="1ed5f-115">Cell name:</span></span>  <br/> | <span data-ttu-id="1ed5f-116">CenterY</span><span class="sxs-lookup"><span data-stu-id="1ed5f-116">CenterY</span></span>  <br/> |
   
<span data-ttu-id="1ed5f-117">Para obtener una referencia a la celda CenterY por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1ed5f-117">To get a reference to the CenterY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1ed5f-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="1ed5f-118">Section index:</span></span>  <br/> |<span data-ttu-id="1ed5f-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1ed5f-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1ed5f-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="1ed5f-120">Row index:</span></span>  <br/> |<span data-ttu-id="1ed5f-121">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="1ed5f-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="1ed5f-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="1ed5f-122">Cell index:</span></span>  <br/> |<span data-ttu-id="1ed5f-123">**visPrintPropertiesCenterY**</span><span class="sxs-lookup"><span data-stu-id="1ed5f-123">**visPrintPropertiesCenterY**</span></span> <br/> |
   

