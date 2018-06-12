---
title: Celda Y Dynamics (Sección de controles)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251284
localization_priority: Normal
ms.assetid: cb221974-2f1a-edb0-477b-39a3c4a64c56
description: Representa la y-coordenadas de punto de anclaje del controlador en coordenadas locales. El punto de anclaje se utiliza para determinar los límites elásticos en las operaciones dinámicas.
ms.openlocfilehash: 162f062d382f3f303ae39db725f3fbfa0790bfc4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823618"
---
# <a name="y-dynamics-cell-controls-section"></a><span data-ttu-id="83e06-104">Celda Y Dynamics (Sección de controles)</span><span class="sxs-lookup"><span data-stu-id="83e06-104">Y Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="83e06-105">Representa la *y* -coordenadas de punto de anclaje del controlador en coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="83e06-105">Represents the  *y*  -coordinate for a control handle's anchor point in local coordinates.</span></span> <span data-ttu-id="83e06-106">El punto de anclaje se utiliza para determinar los límites elásticos en las operaciones dinámicas.</span><span class="sxs-lookup"><span data-stu-id="83e06-106">The anchor point is used for rubber-banding during dynamics.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="83e06-107">Notas</span><span class="sxs-lookup"><span data-stu-id="83e06-107">Remarks</span></span>

<span data-ttu-id="83e06-108">Para obtener una referencia a la celda Y Dynamics por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="83e06-108">To get a reference to the Y Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="83e06-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="83e06-109">Cell name:</span></span>  <br/> | <span data-ttu-id="83e06-110">Controles.</span><span class="sxs-lookup"><span data-stu-id="83e06-110">Controls.</span></span>  <span data-ttu-id="83e06-111">*nombre* . Controles de YDynwhere.</span><span class="sxs-lookup"><span data-stu-id="83e06-111">*name*  .YDynwhere Controls.</span></span>  <span data-ttu-id="83e06-112">*nombre* es el nombre de la fila de controles.</span><span class="sxs-lookup"><span data-stu-id="83e06-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="83e06-113">Para obtener una referencia a la celda Y Dynamics por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="83e06-113">To get a reference to the Y Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="83e06-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="83e06-114">Section index:</span></span>  <br/> |<span data-ttu-id="83e06-115">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="83e06-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="83e06-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="83e06-116">Row index:</span></span>  <br/> |<span data-ttu-id="83e06-117">**visRowControl** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="83e06-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="83e06-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="83e06-118">Cell index:</span></span>  <br/> |<span data-ttu-id="83e06-119">**visCtlYDyn**</span><span class="sxs-lookup"><span data-stu-id="83e06-119">**visCtlYDyn**</span></span> <br/> |
   

