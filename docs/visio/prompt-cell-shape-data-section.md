---
title: Celda Prompt (Sección de datos de formas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251343
localization_priority: Normal
ms.assetid: 42f42d73-a00c-ca93-adc9-4f8869b9cd42
description: Especifica el texto descriptivo o con instrucciones que aparece como sugerencia cuando el mouse se detiene sobre un valor en la ventana datos de formas.
ms.openlocfilehash: 1e11a8c7c680dd53ad7cd9f6877fe29eb34a7b53
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822863"
---
# <a name="prompt-cell-shape-data-section"></a><span data-ttu-id="6dd49-103">Celda Prompt (Sección de datos de formas)</span><span class="sxs-lookup"><span data-stu-id="6dd49-103">Prompt Cell (Shape Data Section)</span></span>

<span data-ttu-id="6dd49-104">Especifica el texto descriptivo o con instrucciones que aparece como sugerencia cuando el mouse se detiene sobre un valor en la ventana **Datos de formas** .</span><span class="sxs-lookup"><span data-stu-id="6dd49-104">Specifies descriptive or instructional text that appears as a tip when the mouse is paused over a value in the **Shape Data** window.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6dd49-105">Notas</span><span class="sxs-lookup"><span data-stu-id="6dd49-105">Remarks</span></span>

<span data-ttu-id="6dd49-106">Para obtener una referencia a la celda Prompt por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="6dd49-106">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6dd49-107">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="6dd49-107">Cell name:</span></span>  <br/> | <span data-ttu-id="6dd49-108">De propiedades.  *Nombre* . Donde *nombre* es el nombre de la fila de símbolo del sistema</span><span class="sxs-lookup"><span data-stu-id="6dd49-108">Prop.  *Name*  .Prompt where  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="6dd49-109">Para obtener una referencia a la celda Prompt por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6dd49-109">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6dd49-110">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="6dd49-110">Section index:</span></span>  <br/> |<span data-ttu-id="6dd49-111">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="6dd49-111">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="6dd49-112">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="6dd49-112">Row index:</span></span>  <br/> |<span data-ttu-id="6dd49-113">**visRowProp +** *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6dd49-113">**visRowProp +** *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6dd49-114">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="6dd49-114">Cell index:</span></span>  <br/> |<span data-ttu-id="6dd49-115">**visCustPropsPrompt**</span><span class="sxs-lookup"><span data-stu-id="6dd49-115">**visCustPropsPrompt**</span></span> <br/> |
   

