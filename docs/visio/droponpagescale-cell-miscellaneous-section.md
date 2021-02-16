---
title: Celda DropOnPageScale (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60042
localization_priority: Normal
ms.assetid: 8927f811-7d8e-ed54-9eec-b86a781168dd
ms.openlocfilehash: 17c597df3d9e7e741d902fd566cc9a5de1f31ea0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423765"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a><span data-ttu-id="c3a1a-102">Celda DropOnPageScale (Sección de varios)</span><span class="sxs-lookup"><span data-stu-id="c3a1a-102">DropOnPageScale Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="c3a1a-103">Contiene el porcentaje equivalente al cambio en la escala de la forma cuando se coloca en la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="c3a1a-103">Contains the percentage by which a shape is scaled when dropped on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c3a1a-104">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c3a1a-104">Remarks</span></span>

<span data-ttu-id="c3a1a-105">En los dos siguientes casos, Visio cambia la escala de las formas de modo que aparezcan de forma adecuada en la página de dibujo:</span><span class="sxs-lookup"><span data-stu-id="c3a1a-105">In the following two cases, Visio scales shapes so that they appear appropriately on the drawing page:</span></span>
  
- <span data-ttu-id="c3a1a-106">Cuando se colocan formas sin medir en dibujos a escala.</span><span class="sxs-lookup"><span data-stu-id="c3a1a-106">When unmeasured shapes are dropped onto scaled drawings.</span></span>
    
- <span data-ttu-id="c3a1a-107">Cuando las formas medidas se descartan en dibujos sin escala.</span><span class="sxs-lookup"><span data-stu-id="c3a1a-107">When measured shapes are dropped onto unscaled drawings.</span></span>
    
<span data-ttu-id="c3a1a-108">El porcentaje de la celda DropOnPageScale indica el factor por el que Visio escale la forma, ya sea hacia arriba ( \> 100) o hacia abajo ( \< 100).</span><span class="sxs-lookup"><span data-stu-id="c3a1a-108">The percentage in the DropOnPageScale cell indicates the factor by which Visio scaled the shape, either up (\>100) or down (\<100).</span></span> <span data-ttu-id="c3a1a-109">Esta cifra se puede usar como factor al calcular los valores que se encuentran en el código de software.</span><span class="sxs-lookup"><span data-stu-id="c3a1a-109">You can use this number as a factor when calculating hard-coded values.</span></span> 
  
<span data-ttu-id="c3a1a-110">El valor es el 100% para formas medidas en dibujos a escala y para formas sin medir en dibujos sin escala.</span><span class="sxs-lookup"><span data-stu-id="c3a1a-110">This value is 100% for measured shapes on scaled drawings or unmeasured shapes on unscaled drawings.</span></span> 
  
<span data-ttu-id="c3a1a-111">Para obtener una referencia a la celda DropOnPageScale por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="c3a1a-111">To get a reference to the DropOnPageScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c3a1a-112">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c3a1a-112">Cell name:</span></span>  <br/> | <span data-ttu-id="c3a1a-113">DropOnPageScale</span><span class="sxs-lookup"><span data-stu-id="c3a1a-113">DropOnPageScale</span></span>  <br/> |
   
<span data-ttu-id="c3a1a-114">Para obtener una referencia desde un programa a la celda DropOnPageScale por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c3a1a-114">To get a reference to the DropOnPageScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c3a1a-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c3a1a-115">Section index:</span></span>  <br/> |<span data-ttu-id="c3a1a-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c3a1a-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c3a1a-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c3a1a-117">Row index:</span></span>  <br/> |<span data-ttu-id="c3a1a-118">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="c3a1a-118">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="c3a1a-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c3a1a-119">Cell index:</span></span>  <br/> |<span data-ttu-id="c3a1a-120">**visObjDropOnPageScale**</span><span class="sxs-lookup"><span data-stu-id="c3a1a-120">**visObjDropOnPageScale**</span></span> <br/> |
   

