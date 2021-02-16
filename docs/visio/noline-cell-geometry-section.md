---
title: Celda NoLine (Sección de Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm715
localization_priority: Normal
ms.assetid: f9624af2-c087-3dde-9140-339c438b3652
description: Determina si se dibuja una línea alrededor del límite del trazado.
ms.openlocfilehash: ad3744ae8deb4ffb4dd2282e50590439c4b218a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433755"
---
# <a name="noline-cell-geometry-section"></a><span data-ttu-id="a7723-103">Celda NoLine (Sección de Geometría)</span><span class="sxs-lookup"><span data-stu-id="a7723-103">NoLine Cell (Geometry Section)</span></span>

<span data-ttu-id="a7723-104">Determina si se dibuja una línea alrededor del límite del trazado.</span><span class="sxs-lookup"><span data-stu-id="a7723-104">Determines whether a line is drawn around the boundary of the path.</span></span>
  
|<span data-ttu-id="a7723-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a7723-105">**Value**</span></span>|<span data-ttu-id="a7723-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a7723-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a7723-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a7723-107">TRUE</span></span>  <br/> | <span data-ttu-id="a7723-108">No se dibuja una línea alrededor del límite del trazado que es el límite de una región rellena.</span><span class="sxs-lookup"><span data-stu-id="a7723-108">A line is not drawn around the boundary of the path that is the boundary of a filled region.</span></span>  <br/> |
| <span data-ttu-id="a7723-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a7723-109">FALSE</span></span>  <br/> | <span data-ttu-id="a7723-110">Se dibuja una línea alrededor del límite de un trazado.</span><span class="sxs-lookup"><span data-stu-id="a7723-110">A line is drawn around the boundary of a path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7723-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a7723-111">Remarks</span></span>

<span data-ttu-id="a7723-p101">Cuando el color de una línea cambia a blanco, la línea sigue existiendo aunque no esté visible en un fondo blanco. Cuando se establece el valor de esta celda a TRUE, no se dibuja ninguna línea.</span><span class="sxs-lookup"><span data-stu-id="a7723-p101">When you change the color of a line to white, the line still exists even though you can't see it on a white background. When you set the value of this cell to TRUE, no line is drawn.</span></span>
  
<span data-ttu-id="a7723-114">Para obtener una referencia a la celda NoLine por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="a7723-114">To get a reference to the NoLine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a7723-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="a7723-115">Cell name:</span></span>  <br/> | <span data-ttu-id="a7723-116">Geometría  *i*  . NoLine donde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="a7723-116">Geometry  *i*  .NoLine            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a7723-117">Para obtener una referencia desde un programa a la celda NoLine por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a7723-117">To get a reference to the NoLine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a7723-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="a7723-118">Section index:</span></span>  <br/> |<span data-ttu-id="a7723-119">**visSectionFirstComponent**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a7723-119">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a7723-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="a7723-120">Row index:</span></span>  <br/> |<span data-ttu-id="a7723-121">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="a7723-121">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="a7723-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="a7723-122">Cell index:</span></span>  <br/> |<span data-ttu-id="a7723-123">**visCompNoLine**</span><span class="sxs-lookup"><span data-stu-id="a7723-123">**visCompNoLine**</span></span> <br/> |
   

