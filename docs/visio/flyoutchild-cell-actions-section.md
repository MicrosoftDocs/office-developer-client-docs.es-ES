---
title: Celda FlyoutChild (sección Acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80003
localization_priority: Normal
ms.assetid: b2405457-843c-0d46-5f4f-9c413826c3f1
description: Determina si la fila es un menú emergente secundario de la última fila por encima de ella que no es un elemento secundario emergente.
ms.openlocfilehash: 85524ea33258449f5c9ee0991ac9a64f8f0eebae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420867"
---
# <a name="flyoutchild-cell-actions-section"></a><span data-ttu-id="4452a-103">Celda FlyoutChild (sección Acciones)</span><span class="sxs-lookup"><span data-stu-id="4452a-103">FlyoutChild Cell (Actions Section)</span></span>

<span data-ttu-id="4452a-104">Determina si la fila es un menú emergente secundario de la última fila por encima de ella que no es un elemento secundario emergente.</span><span class="sxs-lookup"><span data-stu-id="4452a-104">Determines whether the row is a child flyout menu of the last row above it that is not a flyout child.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4452a-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4452a-105">Remarks</span></span>

<span data-ttu-id="4452a-106">Para obtener una referencia desde otra fórmula a la celda FlyoutChild por su nombre, o desde un programa mediante la propiedad **CellsU**, use lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="4452a-106">To get a reference to the FlyoutChild cell by name from another formula, or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4452a-107">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="4452a-107">Cell name:</span></span>  <br/> |<span data-ttu-id="4452a-108">Acciones.</span><span class="sxs-lookup"><span data-stu-id="4452a-108">Actions.</span></span> <span data-ttu-id="4452a-109">*nombre*  . FlyoutChildwhere Actions.</span><span class="sxs-lookup"><span data-stu-id="4452a-109">*name*  .FlyoutChildwhere Actions.</span></span>  <span data-ttu-id="4452a-110">*es*  el nombre de la fila Actions</span><span class="sxs-lookup"><span data-stu-id="4452a-110">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="4452a-111">Para obtener una referencia desde un programa a la celda FlyoutChild por su índice, use la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4452a-111">To get a reference to the FlyoutChild cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4452a-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="4452a-112">Section index:</span></span>  <br/> |<span data-ttu-id="4452a-113">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="4452a-113">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="4452a-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="4452a-114">Row index:</span></span>  <br/> |<span data-ttu-id="4452a-115">**visRowAction**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4452a-115">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="4452a-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="4452a-116">Cell index:</span></span>  <br/> |<span data-ttu-id="4452a-117">**visActionFlyoutChild**</span><span class="sxs-lookup"><span data-stu-id="4452a-117">**visActionFlyoutChild**</span></span> <br/> |
   

