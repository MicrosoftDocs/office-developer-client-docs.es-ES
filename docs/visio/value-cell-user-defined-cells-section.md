---
title: Celda Value (Sección de celdas definidas por el usuario)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1100
localization_priority: Normal
ms.assetid: 495b2aec-e197-75eb-9974-e7c92d26546f
description: Especifica un valor para la correspondiente celda definida por el usuario.
ms.openlocfilehash: d320c35fa8ae65dd0b21a83ad2cf23dbb3af77f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823508"
---
# <a name="value-cell-user-defined-cells-section"></a><span data-ttu-id="94175-103">Celda Value (sección Celdas definidas por el usuario)</span><span class="sxs-lookup"><span data-stu-id="94175-103">Value Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="94175-104">Especifica un valor para la celda correspondiente definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="94175-104">Specifies a value for the corresponding user-defined cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="94175-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="94175-105">Remarks</span></span>

<span data-ttu-id="94175-106">Para hacer referencia a este valor desde otra celda, especifique el nombre definido por el usuario indicado en la etiqueta de fila User.Row.</span><span class="sxs-lookup"><span data-stu-id="94175-106">To refer to this value in another cell, specify the user-defined name entered in the row label User.Row.</span></span>
  
<span data-ttu-id="94175-107">Para obtener una referencia a la celda Value por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="94175-107">To get a reference to the Value cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="94175-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="94175-108">Cell name:</span></span>  <br/> | <span data-ttu-id="94175-109">Usuario.</span><span class="sxs-lookup"><span data-stu-id="94175-109">User.</span></span>  <span data-ttu-id="94175-110">*Nombre* . El valor de where usuario.</span><span class="sxs-lookup"><span data-stu-id="94175-110">*Name*  .Value            where User.</span></span>  <span data-ttu-id="94175-111">*Nombre* es el nombre de fila</span><span class="sxs-lookup"><span data-stu-id="94175-111">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="94175-112">Para obtener una referencia desde un programa a la celda Value por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="94175-112">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="94175-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="94175-113">Section index:</span></span>  <br/> |<span data-ttu-id="94175-114">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="94175-114">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="94175-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="94175-115">Row index:</span></span>  <br/> |<span data-ttu-id="94175-116">**visRowUser** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="94175-116">**visRowUser** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="94175-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="94175-117">Cell index:</span></span>  <br/> |<span data-ttu-id="94175-118">**visUserValue**</span><span class="sxs-lookup"><span data-stu-id="94175-118">**visUserValue**</span></span> <br/> |
   

