---
title: Celda E (Sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251761
localization_priority: Normal
ms.assetid: bc0154b1-6930-1fe0-655c-05eab2d60230
description: Contiene la fórmula de una spline B racional no uniforme (NURBS).
ms.openlocfilehash: 000c4864c6ae98bfcd9e9cfdb16ff68396f63e44
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822049"
---
# <a name="e-cell-geometry-section"></a><span data-ttu-id="3c879-103">Celda E (Sección de geometría)</span><span class="sxs-lookup"><span data-stu-id="3c879-103">E Cell (Geometry Section)</span></span>

<span data-ttu-id="3c879-104">Contiene la fórmula de una spline B racional no uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="3c879-104">Contains a nonuniform rational B-spline (NURBS) formula.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3c879-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3c879-105">Remarks</span></span>

<span data-ttu-id="3c879-106">Para obtener una referencia a la celda E por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="3c879-106">To get a reference to the E cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3c879-107">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="3c879-107">Cell name:</span></span>  <br/> | <span data-ttu-id="3c879-108">Geometría *i* . E *j* donde *i* y *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="3c879-108">Geometry  *i*  .E  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="3c879-109">Para obtener una referencia a la celda E por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3c879-109">To get a reference to the E cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3c879-110">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="3c879-110">Section index:</span></span>  <br/> |<span data-ttu-id="3c879-111">**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3c879-111">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3c879-112">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="3c879-112">Row index:</span></span>  <br/> |<span data-ttu-id="3c879-113">**visRowVertex** +  *j* donde *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3c879-113">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3c879-114">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="3c879-114">Cell index:</span></span>  <br/> |<span data-ttu-id="3c879-115">**visNURBSData**</span><span class="sxs-lookup"><span data-stu-id="3c879-115">**visNURBSData**</span></span> <br/> |
   

