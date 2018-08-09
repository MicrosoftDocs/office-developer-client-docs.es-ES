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
ms.openlocfilehash: 983bb919dbfada65b6d9af464ecfa17c04e970c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822328"
---
# <a name="imgheight-cell-foreign-image-info-section"></a><span data-ttu-id="c09ba-104">Celda ImgHeight (sección Información de imagen externa)</span><span class="sxs-lookup"><span data-stu-id="c09ba-104">ImgHeight Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="c09ba-p102">Determina el alto de la imagen del objeto dentro de su borde. La fórmula predeterminada es:</span><span class="sxs-lookup"><span data-stu-id="c09ba-p102">Determines the height of the object's image within its border. The default formula is:</span></span>
  
<span data-ttu-id="c09ba-107">= Alto \* 1</span><span class="sxs-lookup"><span data-stu-id="c09ba-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c09ba-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c09ba-108">Remarks</span></span>

<span data-ttu-id="c09ba-109">Para obtener una referencia a la celda ImgHeight por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="c09ba-109">To get a reference to the ImgHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c09ba-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c09ba-110">Cell name:</span></span>  <br/> | <span data-ttu-id="c09ba-111">ImgHeight</span><span class="sxs-lookup"><span data-stu-id="c09ba-111">ImgHeight</span></span>  <br/> |
   
<span data-ttu-id="c09ba-112">Para obtener una referencia desde un programa a la celda ImgHeight por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c09ba-112">To get a reference to the ImgHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c09ba-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c09ba-113">Section index:</span></span>  <br/> |<span data-ttu-id="c09ba-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c09ba-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c09ba-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c09ba-115">Row index:</span></span>  <br/> |<span data-ttu-id="c09ba-116">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="c09ba-116">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="c09ba-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c09ba-117">Cell index:</span></span>  <br/> |<span data-ttu-id="c09ba-118">**visFrgnImgHeight**</span><span class="sxs-lookup"><span data-stu-id="c09ba-118">**visFrgnImgHeight**</span></span> <br/> |
   

