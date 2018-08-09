---
title: Celda BulletFont (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60023
localization_priority: Normal
ms.assetid: a75ff1f3-2f4d-89e3-108b-e16a34f5184f
description: Representa el número de la fuente empleada para dar formato al texto cuando se especifica una cadena de viñeta personalizada y el valor de la celda Bullet no es cero.
ms.openlocfilehash: 7cd3333afc30d30ea7b0e5d35650681074744235
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821704"
---
# <a name="bulletfont-cell-paragraph-section"></a><span data-ttu-id="84440-103">Celda BulletFont (sección Párrafo)</span><span class="sxs-lookup"><span data-stu-id="84440-103">BulletFont Cell (Paragraph Section)</span></span>

<span data-ttu-id="84440-104">Representa el número de la fuente empleada para dar formato al texto cuando se especifica una cadena de viñeta personalizada y el valor de la celda Bullet no es cero.</span><span class="sxs-lookup"><span data-stu-id="84440-104">Represents the number of the font used to format the text when a custom bullet string is specified and the value in the Bullet cell is non-zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="84440-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="84440-105">Remarks</span></span>

<span data-ttu-id="84440-p101">Los números de fuente varían según las fuentes instaladas en el sistema. Si el valor es 0 y hay una cadena de viñeta personalizada, la fuente utilizada será la misma que la del primer carácter del párrafo.</span><span class="sxs-lookup"><span data-stu-id="84440-p101">Font numbers vary according to the fonts installed on your system. If the value is 0 and there is a custom bullet string, the font used is the same as the font of the first character of the paragraph.</span></span>
  
<span data-ttu-id="84440-108">Para obtener una referencia a la celda BulletFont por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="84440-108">To get a reference to the BulletFont cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="84440-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="84440-109">Cell name:</span></span>  <br/> | <span data-ttu-id="84440-110">Para.BulletFont [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="84440-110">Para.BulletFont[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="84440-111">Para obtener una referencia desde un programa a la celda BulletFont por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="84440-111">To get a reference to the BulletFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="84440-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="84440-112">Section index:</span></span>  <br/> |<span data-ttu-id="84440-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="84440-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="84440-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="84440-114">Row index:</span></span>  <br/> |<span data-ttu-id="84440-115">**visRowParagraph** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="84440-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="84440-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="84440-116">Cell index:</span></span>  <br/> |<span data-ttu-id="84440-117">**visBulletFont**</span><span class="sxs-lookup"><span data-stu-id="84440-117">**visBulletFont**</span></span> <br/> |
   

