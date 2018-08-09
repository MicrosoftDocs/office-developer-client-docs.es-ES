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
ms.openlocfilehash: ef07f4165882e08a2292e4ee549f8807fe8403e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821761"
---
# <a name="color-cell-character-section"></a><span data-ttu-id="112b3-103">Celda Color (sección Caracteres)</span><span class="sxs-lookup"><span data-stu-id="112b3-103">Color Cell (Character Section)</span></span>

<span data-ttu-id="112b3-104">Determina el color utilizado para el texto de la forma.</span><span class="sxs-lookup"><span data-stu-id="112b3-104">Determines the color used for the shape's text.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="112b3-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="112b3-105">Remarks</span></span>

<span data-ttu-id="112b3-106">Para establecer el color, escriba un número entre el 0 y el 23.</span><span class="sxs-lookup"><span data-stu-id="112b3-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="112b3-107">Para especificar un color personalizado, utilice la función RGB o HSL.</span><span class="sxs-lookup"><span data-stu-id="112b3-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="112b3-108">El valor de un color personalizado es su color RGB y RGB ( *r, g, b*), en lugar de un número, se mostrarán en la ventana ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="112b3-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="112b3-109">Cuando se usa en operaciones numéricas, los colores personalizados tienen valores de 24 y superior.</span><span class="sxs-lookup"><span data-stu-id="112b3-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="112b3-110">Puede establecer la transparencia del color del texto en la celda Transparency.</span><span class="sxs-lookup"><span data-stu-id="112b3-110">You can set the transparency of the text color in the Transparency cell.</span></span>
  
<span data-ttu-id="112b3-111">Para obtener una referencia a la celda Color por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="112b3-111">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="112b3-112">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="112b3-112">Cell name:</span></span>  <br/> |<span data-ttu-id="112b3-113">Char.Color [ *i* ] donde *i* = < 1 >, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="112b3-113">Char.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="112b3-114">Para obtener una referencia desde un programa a la celda Color por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="112b3-114">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="112b3-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="112b3-115">Section index:</span></span>  <br/> |<span data-ttu-id="112b3-116">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="112b3-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="112b3-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="112b3-117">Row index:</span></span>  <br/> |<span data-ttu-id="112b3-118">**visRowCharacter** +  *i* donde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="112b3-118">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="112b3-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="112b3-119">Cell index:</span></span>  <br/> |<span data-ttu-id="112b3-120">**visCharacterColor**</span><span class="sxs-lookup"><span data-stu-id="112b3-120">**visCharacterColor**</span></span> <br/> |
   

