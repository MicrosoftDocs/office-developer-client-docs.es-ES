---
title: Celda LineCap (Sección de formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251231
localization_priority: Normal
ms.assetid: 3519216b-b6cf-2e8c-e20f-adfa373c9028
description: Indica si los remates de una línea son redondos, cuadrados o extendidos.
ms.openlocfilehash: 44de4bff87fd3d121dfce9eec934ec39bc61065a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425206"
---
# <a name="linecap-cell-line-format-section"></a><span data-ttu-id="b83b7-103">Celda LineCap (Sección de formato de línea)</span><span class="sxs-lookup"><span data-stu-id="b83b7-103">LineCap Cell (Line Format Section)</span></span>

<span data-ttu-id="b83b7-104">Indica si los remates de una línea son redondos, cuadrados o extendidos.</span><span class="sxs-lookup"><span data-stu-id="b83b7-104">Indicates whether a line has rounded, square, or extended line caps.</span></span>
  
|<span data-ttu-id="b83b7-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b83b7-105">**Value**</span></span>|<span data-ttu-id="b83b7-106">**Estilo de extremo de línea**</span><span class="sxs-lookup"><span data-stu-id="b83b7-106">**Line end style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b83b7-107">comprendi</span><span class="sxs-lookup"><span data-stu-id="b83b7-107">0</span></span>  <br/> |<span data-ttu-id="b83b7-108">Redondea</span><span class="sxs-lookup"><span data-stu-id="b83b7-108">Rounded</span></span>  <br/> |
|<span data-ttu-id="b83b7-109">1</span><span class="sxs-lookup"><span data-stu-id="b83b7-109">1</span></span>  <br/> |<span data-ttu-id="b83b7-110">Cuadrado</span><span class="sxs-lookup"><span data-stu-id="b83b7-110">Square</span></span>  <br/> |
|<span data-ttu-id="b83b7-111">segundo</span><span class="sxs-lookup"><span data-stu-id="b83b7-111">2</span></span>  <br/> |<span data-ttu-id="b83b7-112">Extendido</span><span class="sxs-lookup"><span data-stu-id="b83b7-112">Extended</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b83b7-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b83b7-113">Remarks</span></span>

<span data-ttu-id="b83b7-114">También puede establecer el valor de esta celda en el cuadro de diálogo **Línea** (en la ficha **Inicio**, en el grupo **Forma**, haga clic en **Línea**, seleccione **Flechas** y, a continuación, haga clic en **Más flechas**).</span><span class="sxs-lookup"><span data-stu-id="b83b7-114">You can also set the value of this cell in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span>
  
<span data-ttu-id="b83b7-115">Para obtener una referencia a la celda LineCap por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="b83b7-115">To get a reference to the LineCap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b83b7-116">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b83b7-116">Cell name:</span></span>  <br/> |<span data-ttu-id="b83b7-117">LineCap</span><span class="sxs-lookup"><span data-stu-id="b83b7-117">LineCap</span></span>  <br/> |
   
<span data-ttu-id="b83b7-118">Para obtener una referencia desde un programa a la celda LineCap por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b83b7-118">To get a reference to the LineCap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b83b7-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b83b7-119">Section index:</span></span>  <br/> |<span data-ttu-id="b83b7-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b83b7-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b83b7-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b83b7-121">Row index:</span></span>  <br/> |<span data-ttu-id="b83b7-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="b83b7-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="b83b7-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b83b7-123">Cell index:</span></span>  <br/> |<span data-ttu-id="b83b7-124">**visLineEndCap**</span><span class="sxs-lookup"><span data-stu-id="b83b7-124">**visLineEndCap**</span></span> <br/> |
   

