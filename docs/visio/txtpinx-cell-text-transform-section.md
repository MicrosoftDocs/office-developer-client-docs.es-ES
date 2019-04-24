---
title: Celda TxtPinX (Sección de transformación de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
localization_priority: Normal
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: 'Determina la coordenada x del centro de rotación del bloque de texto en relación con el origen de la forma. La fórmula predeterminada es:'
ms.openlocfilehash: 836f5c807d0c0e53efc825f62f60429274282165
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282302"
---
# <a name="txtpinx-cell-text-transform-section"></a><span data-ttu-id="9e324-104">Celda TxtPinX (Sección de transformación de texto)</span><span class="sxs-lookup"><span data-stu-id="9e324-104">TxtPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="9e324-105">Determina la coordenada *x* del centro de rotación del bloque de texto en relación con el origen de la forma.</span><span class="sxs-lookup"><span data-stu-id="9e324-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="9e324-106">La fórmula predeterminada es:</span><span class="sxs-lookup"><span data-stu-id="9e324-106">The default formula is:</span></span> 
  
<span data-ttu-id="9e324-107">= Ancho \* 0,5</span><span class="sxs-lookup"><span data-stu-id="9e324-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9e324-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9e324-108">Remarks</span></span>

<span data-ttu-id="9e324-109">Para obtener una referencia a la celda TxtPinX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="9e324-109">To get a reference to the TxtPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9e324-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="9e324-110">Cell name:</span></span>  <br/> | <span data-ttu-id="9e324-111">TxtPinX</span><span class="sxs-lookup"><span data-stu-id="9e324-111">TxtPinX</span></span>  <br/> |
   
<span data-ttu-id="9e324-112">Para obtener una referencia desde un programa a la celda TxtPinX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9e324-112">To get a reference to the TxtPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9e324-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="9e324-113">Section index:</span></span>  <br/> |<span data-ttu-id="9e324-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9e324-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9e324-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="9e324-115">Row index:</span></span>  <br/> |<span data-ttu-id="9e324-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="9e324-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="9e324-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="9e324-117">Cell index:</span></span>  <br/> |<span data-ttu-id="9e324-118">**visXFormPinX**</span><span class="sxs-lookup"><span data-stu-id="9e324-118">**visXFormPinX**</span></span> <br/> |
   

