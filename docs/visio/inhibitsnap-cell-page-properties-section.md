---
title: Celda InhibitSnap (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251620
localization_priority: Normal
ms.assetid: ab9fcebc-1550-3b9e-e3b4-e8b92424390b
description: Determina si las formas de una página de primer plano se ajustan a otros objetos de esta página, así como a formas de una página de fondo.
ms.openlocfilehash: 665130e9f9f938349028ffa1d1c06224e746de5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335325"
---
# <a name="inhibitsnap-cell-page-properties-section"></a><span data-ttu-id="6a8bb-103">Celda InhibitSnap (Sección de propiedades de página)</span><span class="sxs-lookup"><span data-stu-id="6a8bb-103">InhibitSnap Cell (Page Properties Section)</span></span>

<span data-ttu-id="6a8bb-104">Determina si las formas de una página de primer plano se ajustan a otros objetos de esta página, así como a formas de una página de fondo.</span><span class="sxs-lookup"><span data-stu-id="6a8bb-104">Determines whether the shapes on a foreground page snap to other objects on the page and shapes on the background page.</span></span>
  
|<span data-ttu-id="6a8bb-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="6a8bb-105">**Value**</span></span>|<span data-ttu-id="6a8bb-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6a8bb-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6a8bb-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="6a8bb-107">TRUE</span></span>  <br/> | <span data-ttu-id="6a8bb-108">Impide todo ajuste en la página, excepto el de la regla y la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="6a8bb-108">Inhibit all snapping on the page, except for snapping to the ruler and grid.</span></span>  <br/> |
| <span data-ttu-id="6a8bb-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="6a8bb-109">FALSE</span></span>  <br/> | <span data-ttu-id="6a8bb-110">Habilita el ajuste.</span><span class="sxs-lookup"><span data-stu-id="6a8bb-110">Enable snapping.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a8bb-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6a8bb-111">Remarks</span></span>

<span data-ttu-id="6a8bb-112">Para obtener una referencia a la celda InhibitSnap por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="6a8bb-112">To get a reference to the InhibitSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a8bb-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="6a8bb-113">Cell name:</span></span>  <br/> | <span data-ttu-id="6a8bb-114">InhibitSnap</span><span class="sxs-lookup"><span data-stu-id="6a8bb-114">InhibitSnap</span></span>  <br/> |
   
<span data-ttu-id="6a8bb-115">Para obtener una referencia a la celda InhibitSnap por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6a8bb-115">To get a reference to the InhibitSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a8bb-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="6a8bb-116">Section index:</span></span>  <br/> |<span data-ttu-id="6a8bb-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6a8bb-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6a8bb-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="6a8bb-118">Row index:</span></span>  <br/> |<span data-ttu-id="6a8bb-119">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="6a8bb-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="6a8bb-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="6a8bb-120">Cell index:</span></span>  <br/> |<span data-ttu-id="6a8bb-121">**visPageInhibitSnap**</span><span class="sxs-lookup"><span data-stu-id="6a8bb-121">**visPageInhibitSnap**</span></span> <br/> |
   

