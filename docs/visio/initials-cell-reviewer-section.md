---
title: Celda Initials (Sección de revisor)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60045
localization_priority: Normal
ms.assetid: 8f5d34f0-4c4b-5265-83c1-5b86b73d464f
description: Contiene las iniciales del revisor de un documento.
ms.openlocfilehash: 65f0082219c8d6adca55af86c027b2ec5642fb5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822350"
---
# <a name="initials-cell-reviewer-section"></a><span data-ttu-id="9ef0d-103">Celda Initials (sección Revisor)</span><span class="sxs-lookup"><span data-stu-id="9ef0d-103">Initials Cell (Reviewer Section)</span></span>

<span data-ttu-id="9ef0d-104">Contiene las iniciales del revisor de un documento.</span><span class="sxs-lookup"><span data-stu-id="9ef0d-104">Contains the initials of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9ef0d-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ef0d-105">Remarks</span></span>

<span data-ttu-id="9ef0d-106">El valor predeterminado es las iniciales en el cuadro **iniciales** de la ficha **General** en el cuadro de diálogo **Opciones de Visio** (haga clic en la pestaña **archivo** , haga clic en **Opciones**y, a continuación, haga clic en **General** ).</span><span class="sxs-lookup"><span data-stu-id="9ef0d-106">This value defaults to the initials in the **Initials** box on the **General** tab in the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General** ).</span></span> 
  
<span data-ttu-id="9ef0d-107">Para obtener una referencia a la celda Initials por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="9ef0d-107">To get a reference to the Initials cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9ef0d-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="9ef0d-108">Cell name:</span></span>  <br/> | <span data-ttu-id="9ef0d-109">Reviewer.Initials [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="9ef0d-109">Reviewer.Initials [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="9ef0d-110">Para obtener una referencia a la celda Initials por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9ef0d-110">To get a reference to the Initials cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9ef0d-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="9ef0d-111">Section index:</span></span>  <br/> |<span data-ttu-id="9ef0d-112">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="9ef0d-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="9ef0d-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="9ef0d-113">Row index:</span></span>  <br/> |<span data-ttu-id="9ef0d-114">**visRowReviewer** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9ef0d-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9ef0d-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="9ef0d-115">Cell index:</span></span>  <br/> |<span data-ttu-id="9ef0d-116">**visReviewerInitials**</span><span class="sxs-lookup"><span data-stu-id="9ef0d-116">**visReviewerInitials**</span></span> <br/> |
   

