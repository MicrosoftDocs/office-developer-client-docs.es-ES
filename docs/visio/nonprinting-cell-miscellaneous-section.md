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
ms.openlocfilehash: ab00914a9c59cfe94b3f7273f89684f43328b4d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822676"
---
# <a name="nonprinting-cell-miscellaneous-section"></a><span data-ttu-id="245e5-103">Celda NonPrinting (sección Varios)</span><span class="sxs-lookup"><span data-stu-id="245e5-103">NonPrinting Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="245e5-104">Habilita y deshabilita la impresión para la forma seleccionada.</span><span class="sxs-lookup"><span data-stu-id="245e5-104">Switches printing on and off for the selected shape.</span></span>
  
|<span data-ttu-id="245e5-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="245e5-105">**Value**</span></span>|<span data-ttu-id="245e5-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="245e5-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="245e5-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="245e5-107">TRUE</span></span>  <br/> | <span data-ttu-id="245e5-108">Se deshabilita la impresión, pero la forma se mostrará en la ventana de dibujo.</span><span class="sxs-lookup"><span data-stu-id="245e5-108">Printing disabled, but the shape will be displayed in the drawing window.</span></span>  <br/> |
| <span data-ttu-id="245e5-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="245e5-109">FALSE</span></span>  <br/> | <span data-ttu-id="245e5-110">Se habilita la impresión.</span><span class="sxs-lookup"><span data-stu-id="245e5-110">Printing enabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="245e5-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="245e5-111">Remarks</span></span>

<span data-ttu-id="245e5-112">Puede imprimir una guía si la selecciona y establece el valor de su celda NonPrinting en FALSE.</span><span class="sxs-lookup"><span data-stu-id="245e5-112">You can print a guide by selecting it, and then setting the value of its NonPrinting cell to FALSE.</span></span>
  
<span data-ttu-id="245e5-113">Para obtener una referencia a la celda NonPrinting por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="245e5-113">To get a reference to the NonPrinting cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="245e5-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="245e5-114">Cell name:</span></span>  <br/> | <span data-ttu-id="245e5-115">No imprimibles</span><span class="sxs-lookup"><span data-stu-id="245e5-115">NonPrinting</span></span>  <br/> |
   
<span data-ttu-id="245e5-116">Para obtener una referencia a la celda NonPrinting por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="245e5-116">To get a reference to the NonPrinting cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="245e5-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="245e5-117">Section index:</span></span>  <br/> |<span data-ttu-id="245e5-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="245e5-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="245e5-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="245e5-119">Row index:</span></span>  <br/> |<span data-ttu-id="245e5-120">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="245e5-120">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="245e5-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="245e5-121">Cell index:</span></span>  <br/> |<span data-ttu-id="245e5-122">**visNonPrinting**</span><span class="sxs-lookup"><span data-stu-id="245e5-122">**visNonPrinting**</span></span> <br/> |
   

