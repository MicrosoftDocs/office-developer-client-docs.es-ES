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
ms.openlocfilehash: 4867ab57fa59b3a5e76598108fbb92b9bbab7913
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821816"
---
# <a name="complexscriptsize-cell-character-section"></a><span data-ttu-id="9c023-103">Celda ComplexScriptSize (sección Caracteres)</span><span class="sxs-lookup"><span data-stu-id="9c023-103">ComplexScriptSize Cell (Character Section)</span></span>

<span data-ttu-id="9c023-104">Tamaño de la fuente empleada para dar formato a un texto compuesto por caracteres de un alfabeto complejo.</span><span class="sxs-lookup"><span data-stu-id="9c023-104">The size of the font used to format text composed of complex script characters.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9c023-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c023-105">Remarks</span></span>

<span data-ttu-id="9c023-106">Los tamaños de fuente de alfabetos complejos aparecen en la ficha **fuente** en el cuadro de diálogo **texto** (haga clic en la flecha situada en la **fuente** de grupo en la ficha **Inicio** ).</span><span class="sxs-lookup"><span data-stu-id="9c023-106">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="9c023-107">Esta lista aparece sólo si se ha agregado un idioma que contiene caracteres asiáticos o con alfabetos complejos, en el cuadro de diálogo **Preferencias de idioma de Microsoft Office** .</span><span class="sxs-lookup"><span data-stu-id="9c023-107">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="9c023-108">(Haga clic en **Inicio**, haga clic en **Todos los programas**, haga clic en **Microsoft Office**, haga clic en **Herramientas de Microsoft Office**y, a continuación, haga clic en **Preferencias de idioma de Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="9c023-108">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="9c023-p102">Puede especificar este valor como un tamaño explícito o como un porcentaje. Si especifica un porcentaje, el valor se basará en el valor de la celda Size. El valor predeterminado 0 (cero) indica el 100%.</span><span class="sxs-lookup"><span data-stu-id="9c023-p102">You can enter this value as an explicit point size or as a percentage. If you specify a percentage, the value is based on the value in the Size cell. A default value of 0 (zero) means 100%.</span></span> 
  
<span data-ttu-id="9c023-112">Para obtener una referencia a la celda ComplexScriptFont por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="9c023-112">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c023-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="9c023-113">Cell name:</span></span>  <br/> |<span data-ttu-id="9c023-114">Char.ComplexScriptSize [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="9c023-114">Char.ComplexScriptSize[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="9c023-115">Para obtener una referencia desde un programa a la celda ComplexScriptSize por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9c023-115">To get a reference to the ComplexScriptSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c023-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="9c023-116">Section index:</span></span>  <br/> |<span data-ttu-id="9c023-117">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="9c023-117">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="9c023-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="9c023-118">Row index:</span></span>  <br/> |<span data-ttu-id="9c023-119">**visRowCharacter** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9c023-119">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="9c023-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="9c023-120">Cell index:</span></span>  <br/> |<span data-ttu-id="9c023-121">**visCharacterComplexScriptSize**</span><span class="sxs-lookup"><span data-stu-id="9c023-121">**visCharacterComplexScriptSize**</span></span> <br/> |
   

