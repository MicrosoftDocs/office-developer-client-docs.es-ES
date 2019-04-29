---
title: Celda DoubleULine (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm260
localization_priority: Normal
ms.assetid: c18955c8-d653-c29d-d3da-9d3cd0241e17
description: Determina si el intervalo de texto tiene doble subrayado.
ms.openlocfilehash: 2708e7f55e1fd04d5fb902b3d382035790cbbcc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438844"
---
# <a name="doubleuline-cell-character-section"></a><span data-ttu-id="f941b-103">Celda DoubleULine (Sección de caracteres)</span><span class="sxs-lookup"><span data-stu-id="f941b-103">DoubleULine Cell (Character Section)</span></span>

<span data-ttu-id="f941b-104">Determina si el intervalo de texto tiene doble subrayado.</span><span class="sxs-lookup"><span data-stu-id="f941b-104">Determines whether the range of text has a double underline below it.</span></span>
  
|<span data-ttu-id="f941b-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f941b-105">**Value**</span></span>|<span data-ttu-id="f941b-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f941b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f941b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f941b-107">TRUE</span></span>  <br/> |<span data-ttu-id="f941b-108">El texto tiene doble subrayado.</span><span class="sxs-lookup"><span data-stu-id="f941b-108">Text has a double underline below it.</span></span>  <br/> |
|<span data-ttu-id="f941b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f941b-109">FALSE</span></span>  <br/> |<span data-ttu-id="f941b-110">El texto no tiene doble subrayado.</span><span class="sxs-lookup"><span data-stu-id="f941b-110">Text does not have a double underline below it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f941b-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f941b-111">Remarks</span></span>

<span data-ttu-id="f941b-p101">La celda DoubleULine contiene la información de formato que se aplica a un subintervalo del texto de una forma si la sección de caracteres contiene varias filas. En caso contrario, contiene información de formato para todo el texto de la forma.</span><span class="sxs-lookup"><span data-stu-id="f941b-p101">The DoubleULine cell contains formatting information applied to a sub-range of a shape's text if the Characters section contains multiple rows. Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="f941b-114">También puede usar el cuadro de diálogo **Texto** para establecer el valor de esta celda (haga clic en la flecha de **Fuente** en la ficha **Inicio**).</span><span class="sxs-lookup"><span data-stu-id="f941b-114">You can also set the value of this cell by using the **Text** dialog box (click the **Font** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="f941b-115">Para obtener una referencia a la celda DoubleULine por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="f941b-115">To get a reference to the DoubleULine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f941b-116">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="f941b-116">Cell name:</span></span>  <br/> |<span data-ttu-id="f941b-117">Char. DblUnderline [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="f941b-117">Char.DblUnderline[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f941b-118">Para obtener una referencia desde un programa a la celda DoubleULine por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f941b-118">To get a reference to the DoubleULine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f941b-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="f941b-119">Section index:</span></span>  <br/> |<span data-ttu-id="f941b-120">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="f941b-120">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="f941b-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="f941b-121">Row index:</span></span>  <br/> |<span data-ttu-id="f941b-122">**visRowCharacter** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f941b-122">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="f941b-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="f941b-123">Cell index:</span></span>  <br/> |<span data-ttu-id="f941b-124">**visCharacterDblUnderline**</span><span class="sxs-lookup"><span data-stu-id="f941b-124">**visCharacterDblUnderline**</span></span> <br/> |
   

