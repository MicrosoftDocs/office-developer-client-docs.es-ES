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
description: Representa la coordenada y del punto de anclaje de un controlador en coordenadas locales. El punto de anclaje se utiliza para determinar los límites elásticos en las operaciones dinámicas.
ms.openlocfilehash: 13d463ebccd9cc7a23641a036dc5dd967513b07f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404830"
---
# <a name="y-dynamics-cell-controls-section"></a><span data-ttu-id="56764-104">Celda Y Dynamics (Sección de controles)</span><span class="sxs-lookup"><span data-stu-id="56764-104">Y Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="56764-105">Representa la  *coordenada y*  del punto de anclaje de un controlador en coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="56764-105">Represents the  *y*  -coordinate for a control handle's anchor point in local coordinates.</span></span> <span data-ttu-id="56764-106">El punto de anclaje se utiliza para determinar los límites elásticos en las operaciones dinámicas.</span><span class="sxs-lookup"><span data-stu-id="56764-106">The anchor point is used for rubber-banding during dynamics.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="56764-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="56764-107">Remarks</span></span>

<span data-ttu-id="56764-108">Para obtener una referencia a la celda Y Dynamics por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="56764-108">To get a reference to the Y Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="56764-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="56764-109">Cell name:</span></span>  <br/> | <span data-ttu-id="56764-110">Controles.</span><span class="sxs-lookup"><span data-stu-id="56764-110">Controls.</span></span>  <span data-ttu-id="56764-111">*nombre*  . Controles de YDynwhere.</span><span class="sxs-lookup"><span data-stu-id="56764-111">*name*  .YDynwhere Controls.</span></span>  <span data-ttu-id="56764-112">*es*  el nombre de la fila de controles.</span><span class="sxs-lookup"><span data-stu-id="56764-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="56764-113">Para obtener una referencia desde un programa a la celda Y Dynamics por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="56764-113">To get a reference to the Y Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="56764-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="56764-114">Section index:</span></span>  <br/> |<span data-ttu-id="56764-115">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="56764-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="56764-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="56764-116">Row index:</span></span>  <br/> |<span data-ttu-id="56764-117">**visRowControl**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="56764-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="56764-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="56764-118">Cell index:</span></span>  <br/> |<span data-ttu-id="56764-119">**visCtlYDyn**</span><span class="sxs-lookup"><span data-stu-id="56764-119">**visCtlYDyn**</span></span> <br/> |
   

