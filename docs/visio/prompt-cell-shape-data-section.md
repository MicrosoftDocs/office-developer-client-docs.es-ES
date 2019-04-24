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
description: Especifica un texto descriptivo o con instrucciones que aparece como sugerencia cuando el mouse se detiene sobre un valor en la ventana Datos de formas.
ms.openlocfilehash: 4ecb7eb5a1e775d2f3f5271476ef45cdf020d7c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326820"
---
# <a name="prompt-cell-shape-data-section"></a><span data-ttu-id="fa67d-103">Celda Prompt (Sección de datos de formas)</span><span class="sxs-lookup"><span data-stu-id="fa67d-103">Prompt Cell (Shape Data Section)</span></span>

<span data-ttu-id="fa67d-104">Especifica un texto descriptivo o con instrucciones que aparece como sugerencia cuando el mouse se detiene sobre un valor en la ventana **Datos de formas**.</span><span class="sxs-lookup"><span data-stu-id="fa67d-104">Specifies descriptive or instructional text that appears as a tip when the mouse is paused over a value in the **Shape Data** window.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fa67d-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fa67d-105">Remarks</span></span>

<span data-ttu-id="fa67d-106">Para obtener una referencia a la celda Prompt por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="fa67d-106">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fa67d-107">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="fa67d-107">Cell name:</span></span>  <br/> | <span data-ttu-id="fa67d-108">Polyprop.  *Nombre* . Pregunta donde *nombre* es el nombre de la fila</span><span class="sxs-lookup"><span data-stu-id="fa67d-108">Prop.  *Name*  .Prompt where  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="fa67d-109">Para obtener una referencia desde un programa a la celda Prompt por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="fa67d-109">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fa67d-110">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="fa67d-110">Section index:</span></span>  <br/> |<span data-ttu-id="fa67d-111">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="fa67d-111">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="fa67d-112">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="fa67d-112">Row index:</span></span>  <br/> |<span data-ttu-id="fa67d-113">**visRowProp +** *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fa67d-113">**visRowProp +** *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="fa67d-114">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="fa67d-114">Cell index:</span></span>  <br/> |<span data-ttu-id="fa67d-115">**visCustPropsPrompt**</span><span class="sxs-lookup"><span data-stu-id="fa67d-115">**visCustPropsPrompt**</span></span> <br/> |
   

