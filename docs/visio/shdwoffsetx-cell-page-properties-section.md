---
title: Celda ShdwOffsetX (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251373
localization_priority: Normal
ms.assetid: 92ec9b11-f53f-a1c9-832a-6cac08aa5379
description: Determina el desplazamiento horizontal en unidades de página del sombreado de una forma con respecto a la forma.
ms.openlocfilehash: 9aec108146e329d7a8161acc4ca7cdcb19424eff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823210"
---
# <a name="shdwoffsetx-cell-page-properties-section"></a><span data-ttu-id="06449-103">Celda ShdwOffsetX (sección Propiedades de la página)</span><span class="sxs-lookup"><span data-stu-id="06449-103">ShdwOffsetX Cell (Page Properties Section)</span></span>

<span data-ttu-id="06449-104">Determina el desplazamiento horizontal en unidades de página del sombreado de una forma con respecto a la forma.</span><span class="sxs-lookup"><span data-stu-id="06449-104">Determines the distance in page units that a shape's drop shadow is offset horizontally from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="06449-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06449-105">Remarks</span></span>

<span data-ttu-id="06449-p101">Este valor se establece en el cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página**). Este valor no depende de la escala del dibujo. Si se cambia la escala del dibujo, el desplazamiento de la sombra permanece igual.</span><span class="sxs-lookup"><span data-stu-id="06449-p101">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). This value is independent of the scale of the drawing. If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="06449-109">Para obtener una referencia a la celda ShdwOffsetX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="06449-109">To get a reference to the ShdwOffsetX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="06449-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="06449-110">Cell name:</span></span>  <br/> | <span data-ttu-id="06449-111">ShdwOffsetX</span><span class="sxs-lookup"><span data-stu-id="06449-111">ShdwOffsetX</span></span>  <br/> |
   
<span data-ttu-id="06449-112">Para obtener una referencia desde un programa a la celda ShdwOffsetX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="06449-112">To get a reference to the ShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="06449-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="06449-113">Section index:</span></span>  <br/> |<span data-ttu-id="06449-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="06449-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="06449-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="06449-115">Row index:</span></span>  <br/> |<span data-ttu-id="06449-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="06449-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="06449-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="06449-117">Cell index:</span></span>  <br/> |<span data-ttu-id="06449-118">**visPageShdwOffsetX**</span><span class="sxs-lookup"><span data-stu-id="06449-118">**visPageShdwOffsetX**</span></span> <br/> |
   

