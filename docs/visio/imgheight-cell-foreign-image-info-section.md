---
title: Celda ImgHeight (Sección de información de imagen externa)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm445
localization_priority: Normal
ms.assetid: decb86a4-b711-35e1-b9dc-744a84ee177c
description: 'Determina el alto de la imagen del objeto dentro de su borde. La fórmula predeterminada es:'
ms.openlocfilehash: 956bc478604fd19d8dfdbb7079e092e9e8a16e7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411200"
---
# <a name="imgheight-cell-foreign-image-info-section"></a><span data-ttu-id="05960-104">Celda ImgHeight (Sección de información de imagen externa)</span><span class="sxs-lookup"><span data-stu-id="05960-104">ImgHeight Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="05960-p102">Determina el alto de la imagen del objeto dentro de su borde. La fórmula predeterminada es:</span><span class="sxs-lookup"><span data-stu-id="05960-p102">Determines the height of the object's image within its border. The default formula is:</span></span>
  
<span data-ttu-id="05960-107">= Alto \* 1</span><span class="sxs-lookup"><span data-stu-id="05960-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="05960-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="05960-108">Remarks</span></span>

<span data-ttu-id="05960-109">Para obtener una referencia a la celda ImgHeight por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="05960-109">To get a reference to the ImgHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="05960-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="05960-110">Cell name:</span></span>  <br/> | <span data-ttu-id="05960-111">ImgHeight</span><span class="sxs-lookup"><span data-stu-id="05960-111">ImgHeight</span></span>  <br/> |
   
<span data-ttu-id="05960-112">Para obtener una referencia desde un programa a la celda ImgHeight por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="05960-112">To get a reference to the ImgHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="05960-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="05960-113">Section index:</span></span>  <br/> |<span data-ttu-id="05960-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="05960-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="05960-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="05960-115">Row index:</span></span>  <br/> |<span data-ttu-id="05960-116">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="05960-116">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="05960-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="05960-117">Cell index:</span></span>  <br/> |<span data-ttu-id="05960-118">**visFrgnImgHeight**</span><span class="sxs-lookup"><span data-stu-id="05960-118">**visFrgnImgHeight**</span></span> <br/> |
   

