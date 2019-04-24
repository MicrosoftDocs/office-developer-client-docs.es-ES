---
title: Celda NewWindow (Sección de hipervínculos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm695
localization_priority: Normal
ms.assetid: 44995137-d241-937a-c097-0f9d79203cdf
description: Especifica si el hipervínculo se abre en una ventana nueva.
ms.openlocfilehash: 0f9d1e4b1294dea3f211c8d0d69ffc49b6180066
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342234"
---
# <a name="newwindow-cell-hyperlinks-section"></a><span data-ttu-id="31a3d-103">Celda NewWindow (Sección de hipervínculos)</span><span class="sxs-lookup"><span data-stu-id="31a3d-103">NewWindow Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="31a3d-104">Especifica si el hipervínculo se abre en una ventana nueva.</span><span class="sxs-lookup"><span data-stu-id="31a3d-104">Specifies whether to open the hyperlink in a new window.</span></span>
  
|<span data-ttu-id="31a3d-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="31a3d-105">**Value**</span></span>|<span data-ttu-id="31a3d-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="31a3d-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="31a3d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="31a3d-107">TRUE</span></span>  <br/> | <span data-ttu-id="31a3d-108">Abra la página vinculada, el documento o el sitio web en una ventana nueva.</span><span class="sxs-lookup"><span data-stu-id="31a3d-108">Open the linked page, document, or website in a new window.</span></span>  <br/> |
| <span data-ttu-id="31a3d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="31a3d-109">FALSE</span></span>  <br/> | <span data-ttu-id="31a3d-p101">Valor predeterminado. No abrir una ventana nueva para el hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="31a3d-p101">Default. Do not open a new window for the hyperlink.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31a3d-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="31a3d-112">Remarks</span></span>

<span data-ttu-id="31a3d-113">Para obtener una referencia a la celda NewWindow por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="31a3d-113">To get a reference to the NewWindow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="31a3d-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="31a3d-114">Cell name:</span></span>  <br/> | <span data-ttu-id="31a3d-115">Hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="31a3d-115">Hyperlink.</span></span>  <span data-ttu-id="31a3d-116">*Nombre* . NewWindow donde HYPERLINK.</span><span class="sxs-lookup"><span data-stu-id="31a3d-116">*Name*  .NewWindow            where Hyperlink.</span></span>  <span data-ttu-id="31a3d-117">*Name* es el nombre de la fila</span><span class="sxs-lookup"><span data-stu-id="31a3d-117">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="31a3d-118">Para obtener una referencia desde un programa a la celda NewWindow por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="31a3d-118">To get a reference to the NewWindow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="31a3d-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="31a3d-119">Section index:</span></span>  <br/> |<span data-ttu-id="31a3d-120">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="31a3d-120">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="31a3d-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="31a3d-121">Row index:</span></span>  <br/> |<span data-ttu-id="31a3d-122">**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="31a3d-122">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="31a3d-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="31a3d-123">Cell index:</span></span>  <br/> |<span data-ttu-id="31a3d-124">**visHLinkNewWin**</span><span class="sxs-lookup"><span data-stu-id="31a3d-124">**visHLinkNewWin**</span></span> <br/> |
   

