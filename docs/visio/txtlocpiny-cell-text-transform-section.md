---
title: Celda TxtLocPinY (Sección de transformación de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251276
localization_priority: Normal
ms.assetid: 3f46cfcf-7eac-4a37-e782-39f4e7f8fc43
description: 'Determina la coordenada y del centro de rotación del bloque de texto en relación con el origen del bloque de texto. La fórmula predeterminada es:'
ms.openlocfilehash: 937c4e9928d32d55e8336d192b1ecc6140fd8381
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414063"
---
# <a name="txtlocpiny-cell-text-transform-section"></a><span data-ttu-id="5e5a7-104">Celda TxtLocPinY (Sección de transformación de texto)</span><span class="sxs-lookup"><span data-stu-id="5e5a7-104">TxtLocPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="5e5a7-105">Determina la coordenada *y* del centro de rotación del bloque de texto en relación con el origen del bloque de texto.</span><span class="sxs-lookup"><span data-stu-id="5e5a7-105">Determines the  *y*  -coordinate of the text block's center of rotation relative to the origin of the text block.</span></span> <span data-ttu-id="5e5a7-106">La fórmula predeterminada es:</span><span class="sxs-lookup"><span data-stu-id="5e5a7-106">The default formula is:</span></span> 
  
<span data-ttu-id="5e5a7-107">= TxtHeight \* 0,5</span><span class="sxs-lookup"><span data-stu-id="5e5a7-107">= TxtHeight \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5e5a7-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5e5a7-108">Remarks</span></span>

<span data-ttu-id="5e5a7-109">Para obtener una referencia a la celda TxtLocPinY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="5e5a7-109">To get a reference to the TxtLocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5e5a7-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="5e5a7-110">Cell name:</span></span>  <br/> | <span data-ttu-id="5e5a7-111">TxtLocPinY</span><span class="sxs-lookup"><span data-stu-id="5e5a7-111">TxtLocPinY</span></span>  <br/> |
   
<span data-ttu-id="5e5a7-112">Para obtener una referencia desde un programa a la celda TxtLocPinY por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5e5a7-112">To get a reference to the TxtLocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5e5a7-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="5e5a7-113">Section index:</span></span>  <br/> |<span data-ttu-id="5e5a7-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5e5a7-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5e5a7-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="5e5a7-115">Row index:</span></span>  <br/> |<span data-ttu-id="5e5a7-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="5e5a7-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="5e5a7-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="5e5a7-117">Cell index:</span></span>  <br/> |<span data-ttu-id="5e5a7-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="5e5a7-118">**visXFormLocPinY**</span></span> <br/> |
   

