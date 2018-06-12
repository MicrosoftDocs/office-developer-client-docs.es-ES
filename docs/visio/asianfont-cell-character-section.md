---
title: Celda AsianFont (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033764
localization_priority: Normal
ms.assetid: 45bfaaaa-52cc-f8b4-68e7-8b99e5788ce1
description: Contiene el número de la fuente empleada para dar formato al texto con caracteres de lenguas asiáticas. Los números de fuente varían según las fuentes instaladas en el sistema.
ms.openlocfilehash: 1fbaa0b27a0c639519c302129142dcefe5708115
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821532"
---
# <a name="asianfont-cell-character-section"></a><span data-ttu-id="50425-104">Celda AsianFont (Sección de caracteres)</span><span class="sxs-lookup"><span data-stu-id="50425-104">AsianFont Cell (Character Section)</span></span>

<span data-ttu-id="50425-p102">Contiene el número de la fuente empleada para dar formato al texto con caracteres de lenguas asiáticas. Los números de fuente varían según las fuentes instaladas en el sistema.</span><span class="sxs-lookup"><span data-stu-id="50425-p102">Contains the number of the font used to format the text containing Asian characters. Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="50425-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50425-107">Remarks</span></span>

<span data-ttu-id="50425-108">Las fuentes asiáticas aparecen en la ficha **fuente** en el cuadro de diálogo **texto** (haga clic en la flecha situada en la **fuente** de grupo en la ficha **Inicio** ).</span><span class="sxs-lookup"><span data-stu-id="50425-108">Asian fonts are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="50425-109">Esta lista aparece sólo si se ha agregado un idioma que contiene caracteres asiáticos o con alfabetos complejos, en el cuadro de diálogo **Preferencias de idioma de Microsoft Office** .</span><span class="sxs-lookup"><span data-stu-id="50425-109">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="50425-110">(Haga clic en **Inicio**, haga clic en **Todos los programas**, haga clic en **Microsoft Office**, haga clic en **Herramientas de Microsoft Office**y, a continuación, haga clic en **Preferencias de idioma de Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="50425-110">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="50425-p104">El número cero indica que no hay ninguna fuente especificada. Se usará la fuente Latin o fuentes predeterminadas si contienen los caracteres necesarios.</span><span class="sxs-lookup"><span data-stu-id="50425-p104">The number 0 means no font is specified. The Latin font or default fonts are used if they contain the necessary characters.</span></span>
  
<span data-ttu-id="50425-113">Para obtener una referencia a la celda AsianFont por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="50425-113">To get a reference to the AsianFont cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50425-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="50425-114">Cell name:</span></span>  <br/> |<span data-ttu-id="50425-115">Char.AsianFont [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="50425-115">Char.AsianFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="50425-116">Para obtener una referencia a la celda AsianFont por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="50425-116">To get a reference to the AsianFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50425-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="50425-117">Section index:</span></span>  <br/> |<span data-ttu-id="50425-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="50425-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="50425-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="50425-119">Row index:</span></span>  <br/> |<span data-ttu-id="50425-120">**visRowCharacter** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="50425-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="50425-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="50425-121">Cell index:</span></span>  <br/> |<span data-ttu-id="50425-122">**visCharacterAsianFont**</span><span class="sxs-lookup"><span data-stu-id="50425-122">**visCharacterAsianFont**</span></span> <br/> |
   

