---
title: Celda SpAfter (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm960
localization_priority: Normal
ms.assetid: 2dd56ae5-300e-ba09-a73a-83c2b6c2a0ef
description: Determina el espacio insertado después de cada párrafo en el bloque de texto de la forma, además del espacio que determinen la celda SpLine y, si se trata del último párrafo de un bloque de texto, la celda BottomMargin.
ms.openlocfilehash: 2b8fe7e2b0df09561d0db4367f917c8f4b71335d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439838"
---
# <a name="spafter-cell-paragraph-section"></a><span data-ttu-id="6dd32-103">Celda SpAfter (Sección de párrafo)</span><span class="sxs-lookup"><span data-stu-id="6dd32-103">SpAfter Cell (Paragraph Section)</span></span>

<span data-ttu-id="6dd32-104">Determina el espacio insertado después de cada párrafo en el bloque de texto de la forma, además del espacio que determinen la celda SpLine y, si se trata del último párrafo de un bloque de texto, la celda BottomMargin.</span><span class="sxs-lookup"><span data-stu-id="6dd32-104">Determines the amount of space inserted after each paragraph in the shape's text block, in addition to any space from the SpLine cell and, if it is the last paragraph in a text block, the BottomMargin cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6dd32-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6dd32-105">Remarks</span></span>

<span data-ttu-id="6dd32-p101">Este valor no depende de la escala del dibujo. Si se cambia la escala del dibujo, el espacio después del párrafo permanece igual.</span><span class="sxs-lookup"><span data-stu-id="6dd32-p101">This value is independent of the scale of the drawing. If the drawing is scaled, the Space After setting remains the same.</span></span>
  
<span data-ttu-id="6dd32-108">Para obtener una referencia a la celda SpAfter por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="6dd32-108">To get a reference to the SpAfter cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6dd32-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="6dd32-109">Cell name:</span></span>  <br/> | <span data-ttu-id="6dd32-110">Para.SpAfter[  *i*  ] donde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="6dd32-110">Para.SpAfter[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6dd32-111">Para obtener una referencia desde un programa a la celda SpAfter por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6dd32-111">To get a reference to the SpAfter cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6dd32-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="6dd32-112">Section index:</span></span>  <br/> |<span data-ttu-id="6dd32-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="6dd32-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="6dd32-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="6dd32-114">Row index:</span></span>  <br/> |<span data-ttu-id="6dd32-115">**visRowParagraph**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6dd32-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6dd32-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="6dd32-116">Cell index:</span></span>  <br/> |<span data-ttu-id="6dd32-117">**visSpaceAfter**</span><span class="sxs-lookup"><span data-stu-id="6dd32-117">**visSpaceAfter**</span></span> <br/> |
   

