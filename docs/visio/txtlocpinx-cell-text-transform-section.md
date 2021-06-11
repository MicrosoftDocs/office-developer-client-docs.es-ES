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
description: 'Determina la coordenada x del centro de rotación del bloque de texto en relación con el origen del bloque de texto. La fórmula predeterminada es:'
ms.openlocfilehash: 390f8129e8000a043969eda0ab1c8e4ef62515ef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425858"
---
# <a name="txtlocpinx-cell-text-transform-section"></a><span data-ttu-id="b5381-104">Celda TxtLocPinX (Sección de transformación de texto)</span><span class="sxs-lookup"><span data-stu-id="b5381-104">TxtLocPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="b5381-105">Determina la coordenada  *x*  del centro de rotación del bloque de texto en relación con el origen del bloque de texto.</span><span class="sxs-lookup"><span data-stu-id="b5381-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the text block.</span></span> <span data-ttu-id="b5381-106">La fórmula predeterminada es:</span><span class="sxs-lookup"><span data-stu-id="b5381-106">The default formula is:</span></span> 
  
<span data-ttu-id="b5381-107">= TxtWidth \* 0.5</span><span class="sxs-lookup"><span data-stu-id="b5381-107">= TxtWidth \* 0.5</span></span>
  
<span data-ttu-id="b5381-108">Esta fórmula da como resultado el centro horizontal del bloque de texto.</span><span class="sxs-lookup"><span data-stu-id="b5381-108">This formula evaluates to the horizontal center of the text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b5381-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b5381-109">Remarks</span></span>

<span data-ttu-id="b5381-110">Para obtener una referencia a la celda TxtLocPinX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="b5381-110">To get a reference to the TxtLocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b5381-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b5381-111">Cell name:</span></span>  <br/> | <span data-ttu-id="b5381-112">TxtLocPinX</span><span class="sxs-lookup"><span data-stu-id="b5381-112">TxtLocPinX</span></span>  <br/> |
   
<span data-ttu-id="b5381-113">Para obtener una referencia desde un programa a la celda TxtLocPinX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b5381-113">To get a reference to the TxtLocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b5381-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b5381-114">Section index:</span></span>  <br/> |<span data-ttu-id="b5381-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b5381-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b5381-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b5381-116">Row index:</span></span>  <br/> |<span data-ttu-id="b5381-117">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="b5381-117">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="b5381-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b5381-118">Cell index:</span></span>  <br/> |<span data-ttu-id="b5381-119">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="b5381-119">**visXFormLocPinX**</span></span> <br/> |
   

