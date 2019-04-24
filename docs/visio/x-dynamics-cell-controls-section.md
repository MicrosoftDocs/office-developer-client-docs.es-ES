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
description: Representa la coordenada x de un punto de anclaje del controlador en coordenadas locales.
ms.openlocfilehash: 7aef1fe779ae9b862e88eccf0112eb8696377858
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322305"
---
# <a name="x-dynamics-cell-controls-section"></a><span data-ttu-id="9c3ec-103">Celda X Dynamics (Sección de controles)</span><span class="sxs-lookup"><span data-stu-id="9c3ec-103">X Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="9c3ec-104">Representa la coordenada *x* de un punto de anclaje del controlador en coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="9c3ec-104">Represents the  *x*  -coordinate for a control handle's anchor point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9c3ec-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9c3ec-105">Remarks</span></span>

<span data-ttu-id="9c3ec-106">El punto de anclaje se utiliza para determinar los límites elásticos en las operaciones dinámicas.</span><span class="sxs-lookup"><span data-stu-id="9c3ec-106">The anchor point is used for rubber-banding during dynamics.</span></span>
  
<span data-ttu-id="9c3ec-107">Para obtener una referencia a la celda X Dynamics por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="9c3ec-107">To get a reference to the X Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9c3ec-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="9c3ec-108">Cell name:</span></span>  <br/> | <span data-ttu-id="9c3ec-109">Mando.</span><span class="sxs-lookup"><span data-stu-id="9c3ec-109">Controls.</span></span>  <span data-ttu-id="9c3ec-110">*nombre* . Controles XDynwhere.</span><span class="sxs-lookup"><span data-stu-id="9c3ec-110">*name*  .XDynwhere Controls.</span></span>  <span data-ttu-id="9c3ec-111">*nombre* es el nombre de la fila de controles.</span><span class="sxs-lookup"><span data-stu-id="9c3ec-111">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="9c3ec-112">Para obtener una referencia desde un programa a la celda X Dynamics por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9c3ec-112">To get a reference to the X Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9c3ec-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="9c3ec-113">Section index:</span></span>  <br/> |<span data-ttu-id="9c3ec-114">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="9c3ec-114">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="9c3ec-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="9c3ec-115">Row index:</span></span>  <br/> |<span data-ttu-id="9c3ec-116">**visRowControl** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9c3ec-116">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9c3ec-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="9c3ec-117">Cell index:</span></span>  <br/> |<span data-ttu-id="9c3ec-118">**visCtlXDyn**</span><span class="sxs-lookup"><span data-stu-id="9c3ec-118">**visCtlXDyn**</span></span> <br/> |
   

