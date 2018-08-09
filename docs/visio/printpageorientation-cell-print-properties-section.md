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
ms.openlocfilehash: 2adc7dadcb3702e6c5307bb569b2ae1df7aee54e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822869"
---
# <a name="printpageorientation-cell-print-properties-section"></a><span data-ttu-id="6f11f-103">Celda PrintPageOrientation (sección Propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="6f11f-103">PrintPageOrientation Cell (Print Properties Section)</span></span>

<span data-ttu-id="6f11f-104">Determina si la página se imprime con orientación vertical u horizontal.</span><span class="sxs-lookup"><span data-stu-id="6f11f-104">Determines whether the page prints using portrait or landscape orientation.</span></span>
  
|<span data-ttu-id="6f11f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6f11f-105">**Value**</span></span>|<span data-ttu-id="6f11f-106">**Orientation**</span><span class="sxs-lookup"><span data-stu-id="6f11f-106">**Orientation**</span></span>|<span data-ttu-id="6f11f-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="6f11f-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="6f11f-108">0</span><span class="sxs-lookup"><span data-stu-id="6f11f-108">0</span></span>  <br/> | <span data-ttu-id="6f11f-109">Igual que la impresora</span><span class="sxs-lookup"><span data-stu-id="6f11f-109">Same as printer</span></span>  <br/> |<span data-ttu-id="6f11f-110">**visPPOSameAsPrinter**</span><span class="sxs-lookup"><span data-stu-id="6f11f-110">**visPPOSameAsPrinter**</span></span> <br/> |
| <span data-ttu-id="6f11f-111">1</span><span class="sxs-lookup"><span data-stu-id="6f11f-111">1</span></span>  <br/> | <span data-ttu-id="6f11f-112">Vertical</span><span class="sxs-lookup"><span data-stu-id="6f11f-112">Portrait</span></span>  <br/> |<span data-ttu-id="6f11f-113">**visPPOPortrait**</span><span class="sxs-lookup"><span data-stu-id="6f11f-113">**visPPOPortrait**</span></span> <br/> |
|<span data-ttu-id="6f11f-114">2</span><span class="sxs-lookup"><span data-stu-id="6f11f-114">2</span></span>  <br/> |<span data-ttu-id="6f11f-115">Horizontal</span><span class="sxs-lookup"><span data-stu-id="6f11f-115">Landscape</span></span>  <br/> |<span data-ttu-id="6f11f-116">**visPPOLandscape**</span><span class="sxs-lookup"><span data-stu-id="6f11f-116">**visPPOLandscape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f11f-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6f11f-117">Remarks</span></span>

<span data-ttu-id="6f11f-118">Cuando se insertan nuevas páginas en un documento, el valor predeterminado es la configuración en la página activa.</span><span class="sxs-lookup"><span data-stu-id="6f11f-118">When you insert new pages in a document, this setting defaults to the setting in the active page.</span></span>
  
<span data-ttu-id="6f11f-119">Para obtener una referencia a la celda PrintPageOrientation por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="6f11f-119">To get a reference to the PrintPageOrientation cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6f11f-120">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="6f11f-120">Cell name:</span></span>  <br/> | <span data-ttu-id="6f11f-121">PrintPageOrientation</span><span class="sxs-lookup"><span data-stu-id="6f11f-121">PrintPageOrientation</span></span>  <br/> |
   
<span data-ttu-id="6f11f-122">Para obtener una referencia desde un programa a la celda PrintPageOrientation por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6f11f-122">To get a reference to the PrintPageOrientation cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6f11f-123">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="6f11f-123">Section index:</span></span>  <br/> |<span data-ttu-id="6f11f-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6f11f-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6f11f-125">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="6f11f-125">Row index:</span></span>  <br/> |<span data-ttu-id="6f11f-126">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="6f11f-126">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="6f11f-127">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="6f11f-127">Cell index:</span></span>  <br/> |<span data-ttu-id="6f11f-128">**visPrintPropertiesPageOrientation**</span><span class="sxs-lookup"><span data-stu-id="6f11f-128">**visPrintPropertiesPageOrientation**</span></span> <br/> |
   

