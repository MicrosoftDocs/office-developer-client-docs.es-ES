---
title: Celda PrintPageOrientation (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033795
localization_priority: Normal
ms.assetid: f8354d0d-0ce2-fb33-ddf7-611a2c24a8be
description: Determina si la página se imprime con orientación vertical u horizontal.
ms.openlocfilehash: f7e73bea5120d878a1b2dbf553a66b349d247fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434868"
---
# <a name="printpageorientation-cell-print-properties-section"></a><span data-ttu-id="0cdea-103">Celda PrintPageOrientation (Sección de propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="0cdea-103">PrintPageOrientation Cell (Print Properties Section)</span></span>

<span data-ttu-id="0cdea-104">Determina si la página se imprime con orientación vertical u horizontal.</span><span class="sxs-lookup"><span data-stu-id="0cdea-104">Determines whether the page prints using portrait or landscape orientation.</span></span>
  
|<span data-ttu-id="0cdea-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0cdea-105">**Value**</span></span>|<span data-ttu-id="0cdea-106">**Orientación**</span><span class="sxs-lookup"><span data-stu-id="0cdea-106">**Orientation**</span></span>|<span data-ttu-id="0cdea-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="0cdea-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="0cdea-108">0</span><span class="sxs-lookup"><span data-stu-id="0cdea-108">0</span></span>  <br/> | <span data-ttu-id="0cdea-109">Igual que la impresora</span><span class="sxs-lookup"><span data-stu-id="0cdea-109">Same as printer</span></span>  <br/> |<span data-ttu-id="0cdea-110">**visPOSSameAsPrinter**</span><span class="sxs-lookup"><span data-stu-id="0cdea-110">**visPPOSameAsPrinter**</span></span> <br/> |
| <span data-ttu-id="0cdea-111">1 </span><span class="sxs-lookup"><span data-stu-id="0cdea-111">1</span></span>  <br/> | <span data-ttu-id="0cdea-112">Portrait</span><span class="sxs-lookup"><span data-stu-id="0cdea-112">Portrait</span></span>  <br/> |<span data-ttu-id="0cdea-113">**visAGIPortrait**</span><span class="sxs-lookup"><span data-stu-id="0cdea-113">**visPPOPortrait**</span></span> <br/> |
|<span data-ttu-id="0cdea-114">2 </span><span class="sxs-lookup"><span data-stu-id="0cdea-114">2</span></span>  <br/> |<span data-ttu-id="0cdea-115">Horizontal</span><span class="sxs-lookup"><span data-stu-id="0cdea-115">Landscape</span></span>  <br/> |<span data-ttu-id="0cdea-116">**visSCAPELandscape**</span><span class="sxs-lookup"><span data-stu-id="0cdea-116">**visPPOLandscape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0cdea-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0cdea-117">Remarks</span></span>

<span data-ttu-id="0cdea-118">Al insertar nuevas páginas en un documento, esta configuración se establece de forma predeterminada en la configuración de la página activa.</span><span class="sxs-lookup"><span data-stu-id="0cdea-118">When you insert new pages in a document, this setting defaults to the setting in the active page.</span></span>
  
<span data-ttu-id="0cdea-119">Para obtener una referencia a la celda PrintPageOrientation por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="0cdea-119">To get a reference to the PrintPageOrientation cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0cdea-120">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="0cdea-120">Cell name:</span></span>  <br/> | <span data-ttu-id="0cdea-121">PrintPageOrientation</span><span class="sxs-lookup"><span data-stu-id="0cdea-121">PrintPageOrientation</span></span>  <br/> |
   
<span data-ttu-id="0cdea-122">Para obtener una referencia desde un programa a la celda PrintPageOrientation por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="0cdea-122">To get a reference to the PrintPageOrientation cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0cdea-123">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="0cdea-123">Section index:</span></span>  <br/> |<span data-ttu-id="0cdea-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0cdea-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0cdea-125">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="0cdea-125">Row index:</span></span>  <br/> |<span data-ttu-id="0cdea-126">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="0cdea-126">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="0cdea-127">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="0cdea-127">Cell index:</span></span>  <br/> |<span data-ttu-id="0cdea-128">**visPrintPropertiesPageOrientation**</span><span class="sxs-lookup"><span data-stu-id="0cdea-128">**visPrintPropertiesPageOrientation**</span></span> <br/> |
   

