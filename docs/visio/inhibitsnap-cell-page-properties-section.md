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
ms.openlocfilehash: b95dafda9ebef36db34f60585ab3ed2164ade415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822339"
---
# <a name="inhibitsnap-cell-page-properties-section"></a><span data-ttu-id="e0f75-103">Celda InhibitSnap (sección Propiedades de página)</span><span class="sxs-lookup"><span data-stu-id="e0f75-103">InhibitSnap Cell (Page Properties Section)</span></span>

<span data-ttu-id="e0f75-104">Determina si las formas de una página de primer plano se ajustan a otros objetos de esta página, así como a formas de una página de fondo.</span><span class="sxs-lookup"><span data-stu-id="e0f75-104">Determines whether the shapes on a foreground page snap to other objects on the page and shapes on the background page.</span></span>
  
|<span data-ttu-id="e0f75-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e0f75-105">**Value**</span></span>|<span data-ttu-id="e0f75-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e0f75-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e0f75-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e0f75-107">TRUE</span></span>  <br/> | <span data-ttu-id="e0f75-108">Impide todo ajuste en la página, excepto el de la regla y la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="e0f75-108">Inhibit all snapping on the page, except for snapping to the ruler and grid.</span></span>  <br/> |
| <span data-ttu-id="e0f75-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e0f75-109">FALSE</span></span>  <br/> | <span data-ttu-id="e0f75-110">Habilita el ajuste.</span><span class="sxs-lookup"><span data-stu-id="e0f75-110">Enable snapping.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0f75-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e0f75-111">Remarks</span></span>

<span data-ttu-id="e0f75-112">Para obtener una referencia a la celda InhibitSnap por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="e0f75-112">To get a reference to the InhibitSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e0f75-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="e0f75-113">Cell name:</span></span>  <br/> | <span data-ttu-id="e0f75-114">InhibitSnap</span><span class="sxs-lookup"><span data-stu-id="e0f75-114">InhibitSnap</span></span>  <br/> |
   
<span data-ttu-id="e0f75-115">Para obtener una referencia a la celda InhibitSnap por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e0f75-115">To get a reference to the InhibitSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e0f75-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="e0f75-116">Section index:</span></span>  <br/> |<span data-ttu-id="e0f75-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e0f75-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e0f75-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="e0f75-118">Row index:</span></span>  <br/> |<span data-ttu-id="e0f75-119">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="e0f75-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="e0f75-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="e0f75-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e0f75-121">**visPageInhibitSnap**</span><span class="sxs-lookup"><span data-stu-id="e0f75-121">**visPageInhibitSnap**</span></span> <br/> |
   

