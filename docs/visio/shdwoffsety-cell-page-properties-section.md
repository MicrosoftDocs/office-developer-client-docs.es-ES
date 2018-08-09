---
title: Celda ShdwOffsetY (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm930
localization_priority: Normal
ms.assetid: f3f53a7d-7450-b2b0-b508-6044a87450d9
description: Determina el desplazamiento vertical en unidades de página del sombreado de una forma con respecto a la forma.
ms.openlocfilehash: 0228fef00230dd1517d20067fda855225cef5533
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823227"
---
# <a name="shdwoffsety-cell-page-properties-section"></a><span data-ttu-id="76615-103">Celda ShdwOffsetY (sección Propiedades de la página)</span><span class="sxs-lookup"><span data-stu-id="76615-103">ShdwOffsetY Cell (Page Properties Section)</span></span>

<span data-ttu-id="76615-104">Determina el desplazamiento vertical en unidades de página del sombreado de una forma con respecto a la forma.</span><span class="sxs-lookup"><span data-stu-id="76615-104">Determines the distance in page units that a shape's drop shadow is offset vertically from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="76615-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76615-105">Remarks</span></span>

<span data-ttu-id="76615-p101">Este valor se establece en el cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página**). Este valor no depende de la escala del dibujo. Si se cambia la escala del dibujo, el desplazamiento de la sombra permanece igual.</span><span class="sxs-lookup"><span data-stu-id="76615-p101">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). This value is independent of the scale of the drawing. If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="76615-109">Para obtener una referencia a la celda ShdwOffsetY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="76615-109">To get a reference to the ShdwOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="76615-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="76615-110">Cell name:</span></span>  <br/> | <span data-ttu-id="76615-111">ShdwOffsetY</span><span class="sxs-lookup"><span data-stu-id="76615-111">ShdwOffsetY</span></span>  <br/> |
   
<span data-ttu-id="76615-112">Para obtener una referencia desde un programa a la celda ShdwOffsetY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="76615-112">To get a reference to the ShdwOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="76615-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="76615-113">Section index:</span></span>  <br/> |<span data-ttu-id="76615-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="76615-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="76615-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="76615-115">Row index:</span></span>  <br/> |<span data-ttu-id="76615-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="76615-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="76615-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="76615-117">Cell index:</span></span>  <br/> |<span data-ttu-id="76615-118">**visPageShdwOffsetY**</span><span class="sxs-lookup"><span data-stu-id="76615-118">**visPageShdwOffsetY**</span></span> <br/> |
   

