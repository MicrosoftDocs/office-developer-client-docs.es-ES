---
title: Celda LockFromGroupFormat (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 3daeb4704a33ba836cf82c9ab3517c6ca6be8db7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426061"
---
# <a name="lockfromgroupformat-cell-protection-section"></a><span data-ttu-id="3fe4f-102">Celda LockFromGroupFormat (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="3fe4f-102">LockFromGroupFormat Cell (Protection Section)</span></span>

<span data-ttu-id="3fe4f-103">Bloquea los cambios de formato realizados en una forma de grupo para que no se propaguen a sus subformas, a la vez que permiten a los usuarios dar formato directo a las subformas seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-103">Blocks format changes to a group shape from being propagated to its sub-shapes, while still allowing users to format selected sub-shapes directly.</span></span> 
  
<span data-ttu-id="3fe4f-104">El valor de la celda LockFromGroupFormat corresponde a configuración de la casilla de verificación **Contra formato en grupo** del cuadro de diálogo **Protección**.</span><span class="sxs-lookup"><span data-stu-id="3fe4f-104">The value of the LockFromGroupFormat cell corresponds to the **From group formatting** check box setting in the **Protection** dialog box.</span></span> 
  
<span data-ttu-id="3fe4f-105">Para hacer referencia a la celda LockFromGroupFormat por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:

</span><span class="sxs-lookup"><span data-stu-id="3fe4f-105">To refer to the LockFromGroupFormat cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3fe4f-106">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="3fe4f-106">Cell name:</span></span>  <br/> |<span data-ttu-id="3fe4f-107">LockFromGroupFormat</span><span class="sxs-lookup"><span data-stu-id="3fe4f-107">LockFromGroupFormat</span></span>  <br/> |
   
<span data-ttu-id="3fe4f-108">Para hacer referencia desde un programa a la celda LockFromGroupFormat según su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3fe4f-108">To refer to the LockFromGroupFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3fe4f-109">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="3fe4f-109">Section index:</span></span>  <br/> |<span data-ttu-id="3fe4f-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3fe4f-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3fe4f-111">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="3fe4f-111">Row index:</span></span>  <br/> |<span data-ttu-id="3fe4f-112">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="3fe4f-112">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="3fe4f-113">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="3fe4f-113">Cell index:</span></span>  <br/> |<span data-ttu-id="3fe4f-114">**visLockFromGroupFormat**</span><span class="sxs-lookup"><span data-stu-id="3fe4f-114">**visLockFromGroupFormat**</span></span> <br/> |
   
<span data-ttu-id="3fe4f-115">El valor predeterminado de la celda es 0 (False).</span><span class="sxs-lookup"><span data-stu-id="3fe4f-115">The default value for the cell is 0 (False).</span></span>
  

