---
title: Celda NoShow (Sección de Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm735
localization_priority: Normal
ms.assetid: 831075ff-2875-b598-00bb-eb8481fee57b
description: Indica si un trazado se muestra en la página de dibujo.
ms.openlocfilehash: bd42b069e6796b107aafaea3080f6970c4f678c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410353"
---
# <a name="noshow-cell-geometry-section"></a><span data-ttu-id="15aa8-103">Celda NoShow (Sección de Geometría)</span><span class="sxs-lookup"><span data-stu-id="15aa8-103">NoShow Cell (Geometry Section)</span></span>

<span data-ttu-id="15aa8-104">Indica si un trazado se muestra en la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="15aa8-104">Indicates whether a path is displayed on the drawing page.</span></span>
  
|<span data-ttu-id="15aa8-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="15aa8-105">**Value**</span></span>|<span data-ttu-id="15aa8-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="15aa8-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="15aa8-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="15aa8-107">TRUE</span></span>  <br/> | <span data-ttu-id="15aa8-108">El trazo y relleno del trazado representado mediante la sección están ocultos.</span><span class="sxs-lookup"><span data-stu-id="15aa8-108">The stroke and fill of the path represented by the section is hidden.</span></span>  <br/> |
| <span data-ttu-id="15aa8-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="15aa8-109">FALSE</span></span>  <br/> | <span data-ttu-id="15aa8-110">El trazo y el relleno del trazado se muestran.</span><span class="sxs-lookup"><span data-stu-id="15aa8-110">The stroke and fill of the path is shown.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15aa8-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="15aa8-111">Remarks</span></span>

<span data-ttu-id="15aa8-112">Para obtener una referencia a la celda NoShow por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="15aa8-112">To get a reference to the NoShow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="15aa8-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="15aa8-113">Cell name:</span></span>  <br/> | <span data-ttu-id="15aa8-114">Geometría *i* . NoShow donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="15aa8-114">Geometry  *i*  .NoShow            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="15aa8-115">Para obtener una referencia desde un programa a la celda NoShow por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="15aa8-115">To get a reference to the NoShow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="15aa8-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="15aa8-116">Section index:</span></span>  <br/> |<span data-ttu-id="15aa8-117">**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="15aa8-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="15aa8-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="15aa8-118">Row index:</span></span>  <br/> |<span data-ttu-id="15aa8-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="15aa8-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="15aa8-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="15aa8-120">Cell index:</span></span>  <br/> |<span data-ttu-id="15aa8-121">**visCompNoShow**</span><span class="sxs-lookup"><span data-stu-id="15aa8-121">**visCompNoShow**</span></span> <br/> |
   

