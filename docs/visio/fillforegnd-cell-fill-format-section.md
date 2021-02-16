---
title: Celda FillForegnd (Sección de formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251241
localization_priority: Normal
ms.assetid: 7548a480-4dce-45e0-281b-f6f8bdf05c0b
description: Determina el color utilizado para el primer plano (trazo) de la trama de relleno de la forma.
ms.openlocfilehash: 352fecf8d99069cfb5ebd72d295284dc03446364
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415568"
---
# <a name="fillforegnd-cell-fill-format-section"></a><span data-ttu-id="02ef2-103">Celda FillForegnd (Sección de formato de relleno)</span><span class="sxs-lookup"><span data-stu-id="02ef2-103">FillForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="02ef2-104">Determina el color utilizado para el primer plano (trazo) de la trama de relleno de la forma.</span><span class="sxs-lookup"><span data-stu-id="02ef2-104">Determines the color used for the foreground (stroke) of the shape's fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="02ef2-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="02ef2-105">Remarks</span></span>

<span data-ttu-id="02ef2-106">Para establecer el color, escriba un número entre el 0 y el 23.</span><span class="sxs-lookup"><span data-stu-id="02ef2-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="02ef2-107">Para especificar un color personalizado, utilice la función RGB o HSL.</span><span class="sxs-lookup"><span data-stu-id="02ef2-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="02ef2-108">El valor de un color personalizado es su color RGB y RGB( *r, g, b*), en lugar de un número, se mostrará en la ventana ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="02ef2-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="02ef2-109">Cuando se utilizan en operaciones numéricas, los colores personalizados tienen valores iguales o mayores que 24.</span><span class="sxs-lookup"><span data-stu-id="02ef2-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="02ef2-110">Puede establecer la transparencia del relleno de primer plano en la celda FillForegndTrans.</span><span class="sxs-lookup"><span data-stu-id="02ef2-110">You can set the transparency of the foreground fill in the FillForegndTrans cell.</span></span>
  
<span data-ttu-id="02ef2-111">Para obtener una referencia a la celda FillForegnd por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="02ef2-111">To get a reference to the FillForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02ef2-112">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="02ef2-112">Cell name:</span></span>  <br/> |<span data-ttu-id="02ef2-113">FillForegnd</span><span class="sxs-lookup"><span data-stu-id="02ef2-113">FillForegnd</span></span>  <br/> |
   
<span data-ttu-id="02ef2-114">Para obtener una referencia desde un programa a la celda FillForegnd por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="02ef2-114">To get a reference to the FillForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02ef2-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="02ef2-115">Section index:</span></span>  <br/> |<span data-ttu-id="02ef2-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="02ef2-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="02ef2-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="02ef2-117">Row index:</span></span>  <br/> |<span data-ttu-id="02ef2-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="02ef2-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="02ef2-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="02ef2-119">Cell index:</span></span>  <br/> |<span data-ttu-id="02ef2-120">**visFillForegnd**</span><span class="sxs-lookup"><span data-stu-id="02ef2-120">**visFillForegnd**</span></span> <br/> |
   

