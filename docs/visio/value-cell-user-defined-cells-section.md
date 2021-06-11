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
description: Especifica un valor para la celda correspondiente definida por el usuario.
ms.openlocfilehash: 137d22430829f96a9c6ad69a73a6b44e964d5f4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422994"
---
# <a name="value-cell-user-defined-cells-section"></a><span data-ttu-id="5ef4f-103">Celda Value (Sección de celdas definidas por el usuario)</span><span class="sxs-lookup"><span data-stu-id="5ef4f-103">Value Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="5ef4f-104">Especifica un valor para la celda correspondiente definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="5ef4f-104">Specifies a value for the corresponding user-defined cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5ef4f-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5ef4f-105">Remarks</span></span>

<span data-ttu-id="5ef4f-106">Para hacer referencia a este valor desde otra celda, especifique el nombre definido por el usuario indicado en la etiqueta de fila User.Row.</span><span class="sxs-lookup"><span data-stu-id="5ef4f-106">To refer to this value in another cell, specify the user-defined name entered in the row label User.Row.</span></span>
  
<span data-ttu-id="5ef4f-107">Para obtener una referencia a la celda Value por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="5ef4f-107">To get a reference to the Value cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ef4f-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="5ef4f-108">Cell name:</span></span>  <br/> | <span data-ttu-id="5ef4f-109">Usuario.</span><span class="sxs-lookup"><span data-stu-id="5ef4f-109">User.</span></span>  <span data-ttu-id="5ef4f-110">*Nombre*  . Valor donde user.</span><span class="sxs-lookup"><span data-stu-id="5ef4f-110">*Name*  .Value            where User.</span></span>  <span data-ttu-id="5ef4f-111">*Name*  es el nombre de fila</span><span class="sxs-lookup"><span data-stu-id="5ef4f-111">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="5ef4f-112">Para obtener una referencia desde un programa a la celda Value por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5ef4f-112">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ef4f-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="5ef4f-113">Section index:</span></span>  <br/> |<span data-ttu-id="5ef4f-114">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="5ef4f-114">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="5ef4f-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="5ef4f-115">Row index:</span></span>  <br/> |<span data-ttu-id="5ef4f-116">**visRowUser**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5ef4f-116">**visRowUser** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5ef4f-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="5ef4f-117">Cell index:</span></span>  <br/> |<span data-ttu-id="5ef4f-118">**visUserValue**</span><span class="sxs-lookup"><span data-stu-id="5ef4f-118">**visUserValue**</span></span> <br/> |
   

