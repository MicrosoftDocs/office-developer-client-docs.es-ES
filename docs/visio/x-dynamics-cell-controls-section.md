---
title: Celda X Dynamics (Sección de controles)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1145
localization_priority: Normal
ms.assetid: 9757dfb4-6d37-0517-17fe-7593ff12bbfe
description: Representa la x-coordenadas de punto de anclaje del controlador en coordenadas locales.
ms.openlocfilehash: 9dee2381c15ed2817df9f89ebc830cf31bf64c1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823588"
---
# <a name="x-dynamics-cell-controls-section"></a><span data-ttu-id="90dac-103">Celda X Dynamics (Sección de controles)</span><span class="sxs-lookup"><span data-stu-id="90dac-103">X Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="90dac-104">Representa la *x* -coordenadas de punto de anclaje del controlador en coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="90dac-104">Represents the  *x*  -coordinate for a control handle's anchor point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="90dac-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="90dac-105">Remarks</span></span>

<span data-ttu-id="90dac-106">El punto de anclaje se utiliza para determinar los límites elásticos en las operaciones dinámicas.</span><span class="sxs-lookup"><span data-stu-id="90dac-106">The anchor point is used for rubber-banding during dynamics.</span></span>
  
<span data-ttu-id="90dac-107">Para obtener una referencia a la celda X Dynamics por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="90dac-107">To get a reference to the X Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="90dac-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="90dac-108">Cell name:</span></span>  <br/> | <span data-ttu-id="90dac-109">Controles.</span><span class="sxs-lookup"><span data-stu-id="90dac-109">Controls.</span></span>  <span data-ttu-id="90dac-110">*nombre* . Controles de XDynwhere.</span><span class="sxs-lookup"><span data-stu-id="90dac-110">*name*  .XDynwhere Controls.</span></span>  <span data-ttu-id="90dac-111">*nombre* es el nombre de la fila de controles.</span><span class="sxs-lookup"><span data-stu-id="90dac-111">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="90dac-112">Para obtener una referencia a la celda X Dynamics por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="90dac-112">To get a reference to the X Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="90dac-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="90dac-113">Section index:</span></span>  <br/> |<span data-ttu-id="90dac-114">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="90dac-114">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="90dac-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="90dac-115">Row index:</span></span>  <br/> |<span data-ttu-id="90dac-116">**visRowControl** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="90dac-116">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="90dac-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="90dac-117">Cell index:</span></span>  <br/> |<span data-ttu-id="90dac-118">**visCtlXDyn**</span><span class="sxs-lookup"><span data-stu-id="90dac-118">**visCtlXDyn**</span></span> <br/> |
   

