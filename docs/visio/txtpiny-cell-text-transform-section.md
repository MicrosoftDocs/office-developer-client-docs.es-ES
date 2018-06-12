---
title: Celda TxtPinY (Sección de transformación de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1045
localization_priority: Normal
ms.assetid: 88ddf4b5-8248-8c1a-c387-09a607639d26
description: 'Determina la y-coordenadas del centro del bloque de texto de la rotación en relación con el origen de la forma. La fórmula predeterminada es:'
ms.openlocfilehash: e8101463413b177bf8ddd80ed52964d3eeae788f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823461"
---
# <a name="txtpiny-cell-text-transform-section"></a><span data-ttu-id="5274c-104">Celda TxtPinY (Sección de transformación de texto)</span><span class="sxs-lookup"><span data-stu-id="5274c-104">TxtPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="5274c-105">Determina la *y* -coordenadas del centro del bloque de texto de la rotación en relación con el origen de la forma.</span><span class="sxs-lookup"><span data-stu-id="5274c-105">Determines the  *y*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="5274c-106">La fórmula predeterminada es:</span><span class="sxs-lookup"><span data-stu-id="5274c-106">The default formula is:</span></span> 
  
<span data-ttu-id="5274c-107">= Alto \* 0,5</span><span class="sxs-lookup"><span data-stu-id="5274c-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5274c-108">Notas</span><span class="sxs-lookup"><span data-stu-id="5274c-108">Remarks</span></span>

<span data-ttu-id="5274c-109">Para obtener una referencia a la celda TxtPinY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="5274c-109">To get a reference to the TxtPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5274c-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="5274c-110">Cell name:</span></span>  <br/> | <span data-ttu-id="5274c-111">TxtPinY</span><span class="sxs-lookup"><span data-stu-id="5274c-111">TxtPinY</span></span>  <br/> |
   
<span data-ttu-id="5274c-112">Para obtener una referencia a la celda TxtPinY por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5274c-112">To get a reference to the TxtPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5274c-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="5274c-113">Section index:</span></span>  <br/> |<span data-ttu-id="5274c-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5274c-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5274c-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="5274c-115">Row index:</span></span>  <br/> |<span data-ttu-id="5274c-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="5274c-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="5274c-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="5274c-117">Cell index:</span></span>  <br/> |<span data-ttu-id="5274c-118">**visXFormPinY**</span><span class="sxs-lookup"><span data-stu-id="5274c-118">**visXFormPinY**</span></span> <br/> |
   

