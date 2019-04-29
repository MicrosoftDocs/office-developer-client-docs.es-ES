---
title: Celda Name (Sección del revisor)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030992
localization_priority: Normal
ms.assetid: be39cd0b-56bf-a070-f5d8-c9a440d81ee2
description: Contiene el nombre del revisor de un documento.
ms.openlocfilehash: 02f353ab8f2d39cc075211bb13157b93081e9d8f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417689"
---
# <a name="name-cell-reviewer-section"></a><span data-ttu-id="4e11a-103">Celda Name (Sección del revisor)</span><span class="sxs-lookup"><span data-stu-id="4e11a-103">Name Cell (Reviewer Section)</span></span>

<span data-ttu-id="4e11a-104">Contiene el nombre del revisor de un documento.</span><span class="sxs-lookup"><span data-stu-id="4e11a-104">Contains the name of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4e11a-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4e11a-105">Remarks</span></span>

 <span data-ttu-id="4e11a-106">El valor predeterminado es el nombre que se encuentra en el cuadro **nombre de usuario** de la ficha **General** del cuadro de diálogo **Opciones de Visio** (haga clic en la pestaña **archivo** , haga clic en **Opciones**y, a continuación, haga clic en **General**).</span><span class="sxs-lookup"><span data-stu-id="4e11a-106">This value defaults to the name found in the **User name** box on the **General** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General**).</span></span> 
  
<span data-ttu-id="4e11a-107">Para obtener una referencia a la celda name por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="4e11a-107">To get a reference to the Name cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4e11a-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="4e11a-108">Cell name:</span></span>  <br/> | <span data-ttu-id="4e11a-109">Reviewer.Name [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="4e11a-109">Reviewer.Name [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="4e11a-110">Para obtener una referencia desde un programa a la celda Name por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4e11a-110">To get a reference to the Name cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4e11a-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="4e11a-111">Section index:</span></span>  <br/> |<span data-ttu-id="4e11a-112">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="4e11a-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="4e11a-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="4e11a-113">Row index:</span></span>  <br/> |<span data-ttu-id="4e11a-114">**visRowReviewer** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4e11a-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4e11a-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="4e11a-115">Cell index:</span></span>  <br/> |<span data-ttu-id="4e11a-116">**visReviewerName**</span><span class="sxs-lookup"><span data-stu-id="4e11a-116">**visReviewerName**</span></span> <br/> |
   

