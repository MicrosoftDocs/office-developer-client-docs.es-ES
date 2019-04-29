---
title: Celda PageLockDuplicate (sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Determina si la página se puede duplicar, como un valor booleano.
ms.openlocfilehash: 8ce730fcdc2dff5deac44d8c053b84e82a82d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425984"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a><span data-ttu-id="fd3a9-103">Celda PageLockDuplicate (sección de propiedades de página)</span><span class="sxs-lookup"><span data-stu-id="fd3a9-103">PageLockDuplicate Cell (Page Properties Section)</span></span>

<span data-ttu-id="fd3a9-104">Determina si la página se puede duplicar, como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="fd3a9-104">Determines whether the page can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fd3a9-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="fd3a9-105">TRUE</span></span>  <br/> |<span data-ttu-id="fd3a9-106">**Duplicar** en el menú contextual de la página y el método de automatización **Page. duplicado** están deshabilitados para la página.</span><span class="sxs-lookup"><span data-stu-id="fd3a9-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled for the page.</span></span>  <br/> |
|<span data-ttu-id="fd3a9-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="fd3a9-107">FALSE</span></span>  <br/> |<span data-ttu-id="fd3a9-108">La página se puede duplicar.</span><span class="sxs-lookup"><span data-stu-id="fd3a9-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd3a9-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fd3a9-109">Remarks</span></span>

<span data-ttu-id="fd3a9-110">Para obtener una referencia a la celda **PageLockDuplicate** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="fd3a9-110">To get a reference to the **PageLockDuplicate** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fd3a9-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="fd3a9-111">Cell name:</span></span>  <br/> | <span data-ttu-id="fd3a9-112">PageLockDuplicate</span><span class="sxs-lookup"><span data-stu-id="fd3a9-112">PageLockDuplicate</span></span>  <br/> |
   
<span data-ttu-id="fd3a9-113">Para obtener una referencia desde un programa a la celda **PageLockDuplicate** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="fd3a9-113">To get a reference to the **PageLockDuplicate** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fd3a9-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="fd3a9-114">Section index:</span></span>  <br/> |<span data-ttu-id="fd3a9-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fd3a9-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fd3a9-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="fd3a9-116">Row index:</span></span>  <br/> |<span data-ttu-id="fd3a9-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="fd3a9-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="fd3a9-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="fd3a9-118">Cell index:</span></span>  <br/> |<span data-ttu-id="fd3a9-119">**visPageLockDuplicate**</span><span class="sxs-lookup"><span data-stu-id="fd3a9-119">**visPageLockDuplicate**</span></span> <br/> |
   

