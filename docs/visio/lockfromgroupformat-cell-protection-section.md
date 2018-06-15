---
title: Celda LockFromGroupFormat (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 95633ab7a4127564fef65062bcf328d4364ebd86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19822522"
---
# <a name="lockfromgroupformat-cell-protection-section"></a><span data-ttu-id="427fd-102">Celda LockFromGroupFormat (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="427fd-102">LockFromGroupFormat Cell (Protection Section)</span></span>

<span data-ttu-id="427fd-103">Bloques de cambios de formato a una forma de grupo de que se propaga a sus subformas, mientras permite a los usuarios dar formato a las subformas seleccionadas directamente.</span><span class="sxs-lookup"><span data-stu-id="427fd-103">Blocks format changes to a group shape from being propagated to its sub-shapes, while still allowing users to format selected sub-shapes directly.</span></span> 
  
<span data-ttu-id="427fd-104">El valor de la celda LockFromGroupFormat corresponde a la opción de casilla de verificación **contra formato en grupo** en el cuadro de diálogo **protección** .</span><span class="sxs-lookup"><span data-stu-id="427fd-104">The value of the LockFromGroupFormat cell corresponds to the **From group formatting** check box setting in the **Protection** dialog box.</span></span> 
  
<span data-ttu-id="427fd-105">Para hacer referencia a la celda LockFromGroupFormat por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="427fd-105">To refer to the LockFromGroupFormat cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="427fd-106">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="427fd-106">Cell name:</span></span>  <br/> |<span data-ttu-id="427fd-107">LockFromGroupFormat</span><span class="sxs-lookup"><span data-stu-id="427fd-107">LockFromGroupFormat</span></span>  <br/> |
   
<span data-ttu-id="427fd-108">Para hacer referencia a la celda LockFromGroupFormat por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="427fd-108">To refer to the LockFromGroupFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="427fd-109">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="427fd-109">Section index:</span></span>  <br/> |<span data-ttu-id="427fd-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="427fd-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="427fd-111">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="427fd-111">Row index:</span></span>  <br/> |<span data-ttu-id="427fd-112">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="427fd-112">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="427fd-113">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="427fd-113">Cell index:</span></span>  <br/> |<span data-ttu-id="427fd-114">**visLockFromGroupFormat**</span><span class="sxs-lookup"><span data-stu-id="427fd-114">**visLockFromGroupFormat**</span></span> <br/> |
   
<span data-ttu-id="427fd-115">El valor predeterminado de la celda es 0 (False).</span><span class="sxs-lookup"><span data-stu-id="427fd-115">The default value for the cell is 0 (False).</span></span>
  

