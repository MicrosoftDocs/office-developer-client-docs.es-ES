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
description: Determina donde se muestra un estilo en la interfaz de usuario de Microsoft Visio.
ms.openlocfilehash: 5b0221c54c17a3b9957cce5e890842def0ba7525
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822295"
---
# <a name="hideforapply-cell-style-properties-section"></a><span data-ttu-id="ae987-103">Celda HideForApply (sección de propiedades de estilo)</span><span class="sxs-lookup"><span data-stu-id="ae987-103">HideForApply Cell (Style Properties Section)</span></span>

<span data-ttu-id="ae987-104">Determina donde se muestra un estilo en la interfaz de usuario de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="ae987-104">Determines where a style is shown in the Microsoft Visio user interface.</span></span>
  
|<span data-ttu-id="ae987-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ae987-105">**Value**</span></span>|<span data-ttu-id="ae987-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae987-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ae987-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ae987-107">TRUE</span></span>  <br/> | <span data-ttu-id="ae987-108">
          Muestra el estilo solo en **Explorador de dibujos**.
</span><span class="sxs-lookup"><span data-stu-id="ae987-108">Show the style only in the **Drawing Explorer**.</span></span>  <br/> |
| <span data-ttu-id="ae987-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ae987-109">FALSE</span></span>  <br/> | <span data-ttu-id="ae987-110">
          Muestra el estilo en **Explorador de dibujos**.
</span><span class="sxs-lookup"><span data-stu-id="ae987-110">Show the style in the **Drawing Explorer**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae987-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ae987-111">Remarks</span></span>

<span data-ttu-id="ae987-112">Si basa un estilo nuevo en un estilo oculto, el nuevo estilo no heredará dicho atributo.</span><span class="sxs-lookup"><span data-stu-id="ae987-112">When you base a new style on a style that is hidden, the new style does not inherit this attribute.</span></span>
  
<span data-ttu-id="ae987-113">Para obtener una referencia a la celda HideForApply por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="ae987-113">To get a reference to the HideForApply cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ae987-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="ae987-114">Cell name:</span></span>  <br/> | <span data-ttu-id="ae987-115">HideForApply</span><span class="sxs-lookup"><span data-stu-id="ae987-115">HideForApply</span></span>  <br/> |
   
<span data-ttu-id="ae987-116">Para obtener una referencia desde un programa a la celda HideForApply por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ae987-116">To get a reference to the HideForApply cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ae987-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="ae987-117">Section index:</span></span>  <br/> |<span data-ttu-id="ae987-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ae987-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ae987-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="ae987-119">Row index:</span></span>  <br/> |<span data-ttu-id="ae987-120">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="ae987-120">**visRowStyle**</span></span> <br/> |
| <span data-ttu-id="ae987-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="ae987-121">Cell index:</span></span>  <br/> |<span data-ttu-id="ae987-122">**visStyleHidden**</span><span class="sxs-lookup"><span data-stu-id="ae987-122">**visStyleHidden**</span></span> <br/> |
   

