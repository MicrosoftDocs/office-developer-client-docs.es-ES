---
title: Celda NonPrinting (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251321
localization_priority: Normal
ms.assetid: 59fe0887-2092-4fad-ea38-2aba354f3b92
description: Habilita y deshabilita la impresión para la forma seleccionada.
ms.openlocfilehash: c3e1fc1b2d91fa4808f8ea89c904218c2236f5b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357235"
---
# <a name="nonprinting-cell-miscellaneous-section"></a><span data-ttu-id="c4986-103">Celda NonPrinting (sección de varios)</span><span class="sxs-lookup"><span data-stu-id="c4986-103">NonPrinting Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="c4986-104">Habilita y deshabilita la impresión para la forma seleccionada.</span><span class="sxs-lookup"><span data-stu-id="c4986-104">Switches printing on and off for the selected shape.</span></span>
  
|<span data-ttu-id="c4986-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="c4986-105">**Value**</span></span>|<span data-ttu-id="c4986-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c4986-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c4986-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c4986-107">TRUE</span></span>  <br/> | <span data-ttu-id="c4986-108">Se deshabilita la impresión, pero la forma se mostrará en la ventana de dibujo.</span><span class="sxs-lookup"><span data-stu-id="c4986-108">Printing disabled, but the shape will be displayed in the drawing window.</span></span>  <br/> |
| <span data-ttu-id="c4986-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c4986-109">FALSE</span></span>  <br/> | <span data-ttu-id="c4986-110">Se habilita la impresión.</span><span class="sxs-lookup"><span data-stu-id="c4986-110">Printing enabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4986-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c4986-111">Remarks</span></span>

<span data-ttu-id="c4986-112">Puede imprimir una guía si la selecciona y establece el valor de su celda NonPrinting en FALSE.</span><span class="sxs-lookup"><span data-stu-id="c4986-112">You can print a guide by selecting it, and then setting the value of its NonPrinting cell to FALSE.</span></span>
  
<span data-ttu-id="c4986-113">Para obtener una referencia a la celda NonPrinting por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="c4986-113">To get a reference to the NonPrinting cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c4986-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c4986-114">Cell name:</span></span>  <br/> | <span data-ttu-id="c4986-115">No imprimibles</span><span class="sxs-lookup"><span data-stu-id="c4986-115">NonPrinting</span></span>  <br/> |
   
<span data-ttu-id="c4986-116">Para obtener una referencia a la celda NonPrinting por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c4986-116">To get a reference to the NonPrinting cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c4986-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c4986-117">Section index:</span></span>  <br/> |<span data-ttu-id="c4986-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c4986-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c4986-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c4986-119">Row index:</span></span>  <br/> |<span data-ttu-id="c4986-120">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="c4986-120">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="c4986-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c4986-121">Cell index:</span></span>  <br/> |<span data-ttu-id="c4986-122">**visNonPrinting**</span><span class="sxs-lookup"><span data-stu-id="c4986-122">**visNonPrinting**</span></span> <br/> |
   

