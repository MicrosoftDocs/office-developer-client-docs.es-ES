---
title: Celda Gamma (Sección de propiedades de la imagen)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm410
localization_priority: Normal
ms.assetid: 3dcaee26-391c-0494-4380-890ee825dc47
description: Ajusta o corrige la intensidad de una imagen para un dispositivo específico de salida, como por ejemplo un monitor o un escáner. El valor predeterminado es 1 (sin corrección).
ms.openlocfilehash: d00eb11ff1feffacf0d758bb25cdd56281e91327
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409016"
---
# <a name="gamma-cell-image-properties-section"></a><span data-ttu-id="908eb-104">Celda Gamma (Sección de propiedades de la imagen)</span><span class="sxs-lookup"><span data-stu-id="908eb-104">Gamma Cell (Image Properties Section)</span></span>

<span data-ttu-id="908eb-p102">Ajusta o corrige la intensidad de una imagen para un dispositivo específico de salida, como por ejemplo un monitor o un escáner. El valor predeterminado es 1 (sin corrección).</span><span class="sxs-lookup"><span data-stu-id="908eb-p102">Adjusts or corrects the intensity of an image for a particular output device, such as a monitor or scanner. The default value is 1 (no correction).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="908eb-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="908eb-107">Remarks</span></span>

<span data-ttu-id="908eb-108">Para obtener una referencia a la celda Gamma por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="908eb-108">To get a reference to the Gamma cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="908eb-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="908eb-109">Cell name:</span></span>  <br/> | <span data-ttu-id="908eb-110">Gamma</span><span class="sxs-lookup"><span data-stu-id="908eb-110">Gamma</span></span>  <br/> |
   
<span data-ttu-id="908eb-111">Para obtener una referencia desde un programa a la celda Gamma por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="908eb-111">To get a reference to the Gamma cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="908eb-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="908eb-112">Section index:</span></span>  <br/> |<span data-ttu-id="908eb-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="908eb-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="908eb-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="908eb-114">Row index:</span></span>  <br/> |<span data-ttu-id="908eb-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="908eb-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="908eb-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="908eb-116">Cell index:</span></span>  <br/> |<span data-ttu-id="908eb-117">**visImageGamma**</span><span class="sxs-lookup"><span data-stu-id="908eb-117">**visImageGamma**</span></span> <br/> |
   

