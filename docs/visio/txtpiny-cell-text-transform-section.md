---
title: Celda TxtPinY (Sección de transformación de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1045
localization_priority: Normal
ms.assetid: 88ddf4b5-8248-8c1a-c387-09a607639d26
description: 'Determina la coordenada y del centro de rotación del bloque de texto en relación con el origen de la forma. La fórmula predeterminada es:'
ms.openlocfilehash: fc62ac76aa24a698d956690df6e5d1e7cff3fb5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316425"
---
# <a name="txtpiny-cell-text-transform-section"></a><span data-ttu-id="2c760-104">Celda TxtPinY (Sección de transformación de texto)</span><span class="sxs-lookup"><span data-stu-id="2c760-104">TxtPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="2c760-105">Determina la coordenada *y* del centro de rotación del bloque de texto en relación con el origen de la forma.</span><span class="sxs-lookup"><span data-stu-id="2c760-105">Determines the  *y*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="2c760-106">La fórmula predeterminada es:</span><span class="sxs-lookup"><span data-stu-id="2c760-106">The default formula is:</span></span> 
  
<span data-ttu-id="2c760-107">= Altura \* 0,5</span><span class="sxs-lookup"><span data-stu-id="2c760-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2c760-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2c760-108">Remarks</span></span>

<span data-ttu-id="2c760-109">Para obtener una referencia a la celda TxtPinY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="2c760-109">To get a reference to the TxtPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2c760-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="2c760-110">Cell name:</span></span>  <br/> | <span data-ttu-id="2c760-111">TxtPinY</span><span class="sxs-lookup"><span data-stu-id="2c760-111">TxtPinY</span></span>  <br/> |
   
<span data-ttu-id="2c760-112">Para obtener una referencia desde un programa a la celda TxtPinY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2c760-112">To get a reference to the TxtPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2c760-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="2c760-113">Section index:</span></span>  <br/> |<span data-ttu-id="2c760-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2c760-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2c760-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="2c760-115">Row index:</span></span>  <br/> |<span data-ttu-id="2c760-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="2c760-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="2c760-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="2c760-117">Cell index:</span></span>  <br/> |<span data-ttu-id="2c760-118">**visXFormPinY**</span><span class="sxs-lookup"><span data-stu-id="2c760-118">**visXFormPinY**</span></span> <br/> |
   

