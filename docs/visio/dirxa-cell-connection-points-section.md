---
title: Celda DirX / A (Sección de puntos de conexión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251721
localization_priority: Normal
ms.assetid: 00d87b92-0da7-37d6-e7b5-23f350db0a9b
description: Determina la x-component para el vector de alineación necesario de un punto de conexión coincidente. El DirX / una celda también se utiliza para orientar el segmento adjunto de un conector dinámico. Esta celda acepta flotante valor de punto.
ms.openlocfilehash: 49feba7cefbccc4efcbd04e8940c1f801563539e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822000"
---
# <a name="dirx--a-cell-connection-points-section"></a><span data-ttu-id="7def7-105">Celda DirX / A (sección Puntos de conexión)</span><span class="sxs-lookup"><span data-stu-id="7def7-105">DirX / A Cell (Connection Points Section)</span></span>

<span data-ttu-id="7def7-106">Determina la *x* -component para el vector de alineación necesario de un punto de conexión coincidente.</span><span class="sxs-lookup"><span data-stu-id="7def7-106">Determines the  *x*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="7def7-107">El DirX / una celda también se utiliza para orientar el segmento adjunto de un conector dinámico.</span><span class="sxs-lookup"><span data-stu-id="7def7-107">The DirX / A cell is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="7def7-108">Esta celda acepta flotante valor de punto.</span><span class="sxs-lookup"><span data-stu-id="7def7-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7def7-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7def7-109">Remarks</span></span>

<span data-ttu-id="7def7-110">Para obtener una referencia a la celda DirX / A por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="7def7-110">To get a reference to the DirX / A cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7def7-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="7def7-111">Cell name:</span></span>  <br/> | <span data-ttu-id="7def7-112">Connections.DirX [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7def7-112">Connections.DirX[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7def7-113">Para obtener una referencia desde un programa a la celda DirX / A por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7def7-113">To get a reference to the DirX / A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7def7-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="7def7-114">Section index:</span></span>  <br/> |<span data-ttu-id="7def7-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="7def7-115">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="7def7-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="7def7-116">Row index:</span></span>  <br/> |<span data-ttu-id="7def7-117">**visRowConnectionPts** +  *i* donde *i* = 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="7def7-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2</span></span>  <br/> |
| <span data-ttu-id="7def7-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="7def7-118">Cell index:</span></span>  <br/> |<span data-ttu-id="7def7-119">**visCnnctDirX** (filas no extensibles)           **visCnnctA** (filas extensibles)</span><span class="sxs-lookup"><span data-stu-id="7def7-119">**visCnnctDirX** (non-extended rows)           **visCnnctA** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="7def7-120">Para obtener información sobre las filas extensibles y no extensibles, vea la fila de puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="7def7-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

