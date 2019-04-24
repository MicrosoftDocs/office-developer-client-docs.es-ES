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
description: Representa la coordenada y de un punto de anclaje del controlador en coordenadas locales. El punto de anclaje se utiliza para determinar los límites elásticos en las operaciones dinámicas.
ms.openlocfilehash: 13d463ebccd9cc7a23641a036dc5dd967513b07f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341184"
---
# <a name="y-dynamics-cell-controls-section"></a><span data-ttu-id="7e526-104">Celda Y Dynamics (Sección de controles)</span><span class="sxs-lookup"><span data-stu-id="7e526-104">Y Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="7e526-105">Representa la coordenada *y* de un punto de anclaje del controlador en coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="7e526-105">Represents the  *y*  -coordinate for a control handle's anchor point in local coordinates.</span></span> <span data-ttu-id="7e526-106">El punto de anclaje se utiliza para determinar los límites elásticos en las operaciones dinámicas.</span><span class="sxs-lookup"><span data-stu-id="7e526-106">The anchor point is used for rubber-banding during dynamics.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7e526-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7e526-107">Remarks</span></span>

<span data-ttu-id="7e526-108">Para obtener una referencia a la celda Y Dynamics por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="7e526-108">To get a reference to the Y Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7e526-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="7e526-109">Cell name:</span></span>  <br/> | <span data-ttu-id="7e526-110">Mando.</span><span class="sxs-lookup"><span data-stu-id="7e526-110">Controls.</span></span>  <span data-ttu-id="7e526-111">*nombre* . Controles YDynwhere.</span><span class="sxs-lookup"><span data-stu-id="7e526-111">*name*  .YDynwhere Controls.</span></span>  <span data-ttu-id="7e526-112">*nombre* es el nombre de la fila de controles.</span><span class="sxs-lookup"><span data-stu-id="7e526-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="7e526-113">Para obtener una referencia desde un programa a la celda Y Dynamics por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7e526-113">To get a reference to the Y Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7e526-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="7e526-114">Section index:</span></span>  <br/> |<span data-ttu-id="7e526-115">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="7e526-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="7e526-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="7e526-116">Row index:</span></span>  <br/> |<span data-ttu-id="7e526-117">**visRowControl** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7e526-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7e526-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="7e526-118">Cell index:</span></span>  <br/> |<span data-ttu-id="7e526-119">**visCtlYDyn**</span><span class="sxs-lookup"><span data-stu-id="7e526-119">**visCtlYDyn**</span></span> <br/> |
   

