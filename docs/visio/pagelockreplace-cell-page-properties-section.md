---
title: Celda PageLockReplace (sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Indica si el botón reemplazar forma debe estar deshabilitado para esta página.
ms.openlocfilehash: c0495d47a81ed7a23e758c531f7d754291c47852
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339483"
---
# <a name="pagelockreplace-cell-page-properties-section"></a><span data-ttu-id="590ec-103">Celda PageLockReplace (sección de propiedades de página)</span><span class="sxs-lookup"><span data-stu-id="590ec-103">PageLockReplace Cell (Page Properties Section)</span></span>

<span data-ttu-id="590ec-104">Indica si el botón **reemplazar forma** debe estar deshabilitado para esta página.</span><span class="sxs-lookup"><span data-stu-id="590ec-104">Indicates whether the **Replace Shape** button should be disabled for this page.</span></span> 
  
|<span data-ttu-id="590ec-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="590ec-105">**Value**</span></span>|<span data-ttu-id="590ec-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="590ec-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="590ec-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="590ec-107">TRUE</span></span>  <br/> |<span data-ttu-id="590ec-108">El botón **Cambiar forma** aparece atenuado cuando esta página está activa.</span><span class="sxs-lookup"><span data-stu-id="590ec-108">The **Change Shape** button is grayed out when this page is active.</span></span>  <br/> |
|<span data-ttu-id="590ec-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="590ec-109">FALSE</span></span>  <br/> |<span data-ttu-id="590ec-110">Esta página no ha deshabilitado el botón **Cambiar forma** .</span><span class="sxs-lookup"><span data-stu-id="590ec-110">The **Change Shape** button is not disabled by this page.</span></span> <span data-ttu-id="590ec-111">El botón todavía puede estar atenuado si: el **DocLockReplace** en **DocumentSheet** se establece en **true**; la celda **LockReplace** de la forma seleccionada se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="590ec-111">The button may still be grayed out if: the **DocLockReplace** on the **DocumentSheet** is set to **TRUE**; the **LockReplace** cell for the selected shape is set to **TRUE**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="590ec-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="590ec-112">Remarks</span></span>

<span data-ttu-id="590ec-113">Para obtener una referencia a la celda **PageLockReplace** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="590ec-113">To get a reference to the **PageLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="590ec-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="590ec-114">Cell name:</span></span>  <br/> | <span data-ttu-id="590ec-115">PageLockReplace</span><span class="sxs-lookup"><span data-stu-id="590ec-115">PageLockReplace</span></span>  <br/> |
   
<span data-ttu-id="590ec-116">Para obtener una referencia desde un programa a la celda **PageLockReplace** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="590ec-116">To get a reference to the **PageLockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="590ec-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="590ec-117">Section index:</span></span>  <br/> |<span data-ttu-id="590ec-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="590ec-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="590ec-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="590ec-119">Row index:</span></span>  <br/> |<span data-ttu-id="590ec-120">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="590ec-120">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="590ec-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="590ec-121">Cell index:</span></span>  <br/> |<span data-ttu-id="590ec-122">**visPageLockReplace**</span><span class="sxs-lookup"><span data-stu-id="590ec-122">**visPageLockReplace**</span></span> <br/> |
   

