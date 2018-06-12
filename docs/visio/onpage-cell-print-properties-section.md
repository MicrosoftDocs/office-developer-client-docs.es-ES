---
title: Celda OnPage (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033793
localization_priority: Normal
ms.assetid: 4015506a-e24a-0276-c854-7791a7019067
description: Indica si el dibujo se imprime en un número concreto de páginas de la impresora.
ms.openlocfilehash: 5b695ccf6fa2364809e2f5124b9f55ea6aab50e0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822690"
---
# <a name="onpage-cell-print-properties-section"></a><span data-ttu-id="4d436-103">Celda OnPage (Sección de propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="4d436-103">OnPage Cell (Print Properties Section)</span></span>

<span data-ttu-id="4d436-104">Indica si el dibujo se imprime en un número concreto de páginas de la impresora.</span><span class="sxs-lookup"><span data-stu-id="4d436-104">Indicates whether the drawing is printed on a specific number of printer pages.</span></span> 
  
|<span data-ttu-id="4d436-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4d436-105">**Value**</span></span>|<span data-ttu-id="4d436-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4d436-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4d436-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="4d436-107">TRUE</span></span>  <br/> |<span data-ttu-id="4d436-108">Para ajustar la página de dibujo a un número establecido de páginas de la impresora.</span><span class="sxs-lookup"><span data-stu-id="4d436-108">Fit the drawing page to a defined number of printer pages.</span></span>  <br/> |
|<span data-ttu-id="4d436-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="4d436-109">FALSE</span></span>  <br/> |<span data-ttu-id="4d436-110">No ajusta la página de dibujo a un número establecido de páginas de la impresora (predeterminado).</span><span class="sxs-lookup"><span data-stu-id="4d436-110">Do not fit the drawing page to a defined number of printer pages (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d436-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d436-111">Remarks</span></span>

<span data-ttu-id="4d436-p101">Si la celda OnPage se establece en TRUE, Microsoft Visio recurrirá a las celdas PagesX y PagesY para determinar el número de páginas de impresora en que encajar el dibujo. Se omiten los valores de las celdas ScaleX y ScaleY. Esto puede considerarse una opción de escala automática.</span><span class="sxs-lookup"><span data-stu-id="4d436-p101">If the OnPage cell is set to TRUE, Microsoft Visio uses the PagesX and PagesY cells to determine the number of printer pages on which to fit the drawing. Values in the ScaleX and ScaleY cells are ignored. This can be considered an "autoscale" setting.</span></span>
  
<span data-ttu-id="4d436-115">Este valor corresponde a la opción **Ajustar a** en la ficha **Configurar impresión** en el cuadro de diálogo **Configurar página** (en la ficha **Diseño** , haga clic en la flecha de **Configurar página** ).</span><span class="sxs-lookup"><span data-stu-id="4d436-115">This value corresponds to the **Fit to** option on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) .</span></span> 
  
<span data-ttu-id="4d436-116">Para obtener una referencia a la celda OnPage por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="4d436-116">To get a reference to the OnPage cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4d436-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="4d436-117">Cell name:</span></span>  <br/> |<span data-ttu-id="4d436-118">OnPage</span><span class="sxs-lookup"><span data-stu-id="4d436-118">OnPage</span></span>  <br/> |
   
<span data-ttu-id="4d436-119">Para obtener una referencia a la celda OnPage por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4d436-119">To get a reference to the OnPage cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4d436-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="4d436-120">Section index:</span></span>  <br/> |<span data-ttu-id="4d436-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4d436-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4d436-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="4d436-122">Row index:</span></span>  <br/> |<span data-ttu-id="4d436-123">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="4d436-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="4d436-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="4d436-124">Cell index:</span></span>  <br/> |<span data-ttu-id="4d436-125">**visPrintPropertiesOnPage**</span><span class="sxs-lookup"><span data-stu-id="4d436-125">**visPrintPropertiesOnPage**</span></span> <br/> |
   

