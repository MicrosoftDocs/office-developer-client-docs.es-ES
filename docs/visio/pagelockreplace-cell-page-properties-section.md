---
title: Celda PageLockReplace (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Indica si se debe deshabilitar el botón Reemplazar forma para esta página.
ms.openlocfilehash: c0495d47a81ed7a23e758c531f7d754291c47852
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433104"
---
# <a name="pagelockreplace-cell-page-properties-section"></a><span data-ttu-id="5c58a-103">Celda PageLockReplace (Sección de propiedades de página)</span><span class="sxs-lookup"><span data-stu-id="5c58a-103">PageLockReplace Cell (Page Properties Section)</span></span>

<span data-ttu-id="5c58a-104">Indica si se debe deshabilitar **el** botón Reemplazar forma para esta página.</span><span class="sxs-lookup"><span data-stu-id="5c58a-104">Indicates whether the **Replace Shape** button should be disabled for this page.</span></span> 
  
|<span data-ttu-id="5c58a-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5c58a-105">**Value**</span></span>|<span data-ttu-id="5c58a-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5c58a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c58a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="5c58a-107">TRUE</span></span>  <br/> |<span data-ttu-id="5c58a-108">El **botón Cambiar forma** aparece atenuado cuando esta página está activa.</span><span class="sxs-lookup"><span data-stu-id="5c58a-108">The **Change Shape** button is grayed out when this page is active.</span></span>  <br/> |
|<span data-ttu-id="5c58a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="5c58a-109">FALSE</span></span>  <br/> |<span data-ttu-id="5c58a-110">Esta **página no** deshabilita el botón Cambiar forma.</span><span class="sxs-lookup"><span data-stu-id="5c58a-110">The **Change Shape** button is not disabled by this page.</span></span> <span data-ttu-id="5c58a-111">Es posible que el botón aún esté atenuado si: **DocLockReplace** en **documentSheet** está establecido en **TRUE**; la **celda LockReplace** de la forma seleccionada se establece en **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="5c58a-111">The button may still be grayed out if: the **DocLockReplace** on the **DocumentSheet** is set to **TRUE**; the **LockReplace** cell for the selected shape is set to **TRUE**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c58a-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5c58a-112">Remarks</span></span>

<span data-ttu-id="5c58a-113">Para obtener una referencia a la celda **PageLockReplace** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell,** o desde un programa mediante la propiedad **CellsU,** utilice:</span><span class="sxs-lookup"><span data-stu-id="5c58a-113">To get a reference to the **PageLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5c58a-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="5c58a-114">Cell name:</span></span>  <br/> | <span data-ttu-id="5c58a-115">PageLockReplace</span><span class="sxs-lookup"><span data-stu-id="5c58a-115">PageLockReplace</span></span>  <br/> |
   
<span data-ttu-id="5c58a-116">Para obtener una referencia desde un programa a la celda **PageLockReplace** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5c58a-116">To get a reference to the **PageLockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5c58a-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="5c58a-117">Section index:</span></span>  <br/> |<span data-ttu-id="5c58a-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5c58a-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5c58a-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="5c58a-119">Row index:</span></span>  <br/> |<span data-ttu-id="5c58a-120">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="5c58a-120">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="5c58a-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="5c58a-121">Cell index:</span></span>  <br/> |<span data-ttu-id="5c58a-122">**visPageLockReplace**</span><span class="sxs-lookup"><span data-stu-id="5c58a-122">**visPageLockReplace**</span></span> <br/> |
   

