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
ms.openlocfilehash: ddca3697dfcf1f422efacbe395c18f1a6b8ac48c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411508"
---
# <a name="initials-cell-reviewer-section"></a><span data-ttu-id="7b0f8-103">Celda Initials (Sección de revisor)</span><span class="sxs-lookup"><span data-stu-id="7b0f8-103">Initials Cell (Reviewer Section)</span></span>

<span data-ttu-id="7b0f8-104">Contiene las iniciales del revisor de un documento.</span><span class="sxs-lookup"><span data-stu-id="7b0f8-104">Contains the initials of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7b0f8-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7b0f8-105">Remarks</span></span>

<span data-ttu-id="7b0f8-106">Este valor tiene como valor  predeterminado las iniciales del cuadro Iniciales de  la ficha  **General** del cuadro de diálogo Opciones de **Visio** (haga clic en la ficha Archivo, en Opciones y, a continuación, en **General).**</span><span class="sxs-lookup"><span data-stu-id="7b0f8-106">This value defaults to the initials in the **Initials** box on the **General** tab in the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General** ).</span></span> 
  
<span data-ttu-id="7b0f8-107">Para obtener una referencia a la celda Initials por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="7b0f8-107">To get a reference to the Initials cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7b0f8-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="7b0f8-108">Cell name:</span></span>  <br/> | <span data-ttu-id="7b0f8-109">Reviewer.Initials [  *i*  ] donde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7b0f8-109">Reviewer.Initials [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7b0f8-110">Para obtener una referencia a la celda Initials por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7b0f8-110">To get a reference to the Initials cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7b0f8-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="7b0f8-111">Section index:</span></span>  <br/> |<span data-ttu-id="7b0f8-112">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="7b0f8-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="7b0f8-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="7b0f8-113">Row index:</span></span>  <br/> |<span data-ttu-id="7b0f8-114">**visRowReviewer**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7b0f8-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7b0f8-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="7b0f8-115">Cell index:</span></span>  <br/> |<span data-ttu-id="7b0f8-116">**visReviewerInitials**</span><span class="sxs-lookup"><span data-stu-id="7b0f8-116">**visReviewerInitials**</span></span> <br/> |
   

