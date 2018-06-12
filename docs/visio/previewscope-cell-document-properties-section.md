---
title: Celda PreviewScope (Sección de propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm820
localization_priority: Normal
ms.assetid: d03ae1b3-da6c-56d3-4f96-6e131c04e93e
description: Determina si el dibujo incluye una vista previa. Si la incluye, determina si la vista previa muestra la primera página únicamente o todas las páginas del dibujo.
ms.openlocfilehash: 865da052f710481c146d3c2692ddf506018be789
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822852"
---
# <a name="previewscope-cell-document-properties-section"></a><span data-ttu-id="bd09c-104">Celda PreviewScope (Sección de propiedades del documento)</span><span class="sxs-lookup"><span data-stu-id="bd09c-104">PreviewScope Cell (Document Properties Section)</span></span>

<span data-ttu-id="bd09c-p102">Determina si el dibujo incluye una vista previa. Si la incluye, determina si la vista previa muestra la primera página únicamente o todas las páginas del dibujo.</span><span class="sxs-lookup"><span data-stu-id="bd09c-p102">Determines whether your drawing includes a preview. If your drawing does include a preview, it determines whether the preview shows the first page only or all of the pages in the drawing.</span></span>
  
|<span data-ttu-id="bd09c-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="bd09c-107">**Value**</span></span>|<span data-ttu-id="bd09c-108">**Ámbito de vista previa**</span><span class="sxs-lookup"><span data-stu-id="bd09c-108">**Preview scope**</span></span>|<span data-ttu-id="bd09c-109">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="bd09c-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="bd09c-110">0</span><span class="sxs-lookup"><span data-stu-id="bd09c-110">0</span></span>  <br/> | <span data-ttu-id="bd09c-111">Primera página</span><span class="sxs-lookup"><span data-stu-id="bd09c-111">First page</span></span>  <br/> |<span data-ttu-id="bd09c-112">**visDocPreviewScope1stPage**</span><span class="sxs-lookup"><span data-stu-id="bd09c-112">**visDocPreviewScope1stPage**</span></span> <br/> |
| <span data-ttu-id="bd09c-113">1</span><span class="sxs-lookup"><span data-stu-id="bd09c-113">1</span></span>  <br/> | <span data-ttu-id="bd09c-114">Ninguna</span><span class="sxs-lookup"><span data-stu-id="bd09c-114">None</span></span>  <br/> |<span data-ttu-id="bd09c-115">**visDocPreviewScopeNone**</span><span class="sxs-lookup"><span data-stu-id="bd09c-115">**visDocPreviewScopeNone**</span></span> <br/> |
| <span data-ttu-id="bd09c-116">2</span><span class="sxs-lookup"><span data-stu-id="bd09c-116">2</span></span>  <br/> | <span data-ttu-id="bd09c-117">Todas las páginas</span><span class="sxs-lookup"><span data-stu-id="bd09c-117">All pages</span></span>  <br/> |<span data-ttu-id="bd09c-118">**visDocPreviewScopeAllPages**</span><span class="sxs-lookup"><span data-stu-id="bd09c-118">**visDocPreviewScopeAllPages**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd09c-119">Notas</span><span class="sxs-lookup"><span data-stu-id="bd09c-119">Remarks</span></span>

<span data-ttu-id="bd09c-120">También puede establecer este valor en la ficha **Resumen** en el cuadro de diálogo **Propiedades** (haga clic en el botón de **Office** , haga clic en la ficha **información** , haga clic en **Propiedades del documento**y, a continuación, haga clic en **Propiedades avanzadas**).</span><span class="sxs-lookup"><span data-stu-id="bd09c-120">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="bd09c-121">Para obtener una referencia a la celda PreviewScope por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="bd09c-121">To get a reference to the PreviewScope cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd09c-122">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="bd09c-122">Cell name:</span></span>  <br/> | <span data-ttu-id="bd09c-123">PreviewScope</span><span class="sxs-lookup"><span data-stu-id="bd09c-123">PreviewScope</span></span>  <br/> |
   
<span data-ttu-id="bd09c-124">Para obtener una referencia a la celda PreviewScope por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="bd09c-124">To get a reference to the PreviewScope cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd09c-125">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="bd09c-125">Section index:</span></span>  <br/> |<span data-ttu-id="bd09c-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bd09c-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bd09c-127">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="bd09c-127">Row index:</span></span>  <br/> |<span data-ttu-id="bd09c-128">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="bd09c-128">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="bd09c-129">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="bd09c-129">Cell index:</span></span>  <br/> |<span data-ttu-id="bd09c-130">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="bd09c-130">**visDocPreviewScope**</span></span> <br/> |
   

