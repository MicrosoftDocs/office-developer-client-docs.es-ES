---
title: Celda ComplexScriptFont (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60034
localization_priority: Normal
ms.assetid: e1cf9e97-101b-384f-65fe-0169c89dfccc
description: Contiene el número de la fuente empleada para dar formato a un texto compuesto por caracteres de un alfabeto complejo. Los números de fuente varían según las fuentes instaladas en el sistema.
ms.openlocfilehash: 5ec8deb59b875a01592b6d7b652204089ecf11e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404837"
---
# <a name="complexscriptfont-cell-character-section"></a><span data-ttu-id="8e2d9-104">Celda ComplexScriptFont (Sección de caracteres)</span><span class="sxs-lookup"><span data-stu-id="8e2d9-104">ComplexScriptFont Cell (Character Section)</span></span>

<span data-ttu-id="8e2d9-p102">Contiene el número de la fuente empleada para dar formato a un texto compuesto por caracteres de un alfabeto complejo. Los números de fuente varían según las fuentes instaladas en el sistema.</span><span class="sxs-lookup"><span data-stu-id="8e2d9-p102">Contains the number of the font used to format text composed of complex script characters. Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8e2d9-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8e2d9-107">Remarks</span></span>

<span data-ttu-id="8e2d9-108">Los tamaños de fuente de alfabetos complejos aparecen en la ficha **fuente** del cuadro de diálogo **texto** (haga clic en la flecha del grupo **fuente** en la ficha **Inicio** ).</span><span class="sxs-lookup"><span data-stu-id="8e2d9-108">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="8e2d9-109">Esta lista aparece solo si agregó un idioma que contiene caracteres de script complejos o asiáticos en el cuadro de diálogo **Preferencias de idioma de Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="8e2d9-109">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="8e2d9-110">(Haga clic en **Inicio**, **Todos los programas**, **Microsoft Office**, **Herramientas de Microsoft Office** y, a continuación, en **Preferencias de idioma de Microsoft Office**).</span><span class="sxs-lookup"><span data-stu-id="8e2d9-110">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="8e2d9-111">El número cero (0) indica que no hay ninguna fuente especificada.</span><span class="sxs-lookup"><span data-stu-id="8e2d9-111">The number 0 (zero) means no font is specified.</span></span> <span data-ttu-id="8e2d9-112">Se usará la fuente Latin o fuentes predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="8e2d9-112">The Latin font or default fonts are used.</span></span>
  
<span data-ttu-id="8e2d9-113">Para obtener una referencia a la celda ComplexScriptFont por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="8e2d9-113">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e2d9-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="8e2d9-114">Cell name:</span></span>  <br/> |<span data-ttu-id="8e2d9-115">Char. ComplexScriptFont [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="8e2d9-115">Char.ComplexScriptFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8e2d9-116">Para obtener una referencia desde un programa a la celda ComplexScriptFont por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="8e2d9-116">To get a reference to the ComplexScriptFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e2d9-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="8e2d9-117">Section index:</span></span>  <br/> |<span data-ttu-id="8e2d9-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="8e2d9-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="8e2d9-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="8e2d9-119">Row index:</span></span>  <br/> |<span data-ttu-id="8e2d9-120">**visRowCharacter** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8e2d9-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="8e2d9-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="8e2d9-121">Cell index:</span></span>  <br/> |<span data-ttu-id="8e2d9-122">**visCharacterComplexScriptFont**</span><span class="sxs-lookup"><span data-stu-id="8e2d9-122">**visCharacterComplexScriptFont**</span></span> <br/> |
   

