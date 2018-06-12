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
ms.openlocfilehash: 3aab65d27d426287060f7572dad15174acb93199
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822326"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a><span data-ttu-id="6f7fb-104">Celda ImgWidth (Sección de información de imagen externa)</span><span class="sxs-lookup"><span data-stu-id="6f7fb-104">ImgWidth Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="6f7fb-p102">Determina el ancho de la imagen del objeto dentro de su borde. La fórmula predeterminada es:</span><span class="sxs-lookup"><span data-stu-id="6f7fb-p102">Determines the width of the object's image within its border. The default formula is:</span></span>
  
<span data-ttu-id="6f7fb-107">= Width \* 1</span><span class="sxs-lookup"><span data-stu-id="6f7fb-107">= Width \* 1</span></span>
  
<span data-ttu-id="6f7fb-108">Si se recorta el objeto, cambia el factor por el que se multiplica el ancho.</span><span class="sxs-lookup"><span data-stu-id="6f7fb-108">Cropping the object changes the factor by which Width is multiplied.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6f7fb-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6f7fb-109">Remarks</span></span>

<span data-ttu-id="6f7fb-110">Para obtener una referencia a la celda ImgWidth por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="6f7fb-110">To get a reference to the ImgWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6f7fb-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="6f7fb-111">Cell name:</span></span>  <br/> | <span data-ttu-id="6f7fb-112">ImgWidth</span><span class="sxs-lookup"><span data-stu-id="6f7fb-112">ImgWidth</span></span>  <br/> |
   
<span data-ttu-id="6f7fb-113">Para obtener una referencia a la celda ImgWidth por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6f7fb-113">To get a reference to the ImgWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6f7fb-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="6f7fb-114">Section index:</span></span>  <br/> |<span data-ttu-id="6f7fb-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6f7fb-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6f7fb-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="6f7fb-116">Row index:</span></span>  <br/> |<span data-ttu-id="6f7fb-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="6f7fb-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="6f7fb-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="6f7fb-118">Cell index:</span></span>  <br/> |<span data-ttu-id="6f7fb-119">**visFrgnImgWidth**</span><span class="sxs-lookup"><span data-stu-id="6f7fb-119">**visFrgnImgWidth**</span></span> <br/> |
   

