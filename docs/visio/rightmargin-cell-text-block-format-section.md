---
title: Celda RightMargin (Sección de formato del bloque de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251266
localization_priority: Normal
ms.assetid: bc8f5469-e79f-4a68-73cb-d11c938353a4
description: Determina la distancia entre el borde derecho del bloque de texto y el texto que contiene. El valor predeterminado es 0,25 centímetros.
ms.openlocfilehash: 57fdb320395a9a6562983a0148b37c4a70a9a9b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822990"
---
# <a name="rightmargin-cell-text-block-format-section"></a><span data-ttu-id="b3d4a-104">Celda RightMargin (sección Formato del bloque de texto)</span><span class="sxs-lookup"><span data-stu-id="b3d4a-104">RightMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="b3d4a-p102">Determina la distancia entre el borde derecho del bloque de texto y el texto que contiene. El valor predeterminado es 0,25 centímetros.</span><span class="sxs-lookup"><span data-stu-id="b3d4a-p102">Determines the distance between the right border of the text block and the text it contains. The default is 0.1 inch.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b3d4a-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b3d4a-107">Remarks</span></span>

<span data-ttu-id="b3d4a-p103">Este valor no depende de la escala del dibujo. Si se cambia la escala del dibujo, el margen derecho permanece igual.</span><span class="sxs-lookup"><span data-stu-id="b3d4a-p103">This value is independent of the scale of the drawing. If the drawing is scaled, the right margin remains the same.</span></span>
  
<span data-ttu-id="b3d4a-110">Para obtener una referencia a la celda RightMargin por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="b3d4a-110">To get a reference to the RightMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3d4a-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b3d4a-111">Cell name:</span></span>  <br/> | <span data-ttu-id="b3d4a-112">RightMargin</span><span class="sxs-lookup"><span data-stu-id="b3d4a-112">RightMargin</span></span>  <br/> |
   
<span data-ttu-id="b3d4a-113">Para obtener una referencia desde un programa a la celda RightMargin por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b3d4a-113">To get a reference to the RightMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3d4a-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b3d4a-114">Section index:</span></span>  <br/> |<span data-ttu-id="b3d4a-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b3d4a-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b3d4a-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b3d4a-116">Row index:</span></span>  <br/> |<span data-ttu-id="b3d4a-117">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="b3d4a-117">**visRowText**</span></span> <br/> |
| <span data-ttu-id="b3d4a-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b3d4a-118">Cell index:</span></span>  <br/> |<span data-ttu-id="b3d4a-119">**visTxtBlkRightMargin**</span><span class="sxs-lookup"><span data-stu-id="b3d4a-119">**visTxtBlkRightMargin**</span></span> <br/> |
   

