---
title: Celda HideForApply (Sección de propiedades de estilo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251698
localization_priority: Normal
ms.assetid: 62d87db9-b8ca-60b6-bf27-5168c718ec96
description: Determina dónde se muestra un estilo en la interfaz Visio usuario de Microsoft.
ms.openlocfilehash: 7b3830488770a66d7be35923e1807dbcdcd1f1c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423247"
---
# <a name="hideforapply-cell-style-properties-section"></a><span data-ttu-id="bd18c-103">Celda HideForApply (Sección de propiedades de estilo)</span><span class="sxs-lookup"><span data-stu-id="bd18c-103">HideForApply Cell (Style Properties Section)</span></span>

<span data-ttu-id="bd18c-104">Determina dónde se muestra un estilo en la interfaz Visio usuario de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bd18c-104">Determines where a style is shown in the Microsoft Visio user interface.</span></span>
  
|<span data-ttu-id="bd18c-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="bd18c-105">**Value**</span></span>|<span data-ttu-id="bd18c-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bd18c-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bd18c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="bd18c-107">TRUE</span></span>  <br/> | <span data-ttu-id="bd18c-108">Muestra el estilo solo en **Explorador de dibujos**.</span><span class="sxs-lookup"><span data-stu-id="bd18c-108">Show the style only in the **Drawing Explorer**.</span></span>  <br/> |
| <span data-ttu-id="bd18c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="bd18c-109">FALSE</span></span>  <br/> | <span data-ttu-id="bd18c-110">Muestra el estilo en **Explorador de dibujos**.</span><span class="sxs-lookup"><span data-stu-id="bd18c-110">Show the style in the **Drawing Explorer**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd18c-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bd18c-111">Remarks</span></span>

<span data-ttu-id="bd18c-112">Si basa un estilo nuevo en un estilo oculto, el nuevo estilo no heredará dicho atributo.</span><span class="sxs-lookup"><span data-stu-id="bd18c-112">When you base a new style on a style that is hidden, the new style does not inherit this attribute.</span></span>
  
<span data-ttu-id="bd18c-113">Para obtener una referencia a la celda HideForApply por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="bd18c-113">To get a reference to the HideForApply cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd18c-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="bd18c-114">Cell name:</span></span>  <br/> | <span data-ttu-id="bd18c-115">HideForApply</span><span class="sxs-lookup"><span data-stu-id="bd18c-115">HideForApply</span></span>  <br/> |
   
<span data-ttu-id="bd18c-116">Para obtener una referencia desde un programa a la celda HideForApply por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="bd18c-116">To get a reference to the HideForApply cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd18c-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="bd18c-117">Section index:</span></span>  <br/> |<span data-ttu-id="bd18c-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bd18c-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bd18c-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="bd18c-119">Row index:</span></span>  <br/> |<span data-ttu-id="bd18c-120">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="bd18c-120">**visRowStyle**</span></span> <br/> |
| <span data-ttu-id="bd18c-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="bd18c-121">Cell index:</span></span>  <br/> |<span data-ttu-id="bd18c-122">**visStyleHidden**</span><span class="sxs-lookup"><span data-stu-id="bd18c-122">**visStyleHidden**</span></span> <br/> |
   

