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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282911"
---
# <a name="ctrlasinput-cell-page-layout-section"></a><span data-ttu-id="6942c-104">Celda CtrlAsInput (Sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="6942c-104">CtrlAsInput Cell (Page Layout Section)</span></span>

<span data-ttu-id="6942c-p102">Determina qué forma es la principal cuando se emplean formas con controladores. Esta celda establece el comportamiento de todas las formas en la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="6942c-p102">Determines which shape is the parent when using shapes with control handles. This cell sets the behavior for all the shapes on the drawing page.</span></span>
  
|<span data-ttu-id="6942c-107">**Value**</span><span class="sxs-lookup"><span data-stu-id="6942c-107">**Value**</span></span>|<span data-ttu-id="6942c-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6942c-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6942c-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="6942c-109">TRUE</span></span>  <br/> | <span data-ttu-id="6942c-110">Se establece como forma principal la forma a la que está conectado el controlador.</span><span class="sxs-lookup"><span data-stu-id="6942c-110">Set the shape that the control handle is connected to as the parent.</span></span>  <br/> |
| <span data-ttu-id="6942c-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="6942c-111">FALSE</span></span>  <br/> | <span data-ttu-id="6942c-p103">Valor predeterminado. Se establece como forma principal la forma que contiene el controlador.</span><span class="sxs-lookup"><span data-stu-id="6942c-p103">The default. Set shape that contains the control handle as the parent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6942c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6942c-114">Remarks</span></span>

<span data-ttu-id="6942c-115">Para obtener una referencia a la celda CtrlAsInput por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="6942c-115">To get a reference to the CtrlAsInput cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6942c-116">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="6942c-116">Cell name:</span></span>  <br/> | <span data-ttu-id="6942c-117">CtrlAsInput</span><span class="sxs-lookup"><span data-stu-id="6942c-117">CtrlAsInput</span></span>  <br/> |
   
<span data-ttu-id="6942c-118">Para obtener una referencia desde un programa a la celda CtrlAsInput por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6942c-118">To get a reference to the CtrlAsInput cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6942c-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="6942c-119">Section index:</span></span>  <br/> |<span data-ttu-id="6942c-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6942c-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6942c-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="6942c-121">Row index:</span></span>  <br/> |<span data-ttu-id="6942c-122">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="6942c-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="6942c-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="6942c-123">Cell index:</span></span>  <br/> |<span data-ttu-id="6942c-124">**visPLOCtrlAsInput**</span><span class="sxs-lookup"><span data-stu-id="6942c-124">**visPLOCtrlAsInput**</span></span> <br/> |
   

