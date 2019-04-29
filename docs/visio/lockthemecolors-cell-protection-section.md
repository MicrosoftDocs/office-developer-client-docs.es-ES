---
title: Celda LockThemeColors (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm70001
localization_priority: Normal
ms.assetid: 22cedeb3-58b5-3932-9252-5c9dd3e163e3
ms.openlocfilehash: 81091ea33be2158435d240ba14f3c97e8f3fcc39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436849"
---
# <a name="lockthemecolors-cell-protection-section"></a><span data-ttu-id="1368d-102">Celda LockThemeColors (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="1368d-102">LockThemeColors Cell (Protection Section)</span></span>

<span data-ttu-id="1368d-103">Impide la aplicación de los colores del tema a la forma.</span><span class="sxs-lookup"><span data-stu-id="1368d-103">Prevents application of theme colors to the shape.</span></span> 
  
<span data-ttu-id="1368d-104">El valor de la celda LockThemeColors corresponde a configuración de la casilla de verificación **Contra colores del tema** del cuadro de diálogo **Protección**.</span><span class="sxs-lookup"><span data-stu-id="1368d-104">The value of the LockThemeColors cell corresponds to the **From theme colors** check box setting in the **Protection** dialog box.</span></span> 
  
<span data-ttu-id="1368d-105">Para hacer referencia a la celda LockThemeColors por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:

</span><span class="sxs-lookup"><span data-stu-id="1368d-105">To refer to the LockThemeColors cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1368d-106">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="1368d-106">Cell name:</span></span>  <br/> |<span data-ttu-id="1368d-107">LockThemeColors</span><span class="sxs-lookup"><span data-stu-id="1368d-107">LockThemeColors</span></span>  <br/> |
   
<span data-ttu-id="1368d-108">Para hacer referencia desde un programa a la celda LockThemeColors según su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1368d-108">To refer to the LockThemeColors cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1368d-109">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="1368d-109">Section index:</span></span>  <br/> |<span data-ttu-id="1368d-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1368d-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1368d-111">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="1368d-111">Row index:</span></span>  <br/> |<span data-ttu-id="1368d-112">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="1368d-112">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="1368d-113">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="1368d-113">Cell index:</span></span>  <br/> |<span data-ttu-id="1368d-114">**visLockThemeColors**</span><span class="sxs-lookup"><span data-stu-id="1368d-114">**visLockThemeColors**</span></span> <br/> |
   

