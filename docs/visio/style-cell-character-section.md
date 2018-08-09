---
title: Celda Style (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251249
localization_priority: Normal
ms.assetid: 4372f1e1-f0a9-2f63-ff79-58f2afdceed5
description: Muestra el formato de caracteres que se aplica a un intervalo de texto en el bloque de texto de la forma.
ms.openlocfilehash: 48bda5eb798f439e2616b2b910d7ec5ac719d060
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823323"
---
# <a name="style-cell-character-section"></a><span data-ttu-id="a083b-103">Celda Style (sección Caracteres)</span><span class="sxs-lookup"><span data-stu-id="a083b-103">Style Cell (Character Section)</span></span>

<span data-ttu-id="a083b-104">Muestra el formato de caracteres que se aplica a un intervalo de texto en el bloque de texto de la forma.</span><span class="sxs-lookup"><span data-stu-id="a083b-104">Shows the character formatting applied to a range of text in the shape's text block.</span></span>
  
|<span data-ttu-id="a083b-105">**Estilo**</span><span class="sxs-lookup"><span data-stu-id="a083b-105">**Style**</span></span>|<span data-ttu-id="a083b-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a083b-106">**Value**</span></span>|<span data-ttu-id="a083b-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="a083b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="a083b-108">Negrita</span><span class="sxs-lookup"><span data-stu-id="a083b-108">Bold</span></span>  <br/> | <span data-ttu-id="a083b-109">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="a083b-109">&amp;H1</span></span>  <br/> |<span data-ttu-id="a083b-110">**visBold**</span><span class="sxs-lookup"><span data-stu-id="a083b-110">**visBold**</span></span> <br/> |
| <span data-ttu-id="a083b-111">Cursiva</span><span class="sxs-lookup"><span data-stu-id="a083b-111">Italic</span></span>  <br/> | <span data-ttu-id="a083b-112">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="a083b-112">&amp;H2</span></span>  <br/> |<span data-ttu-id="a083b-113">**visItalic**</span><span class="sxs-lookup"><span data-stu-id="a083b-113">**visItalic**</span></span> <br/> |
| <span data-ttu-id="a083b-114">Subrayado</span><span class="sxs-lookup"><span data-stu-id="a083b-114">Underline</span></span>  <br/> | <span data-ttu-id="a083b-115">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="a083b-115">&amp;H4</span></span>  <br/> |<span data-ttu-id="a083b-116">**visUnderLine**</span><span class="sxs-lookup"><span data-stu-id="a083b-116">**visUnderLine**</span></span> <br/> |
| <span data-ttu-id="a083b-117">Versalitas</span><span class="sxs-lookup"><span data-stu-id="a083b-117">Small caps</span></span>  <br/> | <span data-ttu-id="a083b-118">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="a083b-118">&amp;H8</span></span>  <br/> |<span data-ttu-id="a083b-119">**visSmallCaps**</span><span class="sxs-lookup"><span data-stu-id="a083b-119">**visSmallCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a083b-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a083b-120">Remarks</span></span>

<span data-ttu-id="a083b-p101">La celda Style contiene la información de formato que se aplica a un subconjunto del texto de la forma si la sección de caracteres contiene varias filas. En caso contrario, contiene información de formato para todo el texto de la forma.</span><span class="sxs-lookup"><span data-stu-id="a083b-p101">The Style cell contains formatting information applied to a sub-range of a shape's text if the Characters section contains multiple rows. Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="a083b-123">El valor representa un número binario en el que cada bit indica un estilo de carácter.</span><span class="sxs-lookup"><span data-stu-id="a083b-123">The value represents a binary number in which each bit indicates a character style.</span></span> <span data-ttu-id="a083b-124">Por ejemplo, un valor de 3 representa texto en formato de negrita y cursiva.</span><span class="sxs-lookup"><span data-stu-id="a083b-124">For example, a value of 3 represents text formatted in both italic and bold.</span></span> <span data-ttu-id="a083b-125">Si el valor de estilo es 0, el texto es texto sin formato o sin formato.</span><span class="sxs-lookup"><span data-stu-id="a083b-125">If the value of Style is 0, the text is plain, or unformatted.</span></span> <span data-ttu-id="a083b-126">Puede probar para un formato determinado con bits booleano\* funciones.</span><span class="sxs-lookup"><span data-stu-id="a083b-126">You can test for a particular format using Boolean BIT\* functions.</span></span> <span data-ttu-id="a083b-127">Vea la documentación de programación para obtener más información acerca de estas funciones.</span><span class="sxs-lookup"><span data-stu-id="a083b-127">See your programming documentation for details about these functions.</span></span>
  
<span data-ttu-id="a083b-128">Para obtener una referencia a la celda Style por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="a083b-128">To get a reference to the Style cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a083b-129">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="a083b-129">Cell name:</span></span>  <br/> | <span data-ttu-id="a083b-130">Char.Style [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="a083b-130">Char.Style[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a083b-131">Para obtener una referencia desde un programa a la celda Style por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a083b-131">To get a reference to the Style cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a083b-132">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="a083b-132">Section index:</span></span>  <br/> |<span data-ttu-id="a083b-133">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="a083b-133">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="a083b-134">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="a083b-134">Row index:</span></span>  <br/> |<span data-ttu-id="a083b-135">**visRowCharacter** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a083b-135">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a083b-136">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="a083b-136">Cell index:</span></span>  <br/> |<span data-ttu-id="a083b-137">**visCharacterStyle**</span><span class="sxs-lookup"><span data-stu-id="a083b-137">**visCharacterStyle**</span></span> <br/> |
   
 <span data-ttu-id="a083b-138">*Ejemplo*</span><span class="sxs-lookup"><span data-stu-id="a083b-138">*Example*</span></span> 
  
<span data-ttu-id="a083b-139">Suponga que en la celda Color de la primera fila de la sección de caracteres se establece la fórmula siguiente:</span><span class="sxs-lookup"><span data-stu-id="a083b-139">Suppose the Color cell in the first row of a shape's Character section is set to this formula:</span></span>
  
<span data-ttu-id="a083b-140">= IF(BITAND(Char.Style,1)=1,4,3)</span><span class="sxs-lookup"><span data-stu-id="a083b-140">= IF(BITAND(Char.Style,1)=1,4,3)</span></span>
  
<span data-ttu-id="a083b-p103">Entonces, si el primer carácter del texto de la forma está en negrita, el texto cubierto por la primera fila de propiedades de Character será azul (4); en caso contrario será verde (3). En este ejemplo se supone que se utilizan los colores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="a083b-p103">Then if the first character of the shape's text is bold, the text covered by the first Character properties row will be blue (4); otherwise it will be green (3). This example assumes default colors are in effect.</span></span>
  
<span data-ttu-id="a083b-p104">En el siguiente ejemplo se establece la celda Style en un programa. La primera instrucción hace referencia a la celda Style por su nombre, y la segunda por su índice. Ambas instrucciones ponen en cursiva el texto cubierto por la segunda fila de la sección de caracteres de una forma.</span><span class="sxs-lookup"><span data-stu-id="a083b-p104">The following is an example of setting the Style cell in a program. The first statement references the Style cell by name, and the second statement references the Style cell by index. Both statements apply italic to the text covered by the second row of a shape's Character section.</span></span>
  

