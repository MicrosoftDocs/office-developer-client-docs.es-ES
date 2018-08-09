---
title: Celda LocPinY (Sección de transformación de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm685
localization_priority: Normal
ms.assetid: a29c5d4e-d3d6-d984-495a-4b0b130352ef
description: 'Representa la y-coordenadas del eje de la forma (centro de rotación) en relación con el origen de la forma. La fórmula predeterminada para determinar LocPinY es:'
ms.openlocfilehash: 8d98906e8082af0fc54bc01fe3a8537b66ac56b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822543"
---
# <a name="locpiny-cell-shape-transform-section"></a><span data-ttu-id="bfbea-104">Celda LocPinY (sección Transformación de forma)</span><span class="sxs-lookup"><span data-stu-id="bfbea-104">LocPinY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="bfbea-105">Representa la *y* -coordenadas del eje de la forma (centro de rotación) en relación con el origen de la forma.</span><span class="sxs-lookup"><span data-stu-id="bfbea-105">Represents the  *y*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="bfbea-106">La fórmula predeterminada para determinar LocPinY es:</span><span class="sxs-lookup"><span data-stu-id="bfbea-106">The default formula for determining LocPinY is:</span></span> 
  
<span data-ttu-id="bfbea-107">= Alto \* 0,5</span><span class="sxs-lookup"><span data-stu-id="bfbea-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bfbea-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bfbea-108">Remarks</span></span>

<span data-ttu-id="bfbea-109">Para obtener una referencia a la celda LocPinY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="bfbea-109">To get a reference to the LocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bfbea-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="bfbea-110">Cell name:</span></span>  <br/> | <span data-ttu-id="bfbea-111">LocPinY</span><span class="sxs-lookup"><span data-stu-id="bfbea-111">LocPinY</span></span>  <br/> |
   
<span data-ttu-id="bfbea-112">Para obtener una referencia desde un programa a la celda LocPinY por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="bfbea-112">To get a reference to the LocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bfbea-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="bfbea-113">Section index:</span></span>  <br/> |<span data-ttu-id="bfbea-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bfbea-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bfbea-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="bfbea-115">Row index:</span></span>  <br/> |<span data-ttu-id="bfbea-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="bfbea-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="bfbea-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="bfbea-117">Cell index:</span></span>  <br/> |<span data-ttu-id="bfbea-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="bfbea-118">**visXFormLocPinY**</span></span> <br/> |
   

