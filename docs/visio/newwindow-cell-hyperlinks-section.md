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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396340"
---
# <a name="newwindow-cell-hyperlinks-section"></a><span data-ttu-id="0443f-103">Celda NewWindow (sección Hipervínculos)</span><span class="sxs-lookup"><span data-stu-id="0443f-103">NewWindow Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="0443f-104">Especifica si el hipervínculo se abre en una ventana nueva.</span><span class="sxs-lookup"><span data-stu-id="0443f-104">Specifies whether to open the hyperlink in a new window.</span></span>
  
|<span data-ttu-id="0443f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0443f-105">**Value**</span></span>|<span data-ttu-id="0443f-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0443f-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="0443f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="0443f-107">TRUE</span></span>  <br/> | <span data-ttu-id="0443f-108">Abra la página vinculada, documento o sitio Web en una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="0443f-108">Open the linked page, document, or website in a new window.</span></span>  <br/> |
| <span data-ttu-id="0443f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="0443f-109">FALSE</span></span>  <br/> | <span data-ttu-id="0443f-p101">Valor predeterminado. No abrir una ventana nueva para el hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="0443f-p101">Default. Do not open a new window for the hyperlink.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0443f-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0443f-112">Remarks</span></span>

<span data-ttu-id="0443f-113">Para obtener una referencia a la celda NewWindow por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="0443f-113">To get a reference to the NewWindow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0443f-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="0443f-114">Cell name:</span></span>  <br/> | <span data-ttu-id="0443f-115">Hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="0443f-115">Hyperlink.</span></span>  <span data-ttu-id="0443f-116">*Nombre* . NewWindow donde hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="0443f-116">*Name*  .NewWindow            where Hyperlink.</span></span>  <span data-ttu-id="0443f-117">*Nombre* es el nombre de fila</span><span class="sxs-lookup"><span data-stu-id="0443f-117">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="0443f-118">Para obtener una referencia desde un programa a la celda NewWindow por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="0443f-118">To get a reference to the NewWindow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0443f-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="0443f-119">Section index:</span></span>  <br/> |<span data-ttu-id="0443f-120">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="0443f-120">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="0443f-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="0443f-121">Row index:</span></span>  <br/> |<span data-ttu-id="0443f-122">**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="0443f-122">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="0443f-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="0443f-123">Cell index:</span></span>  <br/> |<span data-ttu-id="0443f-124">**visHLinkNewWin**</span><span class="sxs-lookup"><span data-stu-id="0443f-124">**visHLinkNewWin**</span></span> <br/> |
   

