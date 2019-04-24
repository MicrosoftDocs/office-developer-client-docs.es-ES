---
title: Celda Color (Sección de revisor)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60032
localization_priority: Normal
ms.assetid: c1e3d7bf-e6b6-65f1-ae40-80c8ba4821cd
description: Valor RGB que representa el color asignado a la marca de revisión de un documento.
ms.openlocfilehash: d9df6605ca6c8a22353978b9483989ecfc08130d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341821"
---
# <a name="color-cell-reviewer-section"></a><span data-ttu-id="d87fa-103">Celda Color (Sección de revisor)</span><span class="sxs-lookup"><span data-stu-id="d87fa-103">Color Cell (Reviewer Section)</span></span>

<span data-ttu-id="d87fa-104">Valor RGB que representa el color asignado a la marca de revisión de un documento.</span><span class="sxs-lookup"><span data-stu-id="d87fa-104">An RGB value that represents the color assigned to a document reviewer's markup.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d87fa-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d87fa-105">Remarks</span></span>

<span data-ttu-id="d87fa-p101">Los colores se asignan a los revisores en la siguiente secuencia: rojo, azul, verde, violeta, naranja, turquesa y gris. Cuando acaba la secuencia, se vuelve a empezar desde el principio, según vayan agregándose revisores al proceso.</span><span class="sxs-lookup"><span data-stu-id="d87fa-p101">Colors are assigned to reviewers in the following sequence: red, blue, green, violet, orange, turquoise, gray. These colors are cycled through again for any remaining reviewers.</span></span> 
  
<span data-ttu-id="d87fa-108">Los comentarios incluidos en la página de dibujo original siempre aparecen en amarillo, independientemente del color asignado al revisor en la celda Color.</span><span class="sxs-lookup"><span data-stu-id="d87fa-108">Comments entered on the original drawing page are always colored yellow, regardless of the color assigned to a reviewer in the Color cell.</span></span> 
  
<span data-ttu-id="d87fa-109">Para obtener una referencia a la celda Color por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="d87fa-109">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d87fa-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="d87fa-110">Cell name:</span></span>  <br/> | <span data-ttu-id="d87fa-111">Reviewer. color [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d87fa-111">Reviewer.Color [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d87fa-112">Para obtener una referencia desde un programa a la celda Color por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d87fa-112">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d87fa-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="d87fa-113">Section index:</span></span>  <br/> |<span data-ttu-id="d87fa-114">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="d87fa-114">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="d87fa-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="d87fa-115">Row index:</span></span>  <br/> |<span data-ttu-id="d87fa-116">**visRowReviewer** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d87fa-116">**visRowReviewer** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d87fa-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="d87fa-117">Cell index:</span></span>  <br/> |<span data-ttu-id="d87fa-118">**visReviewerColor**</span><span class="sxs-lookup"><span data-stu-id="d87fa-118">**visReviewerColor**</span></span> <br/> |
   

