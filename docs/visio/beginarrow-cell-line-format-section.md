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
ms.openlocfilehash: cf5a512dabd0e6296b83fa7bfd2a2a6134143d50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410297"
---
# <a name="beginarrow-cell-line-format-section"></a><span data-ttu-id="31d55-104">Celda BeginArrow (Sección de formato de línea)</span><span class="sxs-lookup"><span data-stu-id="31d55-104">BeginArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="31d55-p102">Indica si una línea tiene una punta de flecha u otro formato de extremo de línea como primer vértice. Escriba un número entre 0 y 45 o la función USE con el nombre de un extremo de línea personalizado, o bien, utilice el cuadro de diálogo **Línea**.</span><span class="sxs-lookup"><span data-stu-id="31d55-p102">Indicates whether a line has an arrowhead or other line end format at its first vertex. Enter a number from 0 to 45 or the USE function with the name of a custom line end, or use the **Line** dialog box.</span></span> 
  
|<span data-ttu-id="31d55-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="31d55-107">**Value**</span></span>|<span data-ttu-id="31d55-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="31d55-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="31d55-109">comprendi</span><span class="sxs-lookup"><span data-stu-id="31d55-109">0</span></span>  <br/> | <span data-ttu-id="31d55-110">No hay punta de flecha.</span><span class="sxs-lookup"><span data-stu-id="31d55-110">No arrowhead.</span></span>  <br/> |
| <span data-ttu-id="31d55-111">1 -45</span><span class="sxs-lookup"><span data-stu-id="31d55-111">1 - 45</span></span>  <br/> | <span data-ttu-id="31d55-112">Varios estilos de punta de flecha que se corresponden con las entradas indizadas del cuadro de diálogo **Línea**.</span><span class="sxs-lookup"><span data-stu-id="31d55-112">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31d55-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="31d55-113">Remarks</span></span>

<span data-ttu-id="31d55-114">El tamaño de la punta de flecha se establece en la celda BeginArrowSize.</span><span class="sxs-lookup"><span data-stu-id="31d55-114">The size of the arrowhead is set in the BeginArrowSize cell.</span></span>
  
<span data-ttu-id="31d55-115">Para obtener una referencia a la celda BeginArrow por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="31d55-115">To get a reference to the BeginArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="31d55-116">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="31d55-116">Cell name:</span></span>  <br/> | <span data-ttu-id="31d55-117">BeginArrow</span><span class="sxs-lookup"><span data-stu-id="31d55-117">BeginArrow</span></span>  <br/> |
   
<span data-ttu-id="31d55-118">Para obtener una referencia a la celda BeginArrow por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="31d55-118">To get a reference to the BeginArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="31d55-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="31d55-119">Section index:</span></span>  <br/> |<span data-ttu-id="31d55-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="31d55-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="31d55-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="31d55-121">Row index:</span></span>  <br/> |<span data-ttu-id="31d55-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="31d55-122">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="31d55-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="31d55-123">Cell index:</span></span>  <br/> |<span data-ttu-id="31d55-124">**visLineBeginArrow**</span><span class="sxs-lookup"><span data-stu-id="31d55-124">**visLineBeginArrow**</span></span> <br/> |
   

