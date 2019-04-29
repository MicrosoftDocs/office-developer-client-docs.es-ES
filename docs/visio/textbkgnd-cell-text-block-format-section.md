---
title: Celda TextBkgnd (Sección de formato del bloque de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251267
localization_priority: Normal
ms.assetid: a238bf1c-1acd-eacd-22f3-a48acaaa4549
description: Determina el color de fondo del texto de una forma.
ms.openlocfilehash: 2450bf0cb0e013c0f9310eacfca0f5a20e7e6063
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406545"
---
# <a name="textbkgnd-cell-text-block-format-section"></a><span data-ttu-id="6b9b4-103">Celda TextBkgnd (Sección de formato del bloque de texto)</span><span class="sxs-lookup"><span data-stu-id="6b9b4-103">TextBkgnd Cell (Text Block Format Section)</span></span>

<span data-ttu-id="6b9b4-104">Determina el color de fondo del texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="6b9b4-104">Determines the text background color for a shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6b9b4-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b9b4-105">Remarks</span></span>

<span data-ttu-id="6b9b4-106">La celda TextBkgnd puede tener cualquier valor entre 0 y 24, o 255.</span><span class="sxs-lookup"><span data-stu-id="6b9b4-106">The TextBkgnd cell can have any value from 0 through 24, or 255.</span></span> <span data-ttu-id="6b9b4-107">Los valores 0 y 255 ( *visTxtBlklOpaque*) indican un fondo de texto transparente.</span><span class="sxs-lookup"><span data-stu-id="6b9b4-107">The values 0 and 255 ( *visTxtBlklOpaque*) both indicate a transparent text background.</span></span> 
  
<span data-ttu-id="6b9b4-108">Para especificar un color personalizado, utilice la función RGB o HSL más uno; por ejemplo, RGB(255,127,255)+1.</span><span class="sxs-lookup"><span data-stu-id="6b9b4-108">To enter a custom color, use the RGB or HSL function plus one—for example, RGB(255,127,255)+1.</span></span> <span data-ttu-id="6b9b4-109">El valor de un color personalizado es su color RGB y RGB ( *r, g, b*) + 1, en lugar de un número, se mostrará en la ventana ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="6b9b4-109">The value of a custom color is its RGB color, and RGB( *r, g, b*)+1, rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="6b9b4-110">Cuando se utilizan en operaciones numéricas, los colores personalizados tienen valores iguales o mayores que 25.</span><span class="sxs-lookup"><span data-stu-id="6b9b4-110">When used in numeric operations, custom colors have values of 25 and above.</span></span> 
  
<span data-ttu-id="6b9b4-111">Puede establecer la transparencia del color de fondo del texto en la celda TextBkgndTrans.</span><span class="sxs-lookup"><span data-stu-id="6b9b4-111">You can set the transparency of the text background color in the TextBkgndTrans cell.</span></span>
  
<span data-ttu-id="6b9b4-112">Para obtener una referencia a la celda TextBkgnd por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="6b9b4-112">To get a reference to the TextBkgnd cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b9b4-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="6b9b4-113">Cell name:</span></span>  <br/> |<span data-ttu-id="6b9b4-114">TextBkgnd</span><span class="sxs-lookup"><span data-stu-id="6b9b4-114">TextBkgnd</span></span>  <br/> |
   
<span data-ttu-id="6b9b4-115">Para obtener una referencia desde un programa a la celda TextBkgnd por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6b9b4-115">To get a reference to the TextBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b9b4-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="6b9b4-116">Section index:</span></span>  <br/> |<span data-ttu-id="6b9b4-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6b9b4-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6b9b4-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="6b9b4-118">Row index:</span></span>  <br/> |<span data-ttu-id="6b9b4-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="6b9b4-119">**visRowText**</span></span> <br/> |
|<span data-ttu-id="6b9b4-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="6b9b4-120">Cell index:</span></span>  <br/> |<span data-ttu-id="6b9b4-121">**visTxtBlkBkgnd**</span><span class="sxs-lookup"><span data-stu-id="6b9b4-121">**visTxtBlkBkgnd**</span></span> <br/> |
   

