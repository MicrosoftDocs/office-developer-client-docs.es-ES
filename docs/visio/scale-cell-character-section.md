---
title: Celda Scale (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm870
localization_priority: Normal
ms.assetid: d6fe2574-b719-f38e-b1f1-592a812f1682
description: Controla el ancho de la fuente. El valor predeterminado de esta celda es 100%.
ms.openlocfilehash: fedbc0aec23320d03ca358f34babda56eaab31e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823102"
---
# <a name="scale-cell-character-section"></a><span data-ttu-id="5a537-104">Celda Scale (Sección de caracteres)</span><span class="sxs-lookup"><span data-stu-id="5a537-104">Scale Cell (Character Section)</span></span>

<span data-ttu-id="5a537-p102">Controla el ancho de la fuente. El valor predeterminado de esta celda es 100%.</span><span class="sxs-lookup"><span data-stu-id="5a537-p102">Controls the font width. The default value for this cell is 100%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5a537-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a537-107">Remarks</span></span>

<span data-ttu-id="5a537-p103">Establezca un porcentaje entre 1% y 99% para disminuir el ancho de la fuente. Establezca un porcentaje entre 101% y 600% para aumentar el ancho de la fuente.</span><span class="sxs-lookup"><span data-stu-id="5a537-p103">Set the percentage between 1% and 99% to decrease the font width. Set it between 101% and 600% to increase the font width.</span></span>
  
<span data-ttu-id="5a537-110">También puede establecer el valor de esta celda mediante el cuadro de diálogo **texto** (en la ficha **Inicio** , haga clic en la flecha de **fuente** ).</span><span class="sxs-lookup"><span data-stu-id="5a537-110">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="5a537-111">Para obtener una referencia a la celda Scale por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="5a537-111">To get a reference to the Scale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a537-112">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="5a537-112">Cell name:</span></span>  <br/> |<span data-ttu-id="5a537-113">Char.FontScale [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="5a537-113">Char.FontScale[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5a537-114">Para obtener una referencia a la celda Scale por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5a537-114">To get a reference to the Scale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a537-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="5a537-115">Section index:</span></span>  <br/> |<span data-ttu-id="5a537-116">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="5a537-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="5a537-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="5a537-117">Row index:</span></span>  <br/> |<span data-ttu-id="5a537-118">**visRowCharacter** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5a537-118">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="5a537-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="5a537-119">Cell index:</span></span>  <br/> |<span data-ttu-id="5a537-120">**visCharacterFontScale**</span><span class="sxs-lookup"><span data-stu-id="5a537-120">**visCharacterFontScale**</span></span> <br/> |
   

