---
title: Celda Size (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251252
localization_priority: Normal
ms.assetid: a61b50fe-eacb-b3d4-0e4e-ab3e7c972ee9
description: Determina el tamaño del texto del bloque de texto de la forma.
ms.openlocfilehash: f3077441844b859cf224eccc8180d0d56cce851f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823251"
---
# <a name="size-cell-character-section"></a><span data-ttu-id="04285-103">Celda Size (sección Caracteres)</span><span class="sxs-lookup"><span data-stu-id="04285-103">Size Cell (Character Section)</span></span>

<span data-ttu-id="04285-104">Determina el tamaño del texto del bloque de texto de la forma.</span><span class="sxs-lookup"><span data-stu-id="04285-104">Determines the size of the text in the shape's text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="04285-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="04285-105">Remarks</span></span>

<span data-ttu-id="04285-p101">El tamaño del texto no depende de la escala del dibujo. Si se cambia la escala del dibujo, el tamaño del texto permanece igual.</span><span class="sxs-lookup"><span data-stu-id="04285-p101">The text's size is independent of the scale of the drawing. If the drawing is scaled, the text size remains the same.</span></span>
  
<span data-ttu-id="04285-108">Para obtener una referencia a la celda Size por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="04285-108">To get a reference to the Size cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="04285-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="04285-109">Cell name:</span></span>  <br/> | <span data-ttu-id="04285-110">Char.Size [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="04285-110">Char.Size[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="04285-111">Para obtener una referencia desde un programa a la celda Size por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="04285-111">To get a reference to the Size cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="04285-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="04285-112">Section index:</span></span>  <br/> |<span data-ttu-id="04285-113">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="04285-113">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="04285-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="04285-114">Row index:</span></span>  <br/> |<span data-ttu-id="04285-115">**visRowCharacter** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="04285-115">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="04285-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="04285-116">Cell index:</span></span>  <br/> |<span data-ttu-id="04285-117">**visCharacterSize**</span><span class="sxs-lookup"><span data-stu-id="04285-117">**visCharacterSize**</span></span> <br/> |
   

