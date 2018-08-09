---
title: Celda X (Sección de controles)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251281
localization_priority: Normal
ms.assetid: b7aea554-f491-6a9a-4d07-feeab739a9df
description: Representa la x-coordenada que indica la ubicación del controlador de una forma en coordenadas locales.
ms.openlocfilehash: e47b26c72709a2ee74675e73b8e8424bbfb325e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823564"
---
# <a name="x-cell-controls-section"></a><span data-ttu-id="60764-103">Celda X (sección Controles)</span><span class="sxs-lookup"><span data-stu-id="60764-103">X Cell (Controls Section)</span></span>

<span data-ttu-id="60764-104">Representa la *x* -coordenada que indica la ubicación del controlador de una forma en coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="60764-104">Represents the  *x*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="60764-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="60764-105">Remarks</span></span>

<span data-ttu-id="60764-106">Para obtener una referencia a la celda X por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="60764-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="60764-107">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="60764-107">Cell name:</span></span>  <br/> | <span data-ttu-id="60764-108">Controles.</span><span class="sxs-lookup"><span data-stu-id="60764-108">Controls.</span></span>  <span data-ttu-id="60764-109">*nombre* . X donde controla.</span><span class="sxs-lookup"><span data-stu-id="60764-109">*name*  .X where Controls.</span></span>  <span data-ttu-id="60764-110">*nombre* es el nombre de la fila de controles.</span><span class="sxs-lookup"><span data-stu-id="60764-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="60764-111">Para obtener una referencia desde un programa a la celda X por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="60764-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="60764-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="60764-112">Section index:</span></span>  <br/> |<span data-ttu-id="60764-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="60764-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="60764-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="60764-114">Row index:</span></span>  <br/> |<span data-ttu-id="60764-115">**visRowControl** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="60764-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="60764-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="60764-116">Cell index:</span></span>  <br/> |<span data-ttu-id="60764-117">**visCtlX**</span><span class="sxs-lookup"><span data-stu-id="60764-117">**visCtlX**</span></span> <br/> |
   

