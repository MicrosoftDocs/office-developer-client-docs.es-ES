---
title: Celda BeginArrow (Sección de formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51105
localization_priority: Normal
ms.assetid: 0ab4044e-2d77-1fbe-ef20-5d029bc064ba
description: Indica si una línea tiene una punta de flecha u otro formato de extremo de línea como primer vértice. Escriba un número entre 0 y 45 o la función USE con el nombre de un extremo de línea personalizado, o bien, utilice el cuadro de diálogo Línea.
ms.openlocfilehash: c6d5a66d76cfea61b1c9923c5b904dadec5495f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821549"
---
# <a name="beginarrow-cell-line-format-section"></a><span data-ttu-id="41e65-104">Celda BeginArrow (sección Formato de línea)</span><span class="sxs-lookup"><span data-stu-id="41e65-104">BeginArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="41e65-p102">Indica si una línea tiene una punta de flecha u otro formato de extremo de línea como primer vértice. Escriba un número entre 0 y 45 o la función USE con el nombre de un extremo de línea personalizado, o bien, utilice el cuadro de diálogo **Línea**.</span><span class="sxs-lookup"><span data-stu-id="41e65-p102">Indicates whether a line has an arrowhead or other line end format at its first vertex. Enter a number from 0 to 45 or the USE function with the name of a custom line end, or use the **Line** dialog box.</span></span> 
  
|<span data-ttu-id="41e65-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="41e65-107">**Value**</span></span>|<span data-ttu-id="41e65-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="41e65-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="41e65-109">0</span><span class="sxs-lookup"><span data-stu-id="41e65-109">0</span></span>  <br/> | <span data-ttu-id="41e65-110">No hay punta de flecha.</span><span class="sxs-lookup"><span data-stu-id="41e65-110">No arrowhead.</span></span>  <br/> |
| <span data-ttu-id="41e65-111">1: 45</span><span class="sxs-lookup"><span data-stu-id="41e65-111">1 - 45</span></span>  <br/> | <span data-ttu-id="41e65-112">Varios estilos de punta de flecha que se corresponden con las entradas indizadas del cuadro de diálogo **Línea**.</span><span class="sxs-lookup"><span data-stu-id="41e65-112">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41e65-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="41e65-113">Remarks</span></span>

<span data-ttu-id="41e65-114">El tamaño de la punta de flecha se establece en la celda BeginArrowSize.</span><span class="sxs-lookup"><span data-stu-id="41e65-114">The size of the arrowhead is set in the BeginArrowSize cell.</span></span>
  
<span data-ttu-id="41e65-115">Para obtener una referencia a la celda BeginArrow por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="41e65-115">To get a reference to the BeginArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="41e65-116">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="41e65-116">Cell name:</span></span>  <br/> | <span data-ttu-id="41e65-117">BeginArrow</span><span class="sxs-lookup"><span data-stu-id="41e65-117">BeginArrow</span></span>  <br/> |
   
<span data-ttu-id="41e65-118">Para obtener una referencia a la celda BeginArrow por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="41e65-118">To get a reference to the BeginArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="41e65-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="41e65-119">Section index:</span></span>  <br/> |<span data-ttu-id="41e65-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="41e65-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="41e65-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="41e65-121">Row index:</span></span>  <br/> |<span data-ttu-id="41e65-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="41e65-122">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="41e65-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="41e65-123">Cell index:</span></span>  <br/> |<span data-ttu-id="41e65-124">**visLineBeginArrow**</span><span class="sxs-lookup"><span data-stu-id="41e65-124">**visLineBeginArrow**</span></span> <br/> |
   

