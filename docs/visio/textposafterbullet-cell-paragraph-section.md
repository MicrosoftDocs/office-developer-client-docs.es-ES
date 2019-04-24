---
title: Celda TextPosAfterBullet (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60089
localization_priority: Normal
ms.assetid: 08958abb-9d66-5a83-dac3-4cbfd1f6d85e
description: Representa la distancia entra la primera línea del párrafo y la viñeta.
ms.openlocfilehash: a98967cb5f9541434745c3b3d6afafde0878074a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332291"
---
# <a name="textposafterbullet-cell-paragraph-section"></a><span data-ttu-id="bc73c-103">Celda TextPosAfterBullet (Sección de párrafo)</span><span class="sxs-lookup"><span data-stu-id="bc73c-103">TextPosAfterBullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="bc73c-104">Representa la distancia entra la primera línea del párrafo y la viñeta.</span><span class="sxs-lookup"><span data-stu-id="bc73c-104">Represents the distance between the first line of the paragraph and the bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bc73c-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bc73c-105">Remarks</span></span>

<span data-ttu-id="bc73c-p101">Esta distancia se suma a la contenida en la celda IndFirst, que es la sangría izquierda predeterminada. Este valor no depende de la escala de dibujo.</span><span class="sxs-lookup"><span data-stu-id="bc73c-p101">This distance is added to the distance contained in the IndFirst cell, which is the default left indent. This value is independent of the scale of the drawing.</span></span> 
  
<span data-ttu-id="bc73c-108">Para obtener una referencia a la celda TextPosAfterBullet por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="bc73c-108">To get a reference to the TextPosAfterBullet cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bc73c-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="bc73c-109">Cell name:</span></span>  <br/> | <span data-ttu-id="bc73c-110">Para. TextPosAfterBullet [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="bc73c-110">Para.TextPosAfterBullet[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="bc73c-111">Para obtener una referencia desde un programa a la celda TextPosAfterBullet por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="bc73c-111">To get a reference to the TextPosAfterBullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bc73c-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="bc73c-112">Section index:</span></span>  <br/> |<span data-ttu-id="bc73c-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="bc73c-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="bc73c-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="bc73c-114">Row index:</span></span>  <br/> |<span data-ttu-id="bc73c-115">**visRowParagraph** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bc73c-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bc73c-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="bc73c-116">Cell index:</span></span>  <br/> |<span data-ttu-id="bc73c-117">**visTextPosAfterBullet**</span><span class="sxs-lookup"><span data-stu-id="bc73c-117">**visTextPosAfterBullet**</span></span> <br/> |
   

