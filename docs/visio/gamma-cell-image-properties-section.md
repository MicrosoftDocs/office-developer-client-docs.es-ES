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
ms.openlocfilehash: 060cb02aa8fd33e5a6c70a2c0236f16b9552aea0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822210"
---
# <a name="gamma-cell-image-properties-section"></a><span data-ttu-id="af09f-104">Celda Gamma (sección Propiedades de la imagen)</span><span class="sxs-lookup"><span data-stu-id="af09f-104">Gamma Cell (Image Properties Section)</span></span>

<span data-ttu-id="af09f-p102">Ajusta o corrige la intensidad de una imagen para un dispositivo específico de salida, como por ejemplo un monitor o un escáner. El valor predeterminado es 1 (sin corrección).</span><span class="sxs-lookup"><span data-stu-id="af09f-p102">Adjusts or corrects the intensity of an image for a particular output device, such as a monitor or scanner. The default value is 1 (no correction).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="af09f-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="af09f-107">Remarks</span></span>

<span data-ttu-id="af09f-108">Para obtener una referencia a la celda Gamma por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="af09f-108">To get a reference to the Gamma cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="af09f-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="af09f-109">Cell name:</span></span>  <br/> | <span data-ttu-id="af09f-110">Gamma</span><span class="sxs-lookup"><span data-stu-id="af09f-110">Gamma</span></span>  <br/> |
   
<span data-ttu-id="af09f-111">Para obtener una referencia desde un programa a la celda Gamma por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="af09f-111">To get a reference to the Gamma cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="af09f-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="af09f-112">Section index:</span></span>  <br/> |<span data-ttu-id="af09f-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="af09f-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="af09f-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="af09f-114">Row index:</span></span>  <br/> |<span data-ttu-id="af09f-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="af09f-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="af09f-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="af09f-116">Cell index:</span></span>  <br/> |<span data-ttu-id="af09f-117">**visImageGamma**</span><span class="sxs-lookup"><span data-stu-id="af09f-117">**visImageGamma**</span></span> <br/> |
   

