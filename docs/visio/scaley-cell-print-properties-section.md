---
title: Celda ScaleY (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
localization_priority: Normal
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
description: Especifica el porcentaje de ampliación de la página de dibujo en la página de la impresora.
ms.openlocfilehash: 2735b2cfce04cc9a8d8da1a815081aaa5892c723
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823101"
---
# <a name="scaley-cell-print-properties-section"></a><span data-ttu-id="1224e-103">Celda ScaleY (sección Propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="1224e-103">ScaleY Cell (Print Properties Section)</span></span>

<span data-ttu-id="1224e-104">Especifica el porcentaje de ampliación de la página de dibujo en la página de la impresora.</span><span class="sxs-lookup"><span data-stu-id="1224e-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1224e-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1224e-105">Remarks</span></span>

<span data-ttu-id="1224e-106">Este valor solo se usa cuando el valor de la celda OnPage es FALSE.</span><span class="sxs-lookup"><span data-stu-id="1224e-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="1224e-107">Las celdas ScaleX y ScaleY siempre tienen el mismo valor, que corresponde al valor de la opción **Ajustar a** en la ficha **Configurar impresión** en el cuadro de diálogo **Configurar página** (en la ficha **Diseño** , haga clic en la flecha de **Configurar página** ).</span><span class="sxs-lookup"><span data-stu-id="1224e-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="1224e-108">Para obtener una referencia a la celda ScaleY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="1224e-108">To get a reference to the ScaleY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1224e-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="1224e-109">Cell name:</span></span>  <br/> |<span data-ttu-id="1224e-110">ScaleY</span><span class="sxs-lookup"><span data-stu-id="1224e-110">ScaleY</span></span>  <br/> |
   
<span data-ttu-id="1224e-111">Para obtener una referencia desde un programa a la celda ScaleY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1224e-111">To get a reference to the ScaleY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1224e-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="1224e-112">Section index:</span></span>  <br/> |<span data-ttu-id="1224e-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1224e-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1224e-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="1224e-114">Row index:</span></span>  <br/> |<span data-ttu-id="1224e-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="1224e-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="1224e-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="1224e-116">Cell index:</span></span>  <br/> |<span data-ttu-id="1224e-117">**visPrintPropertiesScaleY**</span><span class="sxs-lookup"><span data-stu-id="1224e-117">**visPrintPropertiesScaleY**</span></span> <br/> |
   

