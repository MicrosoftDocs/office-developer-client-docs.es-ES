---
title: Celda BulletString (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm135
localization_priority: Normal
ms.assetid: 38285824-30ad-0cf2-07cb-0103ab3a415a
description: Permite crear un estilo de viñeta personalizado.
ms.openlocfilehash: b7a1d7f845c7b9945670240361a4ac66efa80786
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337565"
---
# <a name="bulletstring-cell-paragraph-section"></a><span data-ttu-id="a547d-103">Celda BulletString (Sección de párrafo)</span><span class="sxs-lookup"><span data-stu-id="a547d-103">BulletString Cell (Paragraph Section)</span></span>

<span data-ttu-id="a547d-104">Permite crear un estilo de viñeta personalizado.</span><span class="sxs-lookup"><span data-stu-id="a547d-104">Allows you to create a custom bullet style.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a547d-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a547d-105">Remarks</span></span>

<span data-ttu-id="a547d-p101">Especifique el estilo como una cadena (entre comillas). Por ejemplo, podría escribir la cadena "ooo".</span><span class="sxs-lookup"><span data-stu-id="a547d-p101">Enter the style as a string (within quotation marks). For example, you could enter the string, "ooo."</span></span>
  
<span data-ttu-id="a547d-108">Asimismo, para establecer el valor de esta celda, haga clic con el botón secundario en una forma, elija **Formato**, haga clic en **Texto** y, a continuación, haga clic en la pestaña **Viñetas**.</span><span class="sxs-lookup"><span data-stu-id="a547d-108">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="a547d-109">Para obtener una referencia a la celda BulletString por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="a547d-109">To get a reference to the BulletString cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a547d-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="a547d-110">Cell name:</span></span>  <br/> |<span data-ttu-id="a547d-111">Para. BulletStr [ *i* ] donde *i* = <1>, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="a547d-111">Para.BulletStr[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="a547d-112">Para obtener una referencia desde un programa a la celda BulletString por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a547d-112">To get a reference to the BulletString cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a547d-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="a547d-113">Section index:</span></span>  <br/> |<span data-ttu-id="a547d-114">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="a547d-114">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="a547d-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="a547d-115">Row index:</span></span>  <br/> |<span data-ttu-id="a547d-116">**visRowParagraph** +  *i* donde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="a547d-116">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="a547d-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="a547d-117">Cell index:</span></span>  <br/> |<span data-ttu-id="a547d-118">**visBulletString**</span><span class="sxs-lookup"><span data-stu-id="a547d-118">**visBulletString**</span></span> <br/> |
   

