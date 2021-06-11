---
title: Celda CtrlAsInput (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1225
localization_priority: Normal
ms.assetid: c6fd0aba-7c33-b77f-207b-ba704b3e0756
description: Determina qué forma es la principal cuando se emplean formas con controladores. Esta celda establece el comportamiento de todas las formas en la página de dibujo.
ms.openlocfilehash: a530c48156043bec0cd58d79aead1a403c17ddce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422624"
---
# <a name="ctrlasinput-cell-page-layout-section"></a><span data-ttu-id="9b57f-104">Celda CtrlAsInput (Sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="9b57f-104">CtrlAsInput Cell (Page Layout Section)</span></span>

<span data-ttu-id="9b57f-p102">Determina qué forma es la principal cuando se emplean formas con controladores. Esta celda establece el comportamiento de todas las formas en la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="9b57f-p102">Determines which shape is the parent when using shapes with control handles. This cell sets the behavior for all the shapes on the drawing page.</span></span>
  
|<span data-ttu-id="9b57f-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9b57f-107">**Value**</span></span>|<span data-ttu-id="9b57f-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9b57f-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9b57f-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="9b57f-109">TRUE</span></span>  <br/> | <span data-ttu-id="9b57f-110">Se establece como forma principal la forma a la que está conectado el controlador.</span><span class="sxs-lookup"><span data-stu-id="9b57f-110">Set the shape that the control handle is connected to as the parent.</span></span>  <br/> |
| <span data-ttu-id="9b57f-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="9b57f-111">FALSE</span></span>  <br/> | <span data-ttu-id="9b57f-p103">Valor predeterminado. Se establece como forma principal la forma que contiene el controlador.</span><span class="sxs-lookup"><span data-stu-id="9b57f-p103">The default. Set shape that contains the control handle as the parent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b57f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9b57f-114">Remarks</span></span>

<span data-ttu-id="9b57f-115">Para obtener una referencia a la celda CtrlAsInput por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="9b57f-115">To get a reference to the CtrlAsInput cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9b57f-116">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="9b57f-116">Cell name:</span></span>  <br/> | <span data-ttu-id="9b57f-117">CtrlAsInput</span><span class="sxs-lookup"><span data-stu-id="9b57f-117">CtrlAsInput</span></span>  <br/> |
   
<span data-ttu-id="9b57f-118">Para obtener una referencia desde un programa a la celda CtrlAsInput por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9b57f-118">To get a reference to the CtrlAsInput cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9b57f-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="9b57f-119">Section index:</span></span>  <br/> |<span data-ttu-id="9b57f-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9b57f-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9b57f-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="9b57f-121">Row index:</span></span>  <br/> |<span data-ttu-id="9b57f-122">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="9b57f-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="9b57f-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="9b57f-123">Cell index:</span></span>  <br/> |<span data-ttu-id="9b57f-124">**visPLOCtrlAsInput**</span><span class="sxs-lookup"><span data-stu-id="9b57f-124">**visPLOCtrlAsInput**</span></span> <br/> |
   

