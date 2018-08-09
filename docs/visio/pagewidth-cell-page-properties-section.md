---
title: Celda PageWidth (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251372
localization_priority: Normal
ms.assetid: b98c5bf3-10c8-7299-2836-3906d6a9135d
description: Determina el ancho de la página impresa en las unidades de dibujo.
ms.openlocfilehash: e03696c8f1c921c930d3563e9c73ef4ae613a7c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822733"
---
# <a name="pagewidth-cell-page-properties-section"></a><span data-ttu-id="da2b5-103">Celda PageWidth (sección Propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="da2b5-103">PageWidth Cell (Page Properties Section)</span></span>

<span data-ttu-id="da2b5-104">Determina el ancho de la página impresa en las unidades de dibujo.</span><span class="sxs-lookup"><span data-stu-id="da2b5-104">Determines the width of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="da2b5-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da2b5-105">Remarks</span></span>

<span data-ttu-id="da2b5-106">También puede establecer el ancho de la página en la ficha **Tamaño de página** del cuadro de diálogo **Configurar página** (en la ficha **Diseño** , haga clic en la flecha de **Configurar página** ) o manualmente si cambia el tamaño de la página con el mouse.</span><span class="sxs-lookup"><span data-stu-id="da2b5-106">You can also set the page width on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) or by manually resizing the page with the mouse.</span></span> <span data-ttu-id="da2b5-107">Para ello, arrastre el borde de la página mientras mantiene presionada la tecla CTRL.</span><span class="sxs-lookup"><span data-stu-id="da2b5-107">To do this, drag the edge of the page while holding down the CTRL key.</span></span> 
  
<span data-ttu-id="da2b5-108">Para obtener una referencia a la celda PageWidth por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="da2b5-108">To get a reference to the PageWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="da2b5-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="da2b5-109">Cell name:</span></span>  <br/> |<span data-ttu-id="da2b5-110">PageWidth</span><span class="sxs-lookup"><span data-stu-id="da2b5-110">PageWidth</span></span>  <br/> |
   
<span data-ttu-id="da2b5-111">Para obtener una referencia desde un programa a la celda PageWidth por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="da2b5-111">To get a reference to the PageWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="da2b5-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="da2b5-112">Section index:</span></span>  <br/> |<span data-ttu-id="da2b5-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="da2b5-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="da2b5-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="da2b5-114">Row index:</span></span>  <br/> |<span data-ttu-id="da2b5-115">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="da2b5-115">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="da2b5-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="da2b5-116">Cell index:</span></span>  <br/> |<span data-ttu-id="da2b5-117">**visPageWidth**</span><span class="sxs-lookup"><span data-stu-id="da2b5-117">**visPageWidth**</span></span> <br/> |
   

