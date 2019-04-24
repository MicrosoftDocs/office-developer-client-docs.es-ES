---
title: Celda Format (Sección de campos de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm400
localization_priority: Normal
ms.assetid: ab937a00-84c2-6c1c-9080-b7c95ead4f63
description: Especifica el formato del campo de texto como una cadena, un número, una fecha u hora, una duración o una moneda.
ms.openlocfilehash: c1c7fc7e9c699b7642369fbb979c005829b06cb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346021"
---
# <a name="format-cell-text-fields-section"></a><span data-ttu-id="b2fbf-103">Celda Format (Sección de campos de texto)</span><span class="sxs-lookup"><span data-stu-id="b2fbf-103">Format Cell (Text Fields Section)</span></span>

<span data-ttu-id="b2fbf-104">Especifica el formato del campo de texto como una cadena, un número, una fecha u hora, una duración o una moneda.</span><span class="sxs-lookup"><span data-stu-id="b2fbf-104">Specifies the formatting of a text field that is a string, a number, a date or time, a duration, or a currency.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b2fbf-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b2fbf-105">Remarks</span></span>

<span data-ttu-id="b2fbf-p101">Si el valor de la celda Type es 0, 2, 5, 6 o 7 (cadena, número, fecha u hora, duración o moneda, respectivamente), especifique el formato de imagen adecuado para el tipo de datos. Por ejemplo, la imagen de formato "# #/4 UU" muestra el número 12,43 pulgadas como 12 2/4 PULGADAS. Para obtener más información sobre cómo especificar una imagen de formato, vea [Imágenes de formato](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="b2fbf-p101">If the value of the Type cell is 0, 2, 5, 6, or 7 (string, number, date or time, duration, or currency, respectively), specify a format picture appropriate for the data type. For example, the format picture "# #/4 UU" formats the number 12.43 in. as 12 2/4 INCHES. For more information about specifying a format picture, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="b2fbf-p102">Un número (Type = 2) puede representar una dimensión, un escalar, un ángulo, una fecha, una hora o una moneda. Para asegurar que el número de entrada sea siempre tratado como una fecha, hora o moneda, utilice la función DATETIME o CY en la celda Format en lugar de un formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="b2fbf-p102">A number (Type = 2) can represent a dimension, scalar, angle, date, time, or currency. To ensure that an input number is always evaluated as a date, time, or currency, use the DATETIME or CY function in the Format cell instead of a format picture.</span></span>
  
<span data-ttu-id="b2fbf-112">Para obtener una referencia a la celda Format por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="b2fbf-112">To get a reference to the Format cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b2fbf-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b2fbf-113">Cell name:</span></span>  <br/> | <span data-ttu-id="b2fbf-114">Fields. Format [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b2fbf-114">Fields.Format[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b2fbf-115">Para obtener una referencia a la celda Format por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b2fbf-115">To get a reference to the Format cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b2fbf-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b2fbf-116">Section index:</span></span>  <br/> |<span data-ttu-id="b2fbf-117">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="b2fbf-117">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="b2fbf-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b2fbf-118">Row index:</span></span>  <br/> |<span data-ttu-id="b2fbf-119">**visRowField** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b2fbf-119">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b2fbf-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b2fbf-120">Cell index:</span></span>  <br/> |<span data-ttu-id="b2fbf-121">**visFieldFormat**</span><span class="sxs-lookup"><span data-stu-id="b2fbf-121">**visFieldFormat**</span></span> <br/> |
   

