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
description: Representa la coordenada x que indica la ubicación del controlador de una forma en coordenadas locales.
ms.openlocfilehash: 58eea4e9c3cfe127c4adcc7fb75e395f53874dd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406454"
---
# <a name="x-cell-controls-section"></a><span data-ttu-id="7ce79-103">Celda X (Sección de controles)</span><span class="sxs-lookup"><span data-stu-id="7ce79-103">X Cell (Controls Section)</span></span>

<span data-ttu-id="7ce79-104">Representa la coordenada *x* que indica la ubicación del controlador de una forma en coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="7ce79-104">Represents the  *x*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7ce79-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7ce79-105">Remarks</span></span>

<span data-ttu-id="7ce79-106">Para obtener una referencia a la celda X por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="7ce79-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7ce79-107">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="7ce79-107">Cell name:</span></span>  <br/> | <span data-ttu-id="7ce79-108">Mando.</span><span class="sxs-lookup"><span data-stu-id="7ce79-108">Controls.</span></span>  <span data-ttu-id="7ce79-109">*nombre* . X donde controles.</span><span class="sxs-lookup"><span data-stu-id="7ce79-109">*name*  .X where Controls.</span></span>  <span data-ttu-id="7ce79-110">*nombre* es el nombre de la fila de controles.</span><span class="sxs-lookup"><span data-stu-id="7ce79-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="7ce79-111">Para obtener una referencia desde un programa a la celda X por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7ce79-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7ce79-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="7ce79-112">Section index:</span></span>  <br/> |<span data-ttu-id="7ce79-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="7ce79-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="7ce79-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="7ce79-114">Row index:</span></span>  <br/> |<span data-ttu-id="7ce79-115">**visRowControl** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7ce79-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7ce79-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="7ce79-116">Cell index:</span></span>  <br/> |<span data-ttu-id="7ce79-117">**visCtlX**</span><span class="sxs-lookup"><span data-stu-id="7ce79-117">**visCtlX**</span></span> <br/> |
   

