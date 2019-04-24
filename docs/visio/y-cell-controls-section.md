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
description: Representa la coordenada y que indica la ubicación del controlador de una forma en coordenadas locales.
ms.openlocfilehash: 14aaa7aef7e7250baeb8ffb863244ece26a201e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360154"
---
# <a name="y-cell-controls-section"></a><span data-ttu-id="dfc4f-103">Celda Y (Sección de controles)</span><span class="sxs-lookup"><span data-stu-id="dfc4f-103">Y Cell (Controls Section)</span></span>

<span data-ttu-id="dfc4f-104">Representa la coordenada *y* que indica la ubicación del controlador de una forma en coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="dfc4f-104">Represents the  *y*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dfc4f-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dfc4f-105">Remarks</span></span>

<span data-ttu-id="dfc4f-106">Para obtener una referencia desde un programa a la celda Y por su índice, utilice la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="dfc4f-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dfc4f-107">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="dfc4f-107">Cell name:</span></span>  <br/> | <span data-ttu-id="dfc4f-108">Mando.</span><span class="sxs-lookup"><span data-stu-id="dfc4f-108">Controls.</span></span>  <span data-ttu-id="dfc4f-109">*nombre* . Controles ydonde.</span><span class="sxs-lookup"><span data-stu-id="dfc4f-109">*name*  .Ywhere Controls.</span></span>  <span data-ttu-id="dfc4f-110">*nombre* es el nombre de la fila de controles.</span><span class="sxs-lookup"><span data-stu-id="dfc4f-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="dfc4f-111">Para obtener una referencia desde un programa a la celda Y por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="dfc4f-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dfc4f-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="dfc4f-112">Section index:</span></span>  <br/> |<span data-ttu-id="dfc4f-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="dfc4f-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="dfc4f-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="dfc4f-114">Row index:</span></span>  <br/> |<span data-ttu-id="dfc4f-115">**visRowControl** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dfc4f-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="dfc4f-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="dfc4f-116">Cell index:</span></span>  <br/> |<span data-ttu-id="dfc4f-117">**visCtlY**</span><span class="sxs-lookup"><span data-stu-id="dfc4f-117">**visCtlY**</span></span> <br/> |
   

