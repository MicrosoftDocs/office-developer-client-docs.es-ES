---
title: Celda DocLockDuplicatePage (Sección de propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Determina si las páginas del documento se pueden duplicar, como un valor booleano.
ms.openlocfilehash: 3f3274c6cfadb81ef514a179279bdaed3543b654
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439663"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a><span data-ttu-id="40f55-103">Celda DocLockDuplicatePage (Sección de propiedades del documento)</span><span class="sxs-lookup"><span data-stu-id="40f55-103">DocLockDuplicatePage Cell (Document Properties Section)</span></span>

<span data-ttu-id="40f55-104">Determina si las páginas del documento se pueden duplicar, como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="40f55-104">Determines whether pages in the document can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40f55-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="40f55-105">TRUE</span></span>  <br/> |<span data-ttu-id="40f55-106">**Los duplicados** en el menú contextual de la página y el método de automatización **Page.Duplicate** están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="40f55-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled.</span></span>  <br/> |
|<span data-ttu-id="40f55-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="40f55-107">FALSE</span></span>  <br/> |<span data-ttu-id="40f55-108">La página se puede duplicar.</span><span class="sxs-lookup"><span data-stu-id="40f55-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40f55-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="40f55-109">Remarks</span></span>

<span data-ttu-id="40f55-110">Para obtener una referencia a la celda **DocLockDuplicatePage** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** o desde un programa mediante la propiedad **CellsU,** utilice:</span><span class="sxs-lookup"><span data-stu-id="40f55-110">To get a reference to the **DocLockDuplicatePage** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="40f55-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="40f55-111">Cell name:</span></span>  <br/> | <span data-ttu-id="40f55-112">DocLockDuplicatePage</span><span class="sxs-lookup"><span data-stu-id="40f55-112">DocLockDuplicatePage</span></span>  <br/> |
   
<span data-ttu-id="40f55-113">Para obtener una referencia desde un programa a la celda **DocLockDuplicatePage** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="40f55-113">To get a reference to the **DocLockDuplicatePage** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="40f55-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="40f55-114">Section index:</span></span>  <br/> |<span data-ttu-id="40f55-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="40f55-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="40f55-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="40f55-116">Row index:</span></span>  <br/> |<span data-ttu-id="40f55-117">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="40f55-117">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="40f55-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="40f55-118">Cell index:</span></span>  <br/> |<span data-ttu-id="40f55-119">**visDocLockDuplicatePage**</span><span class="sxs-lookup"><span data-stu-id="40f55-119">**visDocLockDuplicatePage**</span></span> <br/> |
   

