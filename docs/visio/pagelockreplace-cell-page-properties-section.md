---
title: Celda PageLockReplace (sección Propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Indica si se debe deshabilitar el botón Reemplazar forma para esta página.
ms.openlocfilehash: b3956b3e2f2fcd5c4f82089e08a6e32200374778
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822718"
---
# <a name="pagelockreplace-cell-page-properties-section"></a><span data-ttu-id="689dc-103">Celda PageLockReplace (sección Propiedades de página)</span><span class="sxs-lookup"><span data-stu-id="689dc-103">PageLockReplace Cell (Page Properties Section)</span></span>

<span data-ttu-id="689dc-104">Indica si se debe deshabilitar el botón **Reemplazar forma** para esta página.</span><span class="sxs-lookup"><span data-stu-id="689dc-104">Indicates whether the **Replace Shape** button should be disabled for this page.</span></span> 
  
|<span data-ttu-id="689dc-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="689dc-105">**Value**</span></span>|<span data-ttu-id="689dc-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="689dc-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="689dc-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="689dc-107">TRUE</span></span>  <br/> |<span data-ttu-id="689dc-108">El botón **Cambiar forma** está atenuado cuando esta página está activa.</span><span class="sxs-lookup"><span data-stu-id="689dc-108">The **Change Shape** button is grayed out when this page is active.</span></span>  <br/> |
|<span data-ttu-id="689dc-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="689dc-109">FALSE</span></span>  <br/> |<span data-ttu-id="689dc-110">El botón **Cambiar forma** no está deshabilitado por esta página.</span><span class="sxs-lookup"><span data-stu-id="689dc-110">The **Change Shape** button is not disabled by this page.</span></span> <span data-ttu-id="689dc-111">El botón es posible que aún se atenuada if: el **DocLockReplace** en el **DocumentSheet** está establecida en **TRUE**; la celda **LockReplace** para la forma seleccionada se establece en **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="689dc-111">The button may still be grayed out if: the **DocLockReplace** on the **DocumentSheet** is set to **TRUE**; the **LockReplace** cell for the selected shape is set to **TRUE**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="689dc-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="689dc-112">Remarks</span></span>

<span data-ttu-id="689dc-113">Para obtener una referencia a la celda **PageLockReplace** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="689dc-113">To get a reference to the **PageLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="689dc-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="689dc-114">Cell name:</span></span>  <br/> | <span data-ttu-id="689dc-115">PageLockReplace</span><span class="sxs-lookup"><span data-stu-id="689dc-115">PageLockReplace</span></span>  <br/> |
   
<span data-ttu-id="689dc-116">Para obtener una referencia a la celda **PageLockReplace** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="689dc-116">To get a reference to the **PageLockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="689dc-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="689dc-117">Section index:</span></span>  <br/> |<span data-ttu-id="689dc-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="689dc-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="689dc-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="689dc-119">Row index:</span></span>  <br/> |<span data-ttu-id="689dc-120">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="689dc-120">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="689dc-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="689dc-121">Cell index:</span></span>  <br/> |<span data-ttu-id="689dc-122">**visPageLockReplace**</span><span class="sxs-lookup"><span data-stu-id="689dc-122">**visPageLockReplace**</span></span> <br/> |
   

