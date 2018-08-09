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
ms.openlocfilehash: ad4d9cf1aa3e541f512bc09ffc38cf03204b3c94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822711"
---
# <a name="noshow-cell-geometry-section"></a><span data-ttu-id="fdbde-103">Celda NoShow (sección Geometría)</span><span class="sxs-lookup"><span data-stu-id="fdbde-103">NoShow Cell (Geometry Section)</span></span>

<span data-ttu-id="fdbde-104">Indica si un trazado se muestra en la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="fdbde-104">Indicates whether a path is displayed on the drawing page.</span></span>
  
|<span data-ttu-id="fdbde-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fdbde-105">**Value**</span></span>|<span data-ttu-id="fdbde-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fdbde-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="fdbde-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="fdbde-107">TRUE</span></span>  <br/> | <span data-ttu-id="fdbde-108">El trazo y relleno del trazado representado mediante la sección están ocultos.</span><span class="sxs-lookup"><span data-stu-id="fdbde-108">The stroke and fill of the path represented by the section is hidden.</span></span>  <br/> |
| <span data-ttu-id="fdbde-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="fdbde-109">FALSE</span></span>  <br/> | <span data-ttu-id="fdbde-110">El trazo y el relleno del trazado se muestran.</span><span class="sxs-lookup"><span data-stu-id="fdbde-110">The stroke and fill of the path is shown.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fdbde-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fdbde-111">Remarks</span></span>

<span data-ttu-id="fdbde-112">Para obtener una referencia a la celda NoShow por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="fdbde-112">To get a reference to the NoShow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fdbde-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="fdbde-113">Cell name:</span></span>  <br/> | <span data-ttu-id="fdbde-114">Geometría *i* . NoShow donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="fdbde-114">Geometry  *i*  .NoShow            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="fdbde-115">Para obtener una referencia desde un programa a la celda NoShow por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="fdbde-115">To get a reference to the NoShow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fdbde-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="fdbde-116">Section index:</span></span>  <br/> |<span data-ttu-id="fdbde-117">**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fdbde-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="fdbde-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="fdbde-118">Row index:</span></span>  <br/> |<span data-ttu-id="fdbde-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="fdbde-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="fdbde-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="fdbde-120">Cell index:</span></span>  <br/> |<span data-ttu-id="fdbde-121">**visCompNoShow**</span><span class="sxs-lookup"><span data-stu-id="fdbde-121">**visCompNoShow**</span></span> <br/> |
   

