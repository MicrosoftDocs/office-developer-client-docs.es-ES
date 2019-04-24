---
title: Celda Y (Sección de puntos de conexión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_SDR.chm1175
localization_priority: Normal
ms.assetid: 3af6c949-d6a0-9560-54d7-b01a2ad99960
description: Representa la coordenada y de un punto de conexión en coordenadas locales.
ms.openlocfilehash: b408dc3c07e7bd28c0530b09f649453b4f08c770
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360133"
---
# <a name="y-cell-connection-points-section"></a><span data-ttu-id="b833a-103">Celda Y (Sección de puntos de conexión)</span><span class="sxs-lookup"><span data-stu-id="b833a-103">Y Cell (Connection Points Section)</span></span>

<span data-ttu-id="b833a-104">Representa la coordenada *y* de un punto de conexión en coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="b833a-104">Represents the  *y*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b833a-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b833a-105">Remarks</span></span>

<span data-ttu-id="b833a-106">Para obtener una referencia desde un programa a la celda Y por su índice, utilice la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="b833a-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b833a-107">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b833a-107">Cell name:</span></span>  <br/> | <span data-ttu-id="b833a-108">Connections. Y *i* donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b833a-108">Connections.Y  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b833a-109">Para obtener una referencia desde un programa a la celda Y por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b833a-109">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b833a-110">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b833a-110">Section index:</span></span>  <br/> |<span data-ttu-id="b833a-111">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="b833a-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="b833a-112">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b833a-112">Row index:</span></span>  <br/> |<span data-ttu-id="b833a-113">**visRowConnectionPts** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b833a-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b833a-114">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b833a-114">Cell index:</span></span>  <br/> |<span data-ttu-id="b833a-115">**visY**</span><span class="sxs-lookup"><span data-stu-id="b833a-115">**visY**</span></span> <br/> |
   

