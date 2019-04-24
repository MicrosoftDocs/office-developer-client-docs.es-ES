---
title: Celda ShapeShdwType (Sección de formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033173
localization_priority: Normal
ms.assetid: 1461148d-90a9-6f7c-1b28-9310ffaf0e3b
description: Especifica el tipo de sombra de una forma.
ms.openlocfilehash: 607881e4a520f1376562394c6e40ab5d2508906d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342864"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a><span data-ttu-id="9ea2b-103">Celda ShapeShdwType (Sección de formato de relleno)</span><span class="sxs-lookup"><span data-stu-id="9ea2b-103">ShapeShdwType Cell (Fill Format Section)</span></span>

<span data-ttu-id="9ea2b-104">Especifica el tipo de sombra de una forma.</span><span class="sxs-lookup"><span data-stu-id="9ea2b-104">Specifies the type of shadow for a shape.</span></span> 
  
|<span data-ttu-id="9ea2b-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="9ea2b-105">**Value**</span></span>|<span data-ttu-id="9ea2b-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9ea2b-106">**Description**</span></span>|<span data-ttu-id="9ea2b-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="9ea2b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9ea2b-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="9ea2b-108">0</span></span>  <br/> |<span data-ttu-id="9ea2b-109">Se utilizan las opciones predeterminadas de la página (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="9ea2b-109">Use page default (the default)</span></span>  <br/> |<span data-ttu-id="9ea2b-110">**visFSTPageDefault**</span><span class="sxs-lookup"><span data-stu-id="9ea2b-110">**visFSTPageDefault**</span></span> <br/> |
|<span data-ttu-id="9ea2b-111">1</span><span class="sxs-lookup"><span data-stu-id="9ea2b-111">1</span></span>  <br/> |<span data-ttu-id="9ea2b-112">Simple</span><span class="sxs-lookup"><span data-stu-id="9ea2b-112">Simple</span></span>  <br/> |<span data-ttu-id="9ea2b-113">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="9ea2b-113">**visFSTSimple**</span></span> <br/> |
|<span data-ttu-id="9ea2b-114">segundo</span><span class="sxs-lookup"><span data-stu-id="9ea2b-114">2</span></span>  <br/> |<span data-ttu-id="9ea2b-115">Oblicua</span><span class="sxs-lookup"><span data-stu-id="9ea2b-115">Oblique</span></span>  <br/> |<span data-ttu-id="9ea2b-116">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="9ea2b-116">**visFSTOblique**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ea2b-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9ea2b-117">Remarks</span></span>

<span data-ttu-id="9ea2b-118">Use esta celda para aplicar una sombra de forma diferente de la predeterminada para la página (el tipo de sombra predeterminado de la página se define en la celda ShdwType de la sección Propiedades de página).</span><span class="sxs-lookup"><span data-stu-id="9ea2b-118">Use this cell to apply a shape shadow that is different from the page default (the page default shadow type is defined in the ShdwType cell in the Page Properties Section).</span></span>
  
<span data-ttu-id="9ea2b-119">Las sombras simples se describen en la interfaz de usuario como sombras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="9ea2b-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="9ea2b-120">Una sombra simple proporciona un efecto de sombra sobre un plano paralelo situado detrás de la forma.</span><span class="sxs-lookup"><span data-stu-id="9ea2b-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located behind the shape.</span></span> <span data-ttu-id="9ea2b-121">Las sombras oblicuas se describen en la interfaz de usuario como sombras oblicuas y proporcionan un efecto de sombra que se proyecta sobre un plano perpendicular a la forma.</span><span class="sxs-lookup"><span data-stu-id="9ea2b-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="9ea2b-122">Para obtener una lista de tipos de sombras simples y oblicuas predefinidas, vea el cuadro **Estilo** en el cuadro de diálogo **Sombra** (en la ficha **Inicio**, en el grupo **Forma**, haga clic en **Sombra** y, a continuación, en **Opciones de sombra**).</span><span class="sxs-lookup"><span data-stu-id="9ea2b-122">For a list of predefined simple and oblique shadow types, see the **Style** box in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="9ea2b-123">Para obtener una referencia a la celda ShapeShdwType por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="9ea2b-123">To get a reference to the ShapeShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ea2b-124">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="9ea2b-124">Cell name:</span></span>  <br/> |<span data-ttu-id="9ea2b-125">ShapeShdwType</span><span class="sxs-lookup"><span data-stu-id="9ea2b-125">ShapeShdwType</span></span>  <br/> |
   
<span data-ttu-id="9ea2b-126">Para obtener una referencia desde un programa a la celda ShapeShdwType por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9ea2b-126">To get a reference to the ShapeShdwType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ea2b-127">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="9ea2b-127">Section index:</span></span>  <br/> |<span data-ttu-id="9ea2b-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9ea2b-128">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9ea2b-129">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="9ea2b-129">Row index:</span></span>  <br/> |<span data-ttu-id="9ea2b-130">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="9ea2b-130">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="9ea2b-131">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="9ea2b-131">Cell index:</span></span>  <br/> |<span data-ttu-id="9ea2b-132">**visFillShdwType**</span><span class="sxs-lookup"><span data-stu-id="9ea2b-132">**visFillShdwType**</span></span> <br/> |
   

