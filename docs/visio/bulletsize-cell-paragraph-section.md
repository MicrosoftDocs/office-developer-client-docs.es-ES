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
ms.openlocfilehash: e1b6bd1b4535a70bf99b9cd90af3e0d52128da01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821676"
---
# <a name="bulletsize-cell-paragraph-section"></a><span data-ttu-id="8d1a6-103">Celda BulletSize (sección Párrafo)</span><span class="sxs-lookup"><span data-stu-id="8d1a6-103">BulletSize Cell (Paragraph Section)</span></span>

<span data-ttu-id="8d1a6-104">Especifica el tamaño de una viñeta.</span><span class="sxs-lookup"><span data-stu-id="8d1a6-104">Specifies the size of a bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8d1a6-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8d1a6-105">Remarks</span></span>

<span data-ttu-id="8d1a6-106">Este valor se puede especificar para viñetas predefinidas o personalizadas y como porcentaje o un valor concreto.</span><span class="sxs-lookup"><span data-stu-id="8d1a6-106">This value can be specified for either predefined or custom bullets, as either a percentage or a specific value.</span></span> 
  
<span data-ttu-id="8d1a6-107">Si el valor es cero (0), la viñeta tiene el mismo tamaño de fuente que la del primer carácter del párrafo.</span><span class="sxs-lookup"><span data-stu-id="8d1a6-107">If the value is zero (0), the bullet is the same font size as that of the first character in the paragraph.</span></span> <span data-ttu-id="8d1a6-108">Si el valor es un porcentaje, la viñeta se mide como un porcentaje del tamaño de fuente del primer carácter del párrafo.</span><span class="sxs-lookup"><span data-stu-id="8d1a6-108">If the value is a percentage, the bullet is sized as a percentage of the font size of the first character in the paragraph.</span></span> <span data-ttu-id="8d1a6-109">Los números negativos se tratan como porcentajes.</span><span class="sxs-lookup"><span data-stu-id="8d1a6-109">Negative numbers are treated as percentages.</span></span>
  
<span data-ttu-id="8d1a6-110">Para obtener una referencia a la celda BulletSize por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="8d1a6-110">To get a reference to the BulletSize cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8d1a6-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="8d1a6-111">Cell name:</span></span>  <br/> | <span data-ttu-id="8d1a6-112">Para.BulletFontSize [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="8d1a6-112">Para.BulletFontSize[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8d1a6-113">Para obtener una referencia desde un programa a la celda BulletSize por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="8d1a6-113">To get a reference to the BulletSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8d1a6-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="8d1a6-114">Section index:</span></span>  <br/> |<span data-ttu-id="8d1a6-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="8d1a6-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="8d1a6-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="8d1a6-116">Row index:</span></span>  <br/> |<span data-ttu-id="8d1a6-117">**visRowParagraph** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8d1a6-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8d1a6-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="8d1a6-118">Cell index:</span></span>  <br/> |<span data-ttu-id="8d1a6-119">**visBulletFontSize**</span><span class="sxs-lookup"><span data-stu-id="8d1a6-119">**visBulletFontSize**</span></span> <br/> |
   

