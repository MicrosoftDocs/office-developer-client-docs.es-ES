---
title: Celda LocPinX (Sección de transformación de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm680
localization_priority: Normal
ms.assetid: b82feade-5793-8a6e-3ff4-69a4cbdd2cf9
description: 'Representa la x-coordenadas del eje de la forma (centro de rotación) en relación con el origen de la forma. La fórmula predeterminada para determinar LocPinX es:'
ms.openlocfilehash: 17f7b0fde9a54f6596f2f87f866d30b908e062b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822556"
---
# <a name="locpinx-cell-shape-transform-section"></a><span data-ttu-id="1eb28-104">Celda LocPinX (sección Transformación de forma)</span><span class="sxs-lookup"><span data-stu-id="1eb28-104">LocPinX Cell (Shape Transform Section)</span></span>

<span data-ttu-id="1eb28-105">Representa la *x* -coordenadas del eje de la forma (centro de rotación) en relación con el origen de la forma.</span><span class="sxs-lookup"><span data-stu-id="1eb28-105">Represents the  *x*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="1eb28-106">La fórmula predeterminada para determinar LocPinX es:</span><span class="sxs-lookup"><span data-stu-id="1eb28-106">The default formula for determining LocPinX is:</span></span> 
  
<span data-ttu-id="1eb28-107">= Width \* 0,5</span><span class="sxs-lookup"><span data-stu-id="1eb28-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1eb28-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1eb28-108">Remarks</span></span>

<span data-ttu-id="1eb28-109">Para obtener una referencia a la celda LocPinX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="1eb28-109">To get a reference to the LocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1eb28-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="1eb28-110">Cell name:</span></span>  <br/> | <span data-ttu-id="1eb28-111">LocPinX</span><span class="sxs-lookup"><span data-stu-id="1eb28-111">LocPinX</span></span>  <br/> |
   
<span data-ttu-id="1eb28-112">Para obtener una referencia desde un programa a la celda LocPinX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1eb28-112">To get a reference to the LocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1eb28-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="1eb28-113">Section index:</span></span>  <br/> |<span data-ttu-id="1eb28-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1eb28-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1eb28-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="1eb28-115">Row index:</span></span>  <br/> |<span data-ttu-id="1eb28-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="1eb28-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="1eb28-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="1eb28-117">Cell index:</span></span>  <br/> |<span data-ttu-id="1eb28-118">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="1eb28-118">**visXFormLocPinX**</span></span> <br/> |
   

