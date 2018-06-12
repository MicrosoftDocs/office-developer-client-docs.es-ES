---
title: Celda SpLine (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm970
localization_priority: Normal
ms.assetid: 84f4e5f1-7c28-9e83-8644-28d117bb10a5
description: Determina la distancia entre una línea de texto y la siguiente, expresada como un porcentaje, donde 100% es el alto de una línea de texto.
ms.openlocfilehash: f2f290564d49a056bc3366707b25a7991f8c4401
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823303"
---
# <a name="spline-cell-paragraph-section"></a><span data-ttu-id="c2de4-103">Celda SpLine (Sección de párrafo)</span><span class="sxs-lookup"><span data-stu-id="c2de4-103">SpLine Cell (Paragraph Section)</span></span>

<span data-ttu-id="c2de4-104">Determina la distancia entre una línea de texto y la siguiente, expresada como un porcentaje, donde 100% es el alto de una línea de texto.</span><span class="sxs-lookup"><span data-stu-id="c2de4-104">Determines the distance between one line of text and the next, expressed as a percentage, where 100% is the height of a text line.</span></span>
  
|<span data-ttu-id="c2de4-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c2de4-105">**Value**</span></span>|<span data-ttu-id="c2de4-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c2de4-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c2de4-107">\>0</span><span class="sxs-lookup"><span data-stu-id="c2de4-107">\>0</span></span>  <br/> | <span data-ttu-id="c2de4-108">Espaciado absoluto, independiente del tamaño de la fuente</span><span class="sxs-lookup"><span data-stu-id="c2de4-108">Absolute spacing, regardless of font size</span></span>  <br/> |
| <span data-ttu-id="c2de4-109">=0</span><span class="sxs-lookup"><span data-stu-id="c2de4-109">=0</span></span>  <br/> | <span data-ttu-id="c2de4-110">Se establece como sólido (espaciado = 100% del tamaño de la fuente)</span><span class="sxs-lookup"><span data-stu-id="c2de4-110">Set solid (spacing = 100% of font size)</span></span>  <br/> |
| <span data-ttu-id="c2de4-111">\<0</span><span class="sxs-lookup"><span data-stu-id="c2de4-111">\<0</span></span>  <br/> | <span data-ttu-id="c2de4-112">Un porcentaje del tamaño de la fuente (por ejemplo, -120% produce un espaciado del 120%)</span><span class="sxs-lookup"><span data-stu-id="c2de4-112">A percentage of font size (for example, -120% yields 120% spacing)</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2de4-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c2de4-113">Remarks</span></span>

<span data-ttu-id="c2de4-114">Para obtener una referencia a la celda SpLine por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="c2de4-114">To get a reference to the SpLine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2de4-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c2de4-115">Cell name:</span></span>  <br/> | <span data-ttu-id="c2de4-116">Párrafo.</span><span class="sxs-lookup"><span data-stu-id="c2de4-116">Para.</span></span> <span data-ttu-id="c2de4-117">SpLine [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c2de4-117">SpLine [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c2de4-118">Para obtener una referencia a la celda SpLine por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c2de4-118">To get a reference to the SpLine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2de4-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c2de4-119">Section index:</span></span>  <br/> |<span data-ttu-id="c2de4-120">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="c2de4-120">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="c2de4-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c2de4-121">Row index:</span></span>  <br/> |<span data-ttu-id="c2de4-122">**visRowParagraph** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c2de4-122">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c2de4-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c2de4-123">Cell index:</span></span>  <br/> |<span data-ttu-id="c2de4-124">**visSpaceLine**</span><span class="sxs-lookup"><span data-stu-id="c2de4-124">**visSpaceLine**</span></span> <br/> |
   

