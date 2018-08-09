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
ms.openlocfilehash: 8a41721f91fa9632246e512cfd4ba1a2d871ece5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822161"
---
# <a name="flyoutchild-cell-actions-section"></a><span data-ttu-id="7b530-103">Celda FlyoutChild (sección Acciones)</span><span class="sxs-lookup"><span data-stu-id="7b530-103">FlyoutChild Cell (Actions Section)</span></span>

<span data-ttu-id="7b530-104">Determina si la fila es un menú emergente secundario de la última fila por encima de ella que no es un elemento secundario emergente.</span><span class="sxs-lookup"><span data-stu-id="7b530-104">Determines whether the row is a child flyout menu of the last row above it that is not a flyout child.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7b530-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7b530-105">Remarks</span></span>

<span data-ttu-id="7b530-106">Para obtener una referencia desde otra fórmula a la celda FlyoutChild por su nombre, o desde un programa mediante la propiedad **CellsU**, use lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="7b530-106">To get a reference to the FlyoutChild cell by name from another formula, or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b530-107">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="7b530-107">Cell name:</span></span>  <br/> |<span data-ttu-id="7b530-108">Acciones.</span><span class="sxs-lookup"><span data-stu-id="7b530-108">Actions.</span></span> <span data-ttu-id="7b530-109">*nombre* . Acciones de FlyoutChildwhere.</span><span class="sxs-lookup"><span data-stu-id="7b530-109">*name*  .FlyoutChildwhere Actions.</span></span>  <span data-ttu-id="7b530-110">*nombre* es el nombre de la fila de acciones</span><span class="sxs-lookup"><span data-stu-id="7b530-110">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="7b530-111">Para obtener una referencia desde un programa a la celda FlyoutChild por su índice, use la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7b530-111">To get a reference to the FlyoutChild cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b530-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="7b530-112">Section index:</span></span>  <br/> |<span data-ttu-id="7b530-113">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="7b530-113">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="7b530-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="7b530-114">Row index:</span></span>  <br/> |<span data-ttu-id="7b530-115">**visRowAction** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7b530-115">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="7b530-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="7b530-116">Cell index:</span></span>  <br/> |<span data-ttu-id="7b530-117">**visActionFlyoutChild**</span><span class="sxs-lookup"><span data-stu-id="7b530-117">**visActionFlyoutChild**</span></span> <br/> |
   

