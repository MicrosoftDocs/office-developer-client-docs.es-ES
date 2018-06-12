---
title: Celda DirY / B (Sección de puntos de conexión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm240
localization_priority: Normal
ms.assetid: d951c57d-2c22-0289-35af-44e3c2877b2c
description: Determina la y-component para el vector de alineación necesario de un punto de conexión coincidente. También se usa para orientar el segmento adjunto de un conector dinámico. Esta celda acepta flotante valor de punto.
ms.openlocfilehash: e650e598b1e47d666b2700d683a17300d3a8e67d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821971"
---
# <a name="diry--b-cell-connection-points-section"></a><span data-ttu-id="f4910-105">Celda DirY / B (Sección de puntos de conexión)</span><span class="sxs-lookup"><span data-stu-id="f4910-105">DirY / B Cell (Connection Points Section)</span></span>

<span data-ttu-id="f4910-106">Determina la *y* -component para el vector de alineación necesario de un punto de conexión coincidente.</span><span class="sxs-lookup"><span data-stu-id="f4910-106">Determines the  *y*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="f4910-107">También se usa para orientar el segmento adjunto de un conector dinámico.</span><span class="sxs-lookup"><span data-stu-id="f4910-107">It is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="f4910-108">Esta celda acepta flotante valor de punto.</span><span class="sxs-lookup"><span data-stu-id="f4910-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f4910-109">Notas</span><span class="sxs-lookup"><span data-stu-id="f4910-109">Remarks</span></span>

<span data-ttu-id="f4910-110">Para obtener una referencia a la DirY / B celda por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="f4910-110">To get a reference to the DirY / B cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4910-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="f4910-111">Cell name:</span></span>  <br/> |<span data-ttu-id="f4910-112">Connections.DirY [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="f4910-112">Connections.DirY[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f4910-113">Para obtener una referencia a la DirY / B celda por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f4910-113">To get a reference to the DirY / B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4910-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="f4910-114">Section index:</span></span>  <br/> |<span data-ttu-id="f4910-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="f4910-115">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="f4910-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="f4910-116">Row index:</span></span>  <br/> |<span data-ttu-id="f4910-117">**visRowConnectionPts** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f4910-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="f4910-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="f4910-118">Cell index:</span></span>  <br/> |<span data-ttu-id="f4910-119">**visCnnctDirY** (filas no extensibles)           **visCnnctB** (filas extensibles)</span><span class="sxs-lookup"><span data-stu-id="f4910-119">**visCnnctDirY** (non-extended rows)           **visCnnctB** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="f4910-120">Para obtener información sobre las filas extensibles y no extensibles, vea la fila de puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="f4910-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

