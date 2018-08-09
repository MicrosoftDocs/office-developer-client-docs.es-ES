---
title: Celda DocLockDuplicatePage (sección Propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Determina si se pueden duplicar las páginas del documento, como un valor Boolean.
ms.openlocfilehash: 97bca23a7dc9150f66eb0c87834fca72c215448b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822001"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a><span data-ttu-id="fb22e-103">Celda DocLockDuplicatePage (sección Propiedades del documento)</span><span class="sxs-lookup"><span data-stu-id="fb22e-103">DocLockDuplicatePage Cell (Document Properties Section)</span></span>

<span data-ttu-id="fb22e-104">Determina si se pueden duplicar las páginas del documento, como un valor Boolean.</span><span class="sxs-lookup"><span data-stu-id="fb22e-104">Determines whether pages in the document can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fb22e-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="fb22e-105">TRUE</span></span>  <br/> |<span data-ttu-id="fb22e-106">**Duplicar** en el menú contextual de la página y el método de automatización **Page.Duplicate** están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="fb22e-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled.</span></span>  <br/> |
|<span data-ttu-id="fb22e-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="fb22e-107">FALSE</span></span>  <br/> |<span data-ttu-id="fb22e-108">Puede duplicar la página.</span><span class="sxs-lookup"><span data-stu-id="fb22e-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb22e-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fb22e-109">Remarks</span></span>

<span data-ttu-id="fb22e-110">Para obtener una referencia a la celda **DocLockDuplicatePage** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="fb22e-110">To get a reference to the **DocLockDuplicatePage** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fb22e-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="fb22e-111">Cell name:</span></span>  <br/> | <span data-ttu-id="fb22e-112">DocLockDuplicatePage</span><span class="sxs-lookup"><span data-stu-id="fb22e-112">DocLockDuplicatePage</span></span>  <br/> |
   
<span data-ttu-id="fb22e-113">Para obtener una referencia a la celda **DocLockDuplicatePage** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="fb22e-113">To get a reference to the **DocLockDuplicatePage** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fb22e-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="fb22e-114">Section index:</span></span>  <br/> |<span data-ttu-id="fb22e-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fb22e-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fb22e-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="fb22e-116">Row index:</span></span>  <br/> |<span data-ttu-id="fb22e-117">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="fb22e-117">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="fb22e-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="fb22e-118">Cell index:</span></span>  <br/> |<span data-ttu-id="fb22e-119">**visDocLockDuplicatePage**</span><span class="sxs-lookup"><span data-stu-id="fb22e-119">**visDocLockDuplicatePage**</span></span> <br/> |
   

