---
title: Celda Y (Sección de controles)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251282
localization_priority: Normal
ms.assetid: dd7ea5fa-1d34-44e8-5a29-69ca542aecba
description: Representa la y-coordenada que indica la ubicación del controlador de una forma en coordenadas locales.
ms.openlocfilehash: 8104ae6d647feb4e1b83474b63f40e243e5405e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823584"
---
# <a name="y-cell-controls-section"></a><span data-ttu-id="a125e-103">Celda Y (Sección de controles)</span><span class="sxs-lookup"><span data-stu-id="a125e-103">Y Cell (Controls Section)</span></span>

<span data-ttu-id="a125e-104">Representa la *y* -coordenada que indica la ubicación del controlador de una forma en coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="a125e-104">Represents the  *y*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a125e-105">Notas</span><span class="sxs-lookup"><span data-stu-id="a125e-105">Remarks</span></span>

<span data-ttu-id="a125e-106">Para obtener una referencia a la celda Y por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="a125e-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a125e-107">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="a125e-107">Cell name:</span></span>  <br/> | <span data-ttu-id="a125e-108">Controles.</span><span class="sxs-lookup"><span data-stu-id="a125e-108">Controls.</span></span>  <span data-ttu-id="a125e-109">*nombre* . Controles de Ywhere.</span><span class="sxs-lookup"><span data-stu-id="a125e-109">*name*  .Ywhere Controls.</span></span>  <span data-ttu-id="a125e-110">*nombre* es el nombre de la fila de controles.</span><span class="sxs-lookup"><span data-stu-id="a125e-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="a125e-111">Para obtener una referencia a la celda Y por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a125e-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a125e-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="a125e-112">Section index:</span></span>  <br/> |<span data-ttu-id="a125e-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="a125e-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="a125e-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="a125e-114">Row index:</span></span>  <br/> |<span data-ttu-id="a125e-115">**visRowControl** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a125e-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a125e-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="a125e-116">Cell index:</span></span>  <br/> |<span data-ttu-id="a125e-117">**visCtlY**</span><span class="sxs-lookup"><span data-stu-id="a125e-117">**visCtlY**</span></span> <br/> |
   

