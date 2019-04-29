---
title: Celda Spacing (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm955
localization_priority: Normal
ms.assetid: 46feb136-01ac-1303-66ab-d772c0ec41a0
description: Controla el espacio que hay entre dos o más caracteres. El espacio puede aumentar o disminuir en incrementos de 1/20 de punto.
ms.openlocfilehash: 927b6203b81af453411cdd13b6f8c8342507a61b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430066"
---
# <a name="spacing-cell-character-section"></a><span data-ttu-id="0ab09-104">Celda Spacing (Sección de caracteres)</span><span class="sxs-lookup"><span data-stu-id="0ab09-104">Spacing Cell (Character Section)</span></span>

<span data-ttu-id="0ab09-105">Controla el espacio que hay entre dos o más caracteres.</span><span class="sxs-lookup"><span data-stu-id="0ab09-105">Controls the amount of space between two or more characters.</span></span> <span data-ttu-id="0ab09-106">El espacio puede aumentar o disminuir en incrementos de 1/20 de punto.</span><span class="sxs-lookup"><span data-stu-id="0ab09-106">Space can be added or subtracted in 1/20th point increments.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0ab09-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0ab09-107">Remarks</span></span>

<span data-ttu-id="0ab09-108">También puede usar el cuadro de diálogo **Texto** para establecer el valor de esta celda (en la ficha **Inicio**, haga clic en la flecha de **Fuente**).</span><span class="sxs-lookup"><span data-stu-id="0ab09-108">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="0ab09-109">Para obtener una referencia a la celda Spacing por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="0ab09-109">To get a reference to the Spacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ab09-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="0ab09-110">Cell name:</span></span>  <br/> |<span data-ttu-id="0ab09-111">Char. Letterspace [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0ab09-111">Char.Letterspace[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0ab09-112">Para obtener una referencia desde un programa a la celda Spacing por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="0ab09-112">To get a reference to the Spacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ab09-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="0ab09-113">Section index:</span></span>  <br/> |<span data-ttu-id="0ab09-114">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="0ab09-114">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="0ab09-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="0ab09-115">Row index:</span></span>  <br/> |<span data-ttu-id="0ab09-116">**visRowCharacter** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0ab09-116">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="0ab09-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="0ab09-117">Cell index:</span></span>  <br/> |<span data-ttu-id="0ab09-118">**visCharacterLetterspace**</span><span class="sxs-lookup"><span data-stu-id="0ab09-118">**visCharacterLetterspace**</span></span> <br/> |
   

