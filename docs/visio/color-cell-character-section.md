---
title: Celda Color (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm160
localization_priority: Normal
ms.assetid: 1c9aab2e-6c2f-0684-4e66-c35ac71883d6
description: Determina el color utilizado para el texto de la forma.
ms.openlocfilehash: a27d957781ca9a784e7ab9d5c1ce4f533b9a55ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341842"
---
# <a name="color-cell-character-section"></a><span data-ttu-id="b068b-103">Celda Color (Sección de caracteres)</span><span class="sxs-lookup"><span data-stu-id="b068b-103">Color Cell (Character Section)</span></span>

<span data-ttu-id="b068b-104">Determina el color utilizado para el texto de la forma.</span><span class="sxs-lookup"><span data-stu-id="b068b-104">Determines the color used for the shape's text.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b068b-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b068b-105">Remarks</span></span>

<span data-ttu-id="b068b-106">Para establecer el color, escriba un número entre el 0 y el 23.</span><span class="sxs-lookup"><span data-stu-id="b068b-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="b068b-107">Para especificar un color personalizado, utilice la función RGB o HSL.</span><span class="sxs-lookup"><span data-stu-id="b068b-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="b068b-108">El valor de un color personalizado es su color RGB y RGB ( *r, g, b*), en lugar de un número, se mostrará en la ventana ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="b068b-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="b068b-109">Cuando se utilizan en operaciones numéricas, los colores personalizados tienen valores iguales o mayores que 24.</span><span class="sxs-lookup"><span data-stu-id="b068b-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="b068b-110">Puede establecer la transparencia del color del texto en la celda Transparency.</span><span class="sxs-lookup"><span data-stu-id="b068b-110">You can set the transparency of the text color in the Transparency cell.</span></span>
  
<span data-ttu-id="b068b-111">Para obtener una referencia a la celda Color por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="b068b-111">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b068b-112">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b068b-112">Cell name:</span></span>  <br/> |<span data-ttu-id="b068b-113">Char. color [ *i* ] donde *i* = <1>, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="b068b-113">Char.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="b068b-114">Para obtener una referencia desde un programa a la celda Color por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b068b-114">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b068b-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b068b-115">Section index:</span></span>  <br/> |<span data-ttu-id="b068b-116">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="b068b-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="b068b-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b068b-117">Row index:</span></span>  <br/> |<span data-ttu-id="b068b-118">**visRowCharacter** +  *i* donde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="b068b-118">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="b068b-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b068b-119">Cell index:</span></span>  <br/> |<span data-ttu-id="b068b-120">**visCharacterColor**</span><span class="sxs-lookup"><span data-stu-id="b068b-120">**visCharacterColor**</span></span> <br/> |
   

