---
title: Celda ImgWidth (Sección de información de imagen externa)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm460
localization_priority: Normal
ms.assetid: b57fb962-0b3e-f2e5-3b88-3edf33e40496
description: 'Determina el ancho de la imagen del objeto dentro de su borde. La fórmula predeterminada es:'
ms.openlocfilehash: 9da5e06a7fbf6ae77a49fb0410aefb406e2afecb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344726"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a><span data-ttu-id="998d4-104">Celda ImgWidth (sección de información de imagen externa)</span><span class="sxs-lookup"><span data-stu-id="998d4-104">ImgWidth Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="998d4-105">Determina el ancho de la imagen del objeto dentro de su borde.</span><span class="sxs-lookup"><span data-stu-id="998d4-105">Determines the width of the object's image within its border.</span></span> <span data-ttu-id="998d4-106">La fórmula predeterminada es:</span><span class="sxs-lookup"><span data-stu-id="998d4-106">The default formula is:</span></span>
  
<span data-ttu-id="998d4-107">= Ancho \* 1</span><span class="sxs-lookup"><span data-stu-id="998d4-107">= Width \* 1</span></span>
  
<span data-ttu-id="998d4-108">Si se recorta el objeto, cambia el factor por el que se multiplica el ancho.</span><span class="sxs-lookup"><span data-stu-id="998d4-108">Cropping the object changes the factor by which Width is multiplied.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="998d4-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="998d4-109">Remarks</span></span>

<span data-ttu-id="998d4-110">Para obtener una referencia a la celda ImgWidth por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="998d4-110">To get a reference to the ImgWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="998d4-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="998d4-111">Cell name:</span></span>  <br/> | <span data-ttu-id="998d4-112">ImgWidth</span><span class="sxs-lookup"><span data-stu-id="998d4-112">ImgWidth</span></span>  <br/> |
   
<span data-ttu-id="998d4-113">Para obtener una referencia desde un programa a la celda ImgWidth por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="998d4-113">To get a reference to the ImgWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="998d4-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="998d4-114">Section index:</span></span>  <br/> |<span data-ttu-id="998d4-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="998d4-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="998d4-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="998d4-116">Row index:</span></span>  <br/> |<span data-ttu-id="998d4-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="998d4-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="998d4-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="998d4-118">Cell index:</span></span>  <br/> |<span data-ttu-id="998d4-119">**visFrgnImgWidth**</span><span class="sxs-lookup"><span data-stu-id="998d4-119">**visFrgnImgWidth**</span></span> <br/> |
   

