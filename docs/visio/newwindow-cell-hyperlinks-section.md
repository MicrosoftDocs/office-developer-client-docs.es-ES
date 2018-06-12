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
ms.openlocfilehash: b4d927e1970e994047df3cb89afa7799a825511d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822673"
---
# <a name="newwindow-cell-hyperlinks-section"></a><span data-ttu-id="a5143-103">Celda NewWindow (Sección de hipervínculos)</span><span class="sxs-lookup"><span data-stu-id="a5143-103">NewWindow Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="a5143-104">Especifica si el hipervínculo se abre en una ventana nueva.</span><span class="sxs-lookup"><span data-stu-id="a5143-104">Specifies whether to open the hyperlink in a new window.</span></span>
  
|<span data-ttu-id="a5143-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a5143-105">**Value**</span></span>|<span data-ttu-id="a5143-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a5143-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a5143-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a5143-107">TRUE</span></span>  <br/> | <span data-ttu-id="a5143-108">Abre la página, el documento o el sitio Web vinculado en una ventana nueva.</span><span class="sxs-lookup"><span data-stu-id="a5143-108">Open the linked page, document, or Web site in a new window.</span></span>  <br/> |
| <span data-ttu-id="a5143-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a5143-109">FALSE</span></span>  <br/> | <span data-ttu-id="a5143-p101">Valor predeterminado. No abrir una ventana nueva para el hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="a5143-p101">Default. Do not open a new window for the hyperlink.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5143-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a5143-112">Remarks</span></span>

<span data-ttu-id="a5143-113">Para obtener una referencia a la celda NewWindow por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="a5143-113">To get a reference to the NewWindow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a5143-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="a5143-114">Cell name:</span></span>  <br/> | <span data-ttu-id="a5143-115">Hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="a5143-115">Hyperlink.</span></span>  <span data-ttu-id="a5143-116">*Nombre* . NewWindow donde hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="a5143-116">*Name*  .NewWindow            where Hyperlink.</span></span>  <span data-ttu-id="a5143-117">*Nombre* es el nombre de fila</span><span class="sxs-lookup"><span data-stu-id="a5143-117">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="a5143-118">Para obtener una referencia a la celda NewWindow por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a5143-118">To get a reference to the NewWindow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a5143-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="a5143-119">Section index:</span></span>  <br/> |<span data-ttu-id="a5143-120">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="a5143-120">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="a5143-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="a5143-121">Row index:</span></span>  <br/> |<span data-ttu-id="a5143-122">**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="a5143-122">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="a5143-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="a5143-123">Cell index:</span></span>  <br/> |<span data-ttu-id="a5143-124">**visHLinkNewWin**</span><span class="sxs-lookup"><span data-stu-id="a5143-124">**visHLinkNewWin**</span></span> <br/> |
   

