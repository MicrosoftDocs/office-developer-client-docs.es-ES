---
title: Celda ComplexScriptSize (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033768
localization_priority: Normal
ms.assetid: f58687d7-2ba4-ff77-0bcc-3106867d89de
description: Tamaño de la fuente empleada para dar formato a un texto compuesto por caracteres de un alfabeto complejo.
ms.openlocfilehash: 38b01c4a0142c7eca2923ee9b13963eaa1a62830
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359354"
---
# <a name="complexscriptsize-cell-character-section"></a><span data-ttu-id="d2fd0-103">Celda ComplexScriptSize (Sección de caracteres)</span><span class="sxs-lookup"><span data-stu-id="d2fd0-103">ComplexScriptSize Cell (Character Section)</span></span>

<span data-ttu-id="d2fd0-104">Tamaño de la fuente empleada para dar formato a un texto compuesto por caracteres de un alfabeto complejo.</span><span class="sxs-lookup"><span data-stu-id="d2fd0-104">The size of the font used to format text composed of complex script characters.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d2fd0-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d2fd0-105">Remarks</span></span>

<span data-ttu-id="d2fd0-106">Los tamaños de fuente de alfabetos complejos aparecen en la ficha **fuente** del cuadro de diálogo **texto** (haga clic en la flecha del grupo **fuente** en la ficha **Inicio** ).</span><span class="sxs-lookup"><span data-stu-id="d2fd0-106">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="d2fd0-107">Esta lista aparece solo si agregó un idioma que contiene caracteres de script complejos o asiáticos en el cuadro de diálogo **Preferencias de idioma de Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="d2fd0-107">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="d2fd0-108">(Haga clic en **Inicio**, **Todos los programas**, **Microsoft Office**, **Herramientas de Microsoft Office** y, a continuación, en **Preferencias de idioma de Microsoft Office**).</span><span class="sxs-lookup"><span data-stu-id="d2fd0-108">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="d2fd0-p102">Puede especificar este valor como un tamaño explícito o como un porcentaje. Si especifica un porcentaje, el valor se basará en el valor de la celda Size. El valor predeterminado 0 (cero) indica el 100%.</span><span class="sxs-lookup"><span data-stu-id="d2fd0-p102">You can enter this value as an explicit point size or as a percentage. If you specify a percentage, the value is based on the value in the Size cell. A default value of 0 (zero) means 100%.</span></span> 
  
<span data-ttu-id="d2fd0-112">Para obtener una referencia a la celda ComplexScriptFont por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="d2fd0-112">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2fd0-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="d2fd0-113">Cell name:</span></span>  <br/> |<span data-ttu-id="d2fd0-114">Char. ComplexScriptSize [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d2fd0-114">Char.ComplexScriptSize[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d2fd0-115">Para obtener una referencia desde un programa a la celda ComplexScriptSize por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d2fd0-115">To get a reference to the ComplexScriptSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2fd0-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="d2fd0-116">Section index:</span></span>  <br/> |<span data-ttu-id="d2fd0-117">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="d2fd0-117">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="d2fd0-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="d2fd0-118">Row index:</span></span>  <br/> |<span data-ttu-id="d2fd0-119">**visRowCharacter** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d2fd0-119">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="d2fd0-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="d2fd0-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d2fd0-121">**visCharacterComplexScriptSize**</span><span class="sxs-lookup"><span data-stu-id="d2fd0-121">**visCharacterComplexScriptSize**</span></span> <br/> |
   

