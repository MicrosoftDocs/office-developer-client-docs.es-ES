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
ms.openlocfilehash: be7ec4cccd53cc9d74811e2e45122c8bc29497d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349059"
---
# <a name="shdwoffsety-cell-page-properties-section"></a><span data-ttu-id="c8725-103">Celda ShdwOffsetY (Sección de propiedades de página)</span><span class="sxs-lookup"><span data-stu-id="c8725-103">ShdwOffsetY Cell (Page Properties Section)</span></span>

<span data-ttu-id="c8725-104">Determina el desplazamiento vertical en unidades de página del sombreado de una forma con respecto a la forma.</span><span class="sxs-lookup"><span data-stu-id="c8725-104">Determines the distance in page units that a shape's drop shadow is offset vertically from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c8725-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c8725-105">Remarks</span></span>

<span data-ttu-id="c8725-p101">Este valor se establece en el cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página**). Este valor no depende de la escala del dibujo. Si se cambia la escala del dibujo, el desplazamiento de la sombra permanece igual.</span><span class="sxs-lookup"><span data-stu-id="c8725-p101">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). This value is independent of the scale of the drawing. If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="c8725-109">Para obtener una referencia a la celda ShdwOffsetY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="c8725-109">To get a reference to the ShdwOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c8725-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c8725-110">Cell name:</span></span>  <br/> | <span data-ttu-id="c8725-111">ShdwOffsetY</span><span class="sxs-lookup"><span data-stu-id="c8725-111">ShdwOffsetY</span></span>  <br/> |
   
<span data-ttu-id="c8725-112">Para obtener una referencia desde un programa a la celda ShdwOffsetY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c8725-112">To get a reference to the ShdwOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c8725-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c8725-113">Section index:</span></span>  <br/> |<span data-ttu-id="c8725-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c8725-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c8725-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c8725-115">Row index:</span></span>  <br/> |<span data-ttu-id="c8725-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="c8725-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="c8725-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c8725-117">Cell index:</span></span>  <br/> |<span data-ttu-id="c8725-118">**visPageShdwOffsetY**</span><span class="sxs-lookup"><span data-stu-id="c8725-118">**visPageShdwOffsetY**</span></span> <br/> |
   

