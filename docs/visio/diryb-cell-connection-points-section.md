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
description: Determina el componente y para el vector de alineación necesario de un punto de conexión correspondiente. También se utiliza para orientar el segmento adjunto de un conector dinámico. Esta celda acepta valores de punto flotante.
ms.openlocfilehash: b0dc3c9f7e1a9e87b2ecdace21c8fa1658b1388d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417094"
---
# <a name="diry--b-cell-connection-points-section"></a><span data-ttu-id="85078-105">Celda DirY / B (Sección de puntos de conexión)</span><span class="sxs-lookup"><span data-stu-id="85078-105">DirY / B Cell (Connection Points Section)</span></span>

<span data-ttu-id="85078-106">Determina el componente  *y para*  el vector de alineación necesario de un punto de conexión correspondiente.</span><span class="sxs-lookup"><span data-stu-id="85078-106">Determines the  *y*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="85078-107">También se utiliza para orientar el segmento adjunto de un conector dinámico.</span><span class="sxs-lookup"><span data-stu-id="85078-107">It is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="85078-108">Esta celda toma valores de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="85078-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="85078-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="85078-109">Remarks</span></span>

<span data-ttu-id="85078-110">Para obtener una referencia a la celda DirY / B por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="85078-110">To get a reference to the DirY / B cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85078-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="85078-111">Cell name:</span></span>  <br/> |<span data-ttu-id="85078-112">Connections.DirY[ *i*  ] donde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="85078-112">Connections.DirY[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="85078-113">Para obtener una referencia desde un programa a la celda DirY / B por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="85078-113">To get a reference to the DirY / B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85078-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="85078-114">Section index:</span></span>  <br/> |<span data-ttu-id="85078-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="85078-115">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="85078-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="85078-116">Row index:</span></span>  <br/> |<span data-ttu-id="85078-117">**visRowConnectionPts**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="85078-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="85078-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="85078-118">Cell index:</span></span>  <br/> |<span data-ttu-id="85078-119">**visCnnctDirY** (filas no extendidas)           **visCnnctB** (filas extendidas)</span><span class="sxs-lookup"><span data-stu-id="85078-119">**visCnnctDirY** (non-extended rows)           **visCnnctB** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="85078-120">Para obtener información sobre las filas extensibles y no extensibles, vea la fila de puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="85078-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

