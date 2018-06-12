---
title: Celda TxtPinX (Sección de transformación de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
localization_priority: Normal
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: 'Determina la x-coordenadas del centro del bloque de texto de la rotación en relación con el origen de la forma. La fórmula predeterminada es:'
ms.openlocfilehash: df103557d103dbde7e4a1c8d67cabe37a0af9311
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823455"
---
# <a name="txtpinx-cell-text-transform-section"></a><span data-ttu-id="4c3ea-104">Celda TxtPinX (Sección de transformación de texto)</span><span class="sxs-lookup"><span data-stu-id="4c3ea-104">TxtPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="4c3ea-105">Determina la *x* -coordenadas del centro del bloque de texto de la rotación en relación con el origen de la forma.</span><span class="sxs-lookup"><span data-stu-id="4c3ea-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="4c3ea-106">La fórmula predeterminada es:</span><span class="sxs-lookup"><span data-stu-id="4c3ea-106">The default formula is:</span></span> 
  
<span data-ttu-id="4c3ea-107">= Width \* 0,5</span><span class="sxs-lookup"><span data-stu-id="4c3ea-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4c3ea-108">Notas</span><span class="sxs-lookup"><span data-stu-id="4c3ea-108">Remarks</span></span>

<span data-ttu-id="4c3ea-109">Para obtener una referencia a la celda TxtPinX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="4c3ea-109">To get a reference to the TxtPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4c3ea-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="4c3ea-110">Cell name:</span></span>  <br/> | <span data-ttu-id="4c3ea-111">TxtPinX</span><span class="sxs-lookup"><span data-stu-id="4c3ea-111">TxtPinX</span></span>  <br/> |
   
<span data-ttu-id="4c3ea-112">Para obtener una referencia a la celda TxtPinX por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4c3ea-112">To get a reference to the TxtPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4c3ea-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="4c3ea-113">Section index:</span></span>  <br/> |<span data-ttu-id="4c3ea-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4c3ea-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4c3ea-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="4c3ea-115">Row index:</span></span>  <br/> |<span data-ttu-id="4c3ea-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="4c3ea-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="4c3ea-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="4c3ea-117">Cell index:</span></span>  <br/> |<span data-ttu-id="4c3ea-118">**visXFormPinX**</span><span class="sxs-lookup"><span data-stu-id="4c3ea-118">**visXFormPinX**</span></span> <br/> |
   

