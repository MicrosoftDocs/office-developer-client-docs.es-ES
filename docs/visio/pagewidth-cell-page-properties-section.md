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
ms.openlocfilehash: 6d887cb4335d2725101db54ba2b1483ccf01cff4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434273"
---
# <a name="pagewidth-cell-page-properties-section"></a><span data-ttu-id="88aac-103">Celda PageWidth (Sección de propiedades de página)</span><span class="sxs-lookup"><span data-stu-id="88aac-103">PageWidth Cell (Page Properties Section)</span></span>

<span data-ttu-id="88aac-104">Determina el ancho de la página impresa en las unidades de dibujo.</span><span class="sxs-lookup"><span data-stu-id="88aac-104">Determines the width of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="88aac-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="88aac-105">Remarks</span></span>

<span data-ttu-id="88aac-106">También puede establecer el ancho  de página  en la ficha Tamaño  de página  del cuadro de diálogo Configurar página (en la pestaña Diseño, haga clic en la flecha de configuración de página) o cambiar manualmente el tamaño de la página con el mouse.</span><span class="sxs-lookup"><span data-stu-id="88aac-106">You can also set the page width on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) or by manually resizing the page with the mouse.</span></span> <span data-ttu-id="88aac-107">Para ello, arrastre el borde de la página mientras mantiene presionada la tecla CTRL.</span><span class="sxs-lookup"><span data-stu-id="88aac-107">To do this, drag the edge of the page while holding down the CTRL key.</span></span> 
  
<span data-ttu-id="88aac-108">Para obtener una referencia a la celda PageWidth por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="88aac-108">To get a reference to the PageWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="88aac-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="88aac-109">Cell name:</span></span>  <br/> |<span data-ttu-id="88aac-110">PageWidth</span><span class="sxs-lookup"><span data-stu-id="88aac-110">PageWidth</span></span>  <br/> |
   
<span data-ttu-id="88aac-111">Para obtener una referencia desde un programa a la celda PageWidth por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="88aac-111">To get a reference to the PageWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="88aac-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="88aac-112">Section index:</span></span>  <br/> |<span data-ttu-id="88aac-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="88aac-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="88aac-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="88aac-114">Row index:</span></span>  <br/> |<span data-ttu-id="88aac-115">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="88aac-115">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="88aac-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="88aac-116">Cell index:</span></span>  <br/> |<span data-ttu-id="88aac-117">**visPageWidth**</span><span class="sxs-lookup"><span data-stu-id="88aac-117">**visPageWidth**</span></span> <br/> |
   

