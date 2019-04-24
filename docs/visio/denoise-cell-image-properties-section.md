---
title: Celda Denoise (Sección de propiedades de la imagen)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm225
localization_priority: Normal
ms.assetid: e305585f-f0d8-0494-91d4-0c76929dc170
description: Quita el ruido (píxeles con niveles de color distribuidos aleatoriamente) de una imagen de mapa de bits. El valor predeterminado es 0%.
ms.openlocfilehash: f970fde22e864239ea3f3f9bcb704e7f4692e9cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360252"
---
# <a name="denoise-cell-image-properties-section"></a><span data-ttu-id="466fa-104">Celda Denoise (Sección de propiedades de la imagen)</span><span class="sxs-lookup"><span data-stu-id="466fa-104">Denoise Cell (Image Properties Section)</span></span>

<span data-ttu-id="466fa-105">Quita el ruido (píxeles con niveles de color distribuidos aleatoriamente) de una imagen de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="466fa-105">Removes noise (pixels with randomly distributed color levels) from a bitmap image.</span></span> <span data-ttu-id="466fa-106">El valor predeterminado es 0%.</span><span class="sxs-lookup"><span data-stu-id="466fa-106">The default value is 0%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="466fa-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="466fa-107">Remarks</span></span>

<span data-ttu-id="466fa-108">Para obtener una referencia a la celda Denoise por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="466fa-108">To get a reference to the Denoise cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="466fa-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="466fa-109">Cell name:</span></span>  <br/> | <span data-ttu-id="466fa-110">Denoise</span><span class="sxs-lookup"><span data-stu-id="466fa-110">Denoise</span></span>  <br/> |
   
<span data-ttu-id="466fa-111">Para obtener una referencia desde un programa a la celda Denoise por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="466fa-111">To get a reference to the Denoise cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="466fa-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="466fa-112">Section index:</span></span>  <br/> |<span data-ttu-id="466fa-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="466fa-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="466fa-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="466fa-114">Row index:</span></span>  <br/> |<span data-ttu-id="466fa-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="466fa-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="466fa-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="466fa-116">Cell index:</span></span>  <br/> |<span data-ttu-id="466fa-117">**visImageDenoise**</span><span class="sxs-lookup"><span data-stu-id="466fa-117">**visImageDenoise**</span></span> <br/> |
   

