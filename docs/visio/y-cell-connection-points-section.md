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
description: Representa la y-coordenadas de un punto de conexión en coordenadas locales.
ms.openlocfilehash: 270ae98789e29ca170f260aa70e951d4b2af2962
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823573"
---
# <a name="y-cell-connection-points-section"></a><span data-ttu-id="09b29-103">Celda Y (Sección de puntos de conexión)</span><span class="sxs-lookup"><span data-stu-id="09b29-103">Y Cell (Connection Points Section)</span></span>

<span data-ttu-id="09b29-104">Representa la *y* -coordenadas de un punto de conexión en coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="09b29-104">Represents the  *y*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="09b29-105">Notas</span><span class="sxs-lookup"><span data-stu-id="09b29-105">Remarks</span></span>

<span data-ttu-id="09b29-106">Para obtener una referencia a la celda Y por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="09b29-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="09b29-107">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="09b29-107">Cell name:</span></span>  <br/> | <span data-ttu-id="09b29-108">Connections.Y *i* donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="09b29-108">Connections.Y  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="09b29-109">Para obtener una referencia a la celda Y por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="09b29-109">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="09b29-110">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="09b29-110">Section index:</span></span>  <br/> |<span data-ttu-id="09b29-111">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="09b29-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="09b29-112">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="09b29-112">Row index:</span></span>  <br/> |<span data-ttu-id="09b29-113">**visRowConnectionPts** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="09b29-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="09b29-114">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="09b29-114">Cell index:</span></span>  <br/> |<span data-ttu-id="09b29-115">**visY**</span><span class="sxs-lookup"><span data-stu-id="09b29-115">**visY**</span></span> <br/> |
   

