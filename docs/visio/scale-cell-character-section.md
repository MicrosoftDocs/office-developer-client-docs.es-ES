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
ms.openlocfilehash: 60e896772ddd1d59e1a1da7f2c0e90893658c624
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429155"
---
# <a name="scale-cell-character-section"></a><span data-ttu-id="e72f0-104">Celda Scale (Sección de caracteres)</span><span class="sxs-lookup"><span data-stu-id="e72f0-104">Scale Cell (Character Section)</span></span>

<span data-ttu-id="e72f0-105">Controla el ancho de la fuente.</span><span class="sxs-lookup"><span data-stu-id="e72f0-105">Controls the font width.</span></span> <span data-ttu-id="e72f0-106">El valor predeterminado de esta celda es 100%.</span><span class="sxs-lookup"><span data-stu-id="e72f0-106">The default value for this cell is 100%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e72f0-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e72f0-107">Remarks</span></span>

<span data-ttu-id="e72f0-p103">Establezca un porcentaje entre 1% y 99% para disminuir el ancho de la fuente. Establezca un porcentaje entre 101% y 600% para aumentar el ancho de la fuente.</span><span class="sxs-lookup"><span data-stu-id="e72f0-p103">Set the percentage between 1% and 99% to decrease the font width. Set it between 101% and 600% to increase the font width.</span></span>
  
<span data-ttu-id="e72f0-110">También puede usar el cuadro de diálogo **Texto** para establecer el valor de esta celda (en la ficha **Inicio**, haga clic en la flecha de **Fuente**).</span><span class="sxs-lookup"><span data-stu-id="e72f0-110">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="e72f0-111">Para obtener una referencia a la celda Scale por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="e72f0-111">To get a reference to the Scale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e72f0-112">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="e72f0-112">Cell name:</span></span>  <br/> |<span data-ttu-id="e72f0-113">Char.FontScale[ *i*  ] donde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e72f0-113">Char.FontScale[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e72f0-114">Para obtener una referencia desde un programa a la celda Scale por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e72f0-114">To get a reference to the Scale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e72f0-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="e72f0-115">Section index:</span></span>  <br/> |<span data-ttu-id="e72f0-116">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="e72f0-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="e72f0-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="e72f0-117">Row index:</span></span>  <br/> |<span data-ttu-id="e72f0-118">**visRowCharacter**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e72f0-118">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="e72f0-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="e72f0-119">Cell index:</span></span>  <br/> |<span data-ttu-id="e72f0-120">**visCharacterFontScale**</span><span class="sxs-lookup"><span data-stu-id="e72f0-120">**visCharacterFontScale**</span></span> <br/> |
   

