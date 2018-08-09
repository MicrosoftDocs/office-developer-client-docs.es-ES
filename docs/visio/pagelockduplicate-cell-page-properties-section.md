---
title: Celda PageLockDuplicate (sección Propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Determina si se puede duplicar la página, como un valor Boolean.
ms.openlocfilehash: 6cfe8f7a33942f51130ef103b8aba70a5c38b37d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822712"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a><span data-ttu-id="ad49b-103">Celda PageLockDuplicate (sección Propiedades de página)</span><span class="sxs-lookup"><span data-stu-id="ad49b-103">PageLockDuplicate Cell (Page Properties Section)</span></span>

<span data-ttu-id="ad49b-104">Determina si se puede duplicar la página, como un valor Boolean.</span><span class="sxs-lookup"><span data-stu-id="ad49b-104">Determines whether the page can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ad49b-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="ad49b-105">TRUE</span></span>  <br/> |<span data-ttu-id="ad49b-106">**Duplicar** en el menú contextual de la página y el método de automatización **Page.Duplicate** están deshabilitados para la página.</span><span class="sxs-lookup"><span data-stu-id="ad49b-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled for the page.</span></span>  <br/> |
|<span data-ttu-id="ad49b-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="ad49b-107">FALSE</span></span>  <br/> |<span data-ttu-id="ad49b-108">Puede duplicar la página.</span><span class="sxs-lookup"><span data-stu-id="ad49b-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad49b-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ad49b-109">Remarks</span></span>

<span data-ttu-id="ad49b-110">Para obtener una referencia a la celda **PageLockDuplicate** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="ad49b-110">To get a reference to the **PageLockDuplicate** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ad49b-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="ad49b-111">Cell name:</span></span>  <br/> | <span data-ttu-id="ad49b-112">PageLockDuplicate</span><span class="sxs-lookup"><span data-stu-id="ad49b-112">PageLockDuplicate</span></span>  <br/> |
   
<span data-ttu-id="ad49b-113">Para obtener una referencia a la celda **PageLockDuplicate** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ad49b-113">To get a reference to the **PageLockDuplicate** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ad49b-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="ad49b-114">Section index:</span></span>  <br/> |<span data-ttu-id="ad49b-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ad49b-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ad49b-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="ad49b-116">Row index:</span></span>  <br/> |<span data-ttu-id="ad49b-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="ad49b-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="ad49b-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="ad49b-118">Cell index:</span></span>  <br/> |<span data-ttu-id="ad49b-119">**visPageLockDuplicate**</span><span class="sxs-lookup"><span data-stu-id="ad49b-119">**visPageLockDuplicate**</span></span> <br/> |
   

