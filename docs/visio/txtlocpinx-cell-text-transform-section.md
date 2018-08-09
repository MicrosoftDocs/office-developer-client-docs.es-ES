---
title: Celda TxtLocPinX (Sección de transformación de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
localization_priority: Normal
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: 'Determina la x-coordenadas del centro del bloque de texto de rotación con respecto al origen del bloque de texto. La fórmula predeterminada es:'
ms.openlocfilehash: 6eb48532bb19bce5b0d22ed2cd0997014721df88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823444"
---
# <a name="txtlocpinx-cell-text-transform-section"></a><span data-ttu-id="9a85f-104">Celda TxtLocPinX (sección Transformación de texto)</span><span class="sxs-lookup"><span data-stu-id="9a85f-104">TxtLocPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="9a85f-105">Determina la *x* -coordenadas del centro del bloque de texto de rotación con respecto al origen del bloque de texto.</span><span class="sxs-lookup"><span data-stu-id="9a85f-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the text block.</span></span> <span data-ttu-id="9a85f-106">La fórmula predeterminada es:</span><span class="sxs-lookup"><span data-stu-id="9a85f-106">The default formula is:</span></span> 
  
<span data-ttu-id="9a85f-107">= TxtWidth \* 0,5</span><span class="sxs-lookup"><span data-stu-id="9a85f-107">= TxtWidth \* 0.5</span></span>
  
<span data-ttu-id="9a85f-108">Esta fórmula da como resultado el centro horizontal del bloque de texto.</span><span class="sxs-lookup"><span data-stu-id="9a85f-108">This formula evaluates to the horizontal center of the text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9a85f-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9a85f-109">Remarks</span></span>

<span data-ttu-id="9a85f-110">Para obtener una referencia a la celda TxtLocPinX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="9a85f-110">To get a reference to the TxtLocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9a85f-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="9a85f-111">Cell name:</span></span>  <br/> | <span data-ttu-id="9a85f-112">TxtLocPinX</span><span class="sxs-lookup"><span data-stu-id="9a85f-112">TxtLocPinX</span></span>  <br/> |
   
<span data-ttu-id="9a85f-113">Para obtener una referencia desde un programa a la celda TxtLocPinX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9a85f-113">To get a reference to the TxtLocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9a85f-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="9a85f-114">Section index:</span></span>  <br/> |<span data-ttu-id="9a85f-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9a85f-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9a85f-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="9a85f-116">Row index:</span></span>  <br/> |<span data-ttu-id="9a85f-117">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="9a85f-117">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="9a85f-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="9a85f-118">Cell index:</span></span>  <br/> |<span data-ttu-id="9a85f-119">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="9a85f-119">**visXFormLocPinX**</span></span> <br/> |
   

