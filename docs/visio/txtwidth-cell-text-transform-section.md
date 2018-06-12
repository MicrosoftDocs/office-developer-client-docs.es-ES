---
title: Celda TxtWidth (Sección de transformación de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251270
localization_priority: Normal
ms.assetid: e2215c67-25fa-1d75-9cce-f126bb8760a1
description: 'Determina el ancho del bloque de texto. La fórmula predeterminada es:'
ms.openlocfilehash: ecba66aaf1f7eeb6d16c6b0d4c6569aed051910f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823477"
---
# <a name="txtwidth-cell-text-transform-section"></a><span data-ttu-id="9382c-104">Celda TxtWidth (Sección de transformación de texto)</span><span class="sxs-lookup"><span data-stu-id="9382c-104">TxtWidth Cell (Text Transform Section)</span></span>

<span data-ttu-id="9382c-p102">Determina el ancho del bloque de texto. La fórmula predeterminada es:</span><span class="sxs-lookup"><span data-stu-id="9382c-p102">Determines the width of the text block. The default formula is:</span></span>
  
<span data-ttu-id="9382c-107">= Width \* 1</span><span class="sxs-lookup"><span data-stu-id="9382c-107">= Width \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9382c-108">Notas</span><span class="sxs-lookup"><span data-stu-id="9382c-108">Remarks</span></span>

<span data-ttu-id="9382c-109">Para obtener una referencia a la celda TxtWidth por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="9382c-109">To get a reference to the TxtWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9382c-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="9382c-110">Cell name:</span></span>  <br/> | <span data-ttu-id="9382c-111">TxtWidth</span><span class="sxs-lookup"><span data-stu-id="9382c-111">TxtWidth</span></span>  <br/> |
   
<span data-ttu-id="9382c-112">Para obtener una referencia a la celda TxtWidth por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9382c-112">To get a reference to the TxtWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9382c-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="9382c-113">Section index:</span></span>  <br/> |<span data-ttu-id="9382c-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9382c-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9382c-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="9382c-115">Row index:</span></span>  <br/> |<span data-ttu-id="9382c-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="9382c-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="9382c-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="9382c-117">Cell index:</span></span>  <br/> |<span data-ttu-id="9382c-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="9382c-118">**visXFormWidth**</span></span> <br/> |
   

