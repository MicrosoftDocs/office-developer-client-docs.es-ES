---
title: Celda ShdwType (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
localization_priority: Normal
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: Indica el tipo de sombra predeterminado para una página.
ms.openlocfilehash: 1fc5c31a723d5d409110d94ff543a45dadabf264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823221"
---
# <a name="shdwtype-cell-page-properties-section"></a><span data-ttu-id="8617b-103">Celda ShdwType (sección Propiedades de la página)</span><span class="sxs-lookup"><span data-stu-id="8617b-103">ShdwType Cell (Page Properties Section)</span></span>

<span data-ttu-id="8617b-104">Indica el tipo de sombra predeterminado para una página.</span><span class="sxs-lookup"><span data-stu-id="8617b-104">Indicates the default shadow type for a page.</span></span>
  
|<span data-ttu-id="8617b-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8617b-105">**Value**</span></span>|<span data-ttu-id="8617b-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8617b-106">**Description**</span></span>|<span data-ttu-id="8617b-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="8617b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="8617b-108">1</span><span class="sxs-lookup"><span data-stu-id="8617b-108">1</span></span>  <br/> | <span data-ttu-id="8617b-109">Simple</span><span class="sxs-lookup"><span data-stu-id="8617b-109">Simple</span></span>  <br/> |<span data-ttu-id="8617b-110">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="8617b-110">**visFSTSimple**</span></span> <br/> |
| <span data-ttu-id="8617b-111">2</span><span class="sxs-lookup"><span data-stu-id="8617b-111">2</span></span>  <br/> | <span data-ttu-id="8617b-112">Oblicuo</span><span class="sxs-lookup"><span data-stu-id="8617b-112">Oblique</span></span>  <br/> |<span data-ttu-id="8617b-113">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="8617b-113">**visFSTOblique**</span></span> <br/> |
|<span data-ttu-id="8617b-114">3</span><span class="sxs-lookup"><span data-stu-id="8617b-114">3</span></span>  <br/> |<span data-ttu-id="8617b-115">Interna</span><span class="sxs-lookup"><span data-stu-id="8617b-115">Inner</span></span>  <br/> |<span data-ttu-id="8617b-116">**visFSTInner**</span><span class="sxs-lookup"><span data-stu-id="8617b-116">**visFSTInner**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8617b-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8617b-117">Remarks</span></span>

 <span data-ttu-id="8617b-118">El tipo de sombra que se describe en esta celda se utiliza cuando la celda ShapeShdwType (tipo de sombra para una forma individual en la página) se establece el valor predeterminado de página (**visFSTPageDefault** ).</span><span class="sxs-lookup"><span data-stu-id="8617b-118">The shadow type described in this cell is used whenever the ShapeShdwType Cell (the shadow type for an individual shape on the page) is set to Page Default (**visFSTPageDefault** ).</span></span> 
  
<span data-ttu-id="8617b-119">Se describen los tipos de sombra simple como sombras de desplazamiento en la interfaz de usuario (UI).</span><span class="sxs-lookup"><span data-stu-id="8617b-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="8617b-120">Una sombra simple proporciona el efecto de sombra sobre un plano paralelo situado a cierta distancia detrás de él.</span><span class="sxs-lookup"><span data-stu-id="8617b-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located some distance behind it.</span></span> <span data-ttu-id="8617b-121">Las sombras oblicuas se describen como sombras oblicuas en la interfaz de usuario y dan el efecto de la sombra se convierte en un plano perpendicular a la forma.</span><span class="sxs-lookup"><span data-stu-id="8617b-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="8617b-122">Para consultar una lista de tipos de sombras simples y oblicuas predeterminados, vea la lista **Estilo** de la ficha **Sombras** del cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página**).</span><span class="sxs-lookup"><span data-stu-id="8617b-122">For a list of predefined simple and oblique shadow types, see the **Style** list on the **Shadows** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="8617b-123">Para obtener una referencia a la celda ShdwType por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="8617b-123">To get a reference to the ShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8617b-124">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="8617b-124">Cell name:</span></span>  <br/> | <span data-ttu-id="8617b-125">ShdwType</span><span class="sxs-lookup"><span data-stu-id="8617b-125">ShdwType</span></span>  <br/> |
   
<span data-ttu-id="8617b-126">Para obtener una referencia desde un programa a la celda ShapeShdwOffsetX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="8617b-126">To get a reference to the ShapeShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8617b-127">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="8617b-127">Section index:</span></span>  <br/> |<span data-ttu-id="8617b-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8617b-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8617b-129">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="8617b-129">Row index:</span></span>  <br/> |<span data-ttu-id="8617b-130">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="8617b-130">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="8617b-131">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="8617b-131">Cell index:</span></span>  <br/> |<span data-ttu-id="8617b-132">**visPageShdwType**</span><span class="sxs-lookup"><span data-stu-id="8617b-132">**visPageShdwType**</span></span> <br/> |
   

