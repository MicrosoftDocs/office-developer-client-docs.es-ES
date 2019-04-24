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
description: Representa la coordenada x de un punto de conexión en coordenadas locales.
ms.openlocfilehash: 496e5af6ea5b7ba99730b23dcbb510db6af9b23b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339882"
---
# <a name="x-cell-connection-points-section"></a><span data-ttu-id="3c13c-103">Celda X (Sección de puntos de conexión)</span><span class="sxs-lookup"><span data-stu-id="3c13c-103">X Cell (Connection Points Section)</span></span>

<span data-ttu-id="3c13c-104">Representa la coordenada *x* de un punto de conexión en coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="3c13c-104">Represents the  *x*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3c13c-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3c13c-105">Remarks</span></span>

<span data-ttu-id="3c13c-106">Para obtener una referencia a la celda X por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="3c13c-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3c13c-107">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="3c13c-107">Cell name:</span></span>  <br/> | <span data-ttu-id="3c13c-108">Connections. X *i* donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="3c13c-108">Connections.X  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="3c13c-109">Para obtener una referencia desde un programa a la celda X por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3c13c-109">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3c13c-110">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="3c13c-110">Section index:</span></span>  <br/> |<span data-ttu-id="3c13c-111">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="3c13c-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="3c13c-112">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="3c13c-112">Row index:</span></span>  <br/> |<span data-ttu-id="3c13c-113">**visRowConnectionPts** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3c13c-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3c13c-114">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="3c13c-114">Cell index:</span></span>  <br/> |<span data-ttu-id="3c13c-115">**visX**</span><span class="sxs-lookup"><span data-stu-id="3c13c-115">**visX**</span></span> <br/> |
   

