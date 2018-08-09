---
title: Celda X (Sección de puntos de conexión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251746
localization_priority: Normal
ms.assetid: 11c69600-4e1f-4c52-ff35-b6a7cc6c734c
description: Representa la x-coordenadas de un punto de conexión en coordenadas locales.
ms.openlocfilehash: 27821f9aa94f97d8e019d7c7307c036549bf807b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823559"
---
# <a name="x-cell-connection-points-section"></a><span data-ttu-id="5145e-103">Celda X (sección Puntos de conexión)</span><span class="sxs-lookup"><span data-stu-id="5145e-103">X Cell (Connection Points Section)</span></span>

<span data-ttu-id="5145e-104">Representa la *x* -coordenadas de un punto de conexión en coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="5145e-104">Represents the  *x*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5145e-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5145e-105">Remarks</span></span>

<span data-ttu-id="5145e-106">Para obtener una referencia a la celda X por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="5145e-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5145e-107">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="5145e-107">Cell name:</span></span>  <br/> | <span data-ttu-id="5145e-108">Propiedad *i* donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="5145e-108">Connections.X  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5145e-109">Para obtener una referencia desde un programa a la celda X por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5145e-109">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5145e-110">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="5145e-110">Section index:</span></span>  <br/> |<span data-ttu-id="5145e-111">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="5145e-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="5145e-112">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="5145e-112">Row index:</span></span>  <br/> |<span data-ttu-id="5145e-113">**visRowConnectionPts** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5145e-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5145e-114">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="5145e-114">Cell index:</span></span>  <br/> |<span data-ttu-id="5145e-115">**visX**</span><span class="sxs-lookup"><span data-stu-id="5145e-115">**visX**</span></span> <br/> |
   

