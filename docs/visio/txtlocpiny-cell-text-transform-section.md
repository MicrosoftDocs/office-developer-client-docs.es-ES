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
description: 'Determina la y-coordenadas del centro del bloque de texto de rotación en relación con el origen del bloque de texto. La fórmula predeterminada es:'
ms.openlocfilehash: 7d43f63b8560df5fc5daf09a429ce30ec976d131
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823453"
---
# <a name="txtlocpiny-cell-text-transform-section"></a><span data-ttu-id="a0318-104">Celda TxtLocPinY (sección Transformación de texto)</span><span class="sxs-lookup"><span data-stu-id="a0318-104">TxtLocPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="a0318-105">Determina la *y* -coordenadas del centro del bloque de texto de rotación en relación con el origen del bloque de texto.</span><span class="sxs-lookup"><span data-stu-id="a0318-105">Determines the  *y*  -coordinate of the text block's center of rotation relative to the origin of the text block.</span></span> <span data-ttu-id="a0318-106">La fórmula predeterminada es:</span><span class="sxs-lookup"><span data-stu-id="a0318-106">The default formula is:</span></span> 
  
<span data-ttu-id="a0318-107">= TxtHeight \* 0,5</span><span class="sxs-lookup"><span data-stu-id="a0318-107">= TxtHeight \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a0318-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a0318-108">Remarks</span></span>

<span data-ttu-id="a0318-109">Para obtener una referencia a la celda TxtLocPinY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="a0318-109">To get a reference to the TxtLocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a0318-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="a0318-110">Cell name:</span></span>  <br/> | <span data-ttu-id="a0318-111">TxtLocPinY</span><span class="sxs-lookup"><span data-stu-id="a0318-111">TxtLocPinY</span></span>  <br/> |
   
<span data-ttu-id="a0318-112">Para obtener una referencia desde un programa a la celda TxtLocPinY por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a0318-112">To get a reference to the TxtLocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a0318-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="a0318-113">Section index:</span></span>  <br/> |<span data-ttu-id="a0318-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a0318-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a0318-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="a0318-115">Row index:</span></span>  <br/> |<span data-ttu-id="a0318-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="a0318-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="a0318-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="a0318-117">Cell index:</span></span>  <br/> |<span data-ttu-id="a0318-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="a0318-118">**visXFormLocPinY**</span></span> <br/> |
   

