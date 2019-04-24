---
title: Celda BulletSize (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033780
localization_priority: Normal
ms.assetid: 6ff5d07b-17e2-f6ca-1860-5d498a9ebf06
description: Especifica el tamaño de una viñeta.
ms.openlocfilehash: 8671bc6f5ec40814b13727bc458f74eb2893f839
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337614"
---
# <a name="bulletsize-cell-paragraph-section"></a><span data-ttu-id="72c60-103">Celda BulletSize (Sección de párrafo)</span><span class="sxs-lookup"><span data-stu-id="72c60-103">BulletSize Cell (Paragraph Section)</span></span>

<span data-ttu-id="72c60-104">Especifica el tamaño de una viñeta.</span><span class="sxs-lookup"><span data-stu-id="72c60-104">Specifies the size of a bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="72c60-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="72c60-105">Remarks</span></span>

<span data-ttu-id="72c60-106">Este valor se puede especificar para viñetas predefinidas o personalizadas y como porcentaje o un valor concreto.</span><span class="sxs-lookup"><span data-stu-id="72c60-106">This value can be specified for either predefined or custom bullets, as either a percentage or a specific value.</span></span> 
  
<span data-ttu-id="72c60-107">Si el valor es cero (0), la viñeta es el mismo tamaño de fuente que el del primer carácter del párrafo.</span><span class="sxs-lookup"><span data-stu-id="72c60-107">If the value is zero (0), the bullet is the same font size as that of the first character in the paragraph.</span></span> <span data-ttu-id="72c60-108">Si el valor se expresa mediante un porcentaje, el tamaño de la viñeta será un porcentaje del tamaño de la fuente del primer carácter del párrafo.</span><span class="sxs-lookup"><span data-stu-id="72c60-108">If the value is a percentage, the bullet is sized as a percentage of the font size of the first character in the paragraph.</span></span> <span data-ttu-id="72c60-109">Los números negativos se tratan como porcentajes.</span><span class="sxs-lookup"><span data-stu-id="72c60-109">Negative numbers are treated as percentages.</span></span>
  
<span data-ttu-id="72c60-110">Para obtener una referencia a la celda BulletSize por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="72c60-110">To get a reference to the BulletSize cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="72c60-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="72c60-111">Cell name:</span></span>  <br/> | <span data-ttu-id="72c60-112">Para. BulletFontSize [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="72c60-112">Para.BulletFontSize[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="72c60-113">Para obtener una referencia desde un programa a la celda BulletSize por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="72c60-113">To get a reference to the BulletSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="72c60-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="72c60-114">Section index:</span></span>  <br/> |<span data-ttu-id="72c60-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="72c60-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="72c60-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="72c60-116">Row index:</span></span>  <br/> |<span data-ttu-id="72c60-117">**visRowParagraph** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="72c60-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="72c60-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="72c60-118">Cell index:</span></span>  <br/> |<span data-ttu-id="72c60-119">**visBulletFontSize**</span><span class="sxs-lookup"><span data-stu-id="72c60-119">**visBulletFontSize**</span></span> <br/> |
   

