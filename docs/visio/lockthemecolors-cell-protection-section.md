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
ms.openlocfilehash: 2ca8af2c7a41259af73a111af331ce1031e5f46c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19822529"
---
# <a name="lockthemecolors-cell-protection-section"></a><span data-ttu-id="323b9-102">Celda LockThemeColors (sección Protección)</span><span class="sxs-lookup"><span data-stu-id="323b9-102">LockThemeColors Cell (Protection Section)</span></span>

<span data-ttu-id="323b9-103">Impide la aplicación de colores del tema a la forma.</span><span class="sxs-lookup"><span data-stu-id="323b9-103">Prevents application of theme colors to the shape.</span></span> 
  
<span data-ttu-id="323b9-104">El valor de la celda LockThemeColors corresponde a configuración de la casilla de verificación **Contra colores del tema** del cuadro de diálogo **Protección**.</span><span class="sxs-lookup"><span data-stu-id="323b9-104">The value of the LockThemeColors cell corresponds to the **From theme colors** check box setting in the **Protection** dialog box.</span></span> 
  
<span data-ttu-id="323b9-105">Para hacer referencia a la celda LockThemeColors por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:

</span><span class="sxs-lookup"><span data-stu-id="323b9-105">To refer to the LockThemeColors cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="323b9-106">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="323b9-106">Cell name:</span></span>  <br/> |<span data-ttu-id="323b9-107">LockThemeColors</span><span class="sxs-lookup"><span data-stu-id="323b9-107">LockThemeColors</span></span>  <br/> |
   
<span data-ttu-id="323b9-108">Para hacer referencia desde un programa a la celda LockThemeColors según su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:

</span><span class="sxs-lookup"><span data-stu-id="323b9-108">To refer to the LockThemeColors cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="323b9-109">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="323b9-109">Section index:</span></span>  <br/> |<span data-ttu-id="323b9-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="323b9-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="323b9-111">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="323b9-111">Row index:</span></span>  <br/> |<span data-ttu-id="323b9-112">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="323b9-112">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="323b9-113">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="323b9-113">Cell index:</span></span>  <br/> |<span data-ttu-id="323b9-114">**visLockThemeColors**</span><span class="sxs-lookup"><span data-stu-id="323b9-114">**visLockThemeColors**</span></span> <br/> |
   

