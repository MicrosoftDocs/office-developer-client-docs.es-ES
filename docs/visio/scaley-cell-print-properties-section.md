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
ms.openlocfilehash: 0f8e86675a039002b60438eac7df92f4a2b13b98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342731"
---
# <a name="scaley-cell-print-properties-section"></a><span data-ttu-id="aae5c-103">Celda ScaleY (sección de propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="aae5c-103">ScaleY Cell (Print Properties Section)</span></span>

<span data-ttu-id="aae5c-104">Especifica el porcentaje de ampliación de la página de dibujo en la página de la impresora.</span><span class="sxs-lookup"><span data-stu-id="aae5c-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aae5c-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aae5c-105">Remarks</span></span>

<span data-ttu-id="aae5c-106">Este valor solo se usa cuando el valor de la celda OnPage es FALSE.</span><span class="sxs-lookup"><span data-stu-id="aae5c-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="aae5c-107">Las celdas ScaleX y scaleY siempre tienen el mismo valor, que corresponde al valor de la opción **ajustar a** de la ficha **Configurar impresión** del cuadro de diálogo **Configurar página** (en la ficha **diseño** , haga clic en la flecha de **Configurar página** ).</span><span class="sxs-lookup"><span data-stu-id="aae5c-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="aae5c-108">Para obtener una referencia a la celda ScaleY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="aae5c-108">To get a reference to the ScaleY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aae5c-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="aae5c-109">Cell name:</span></span>  <br/> |<span data-ttu-id="aae5c-110">ScaleY</span><span class="sxs-lookup"><span data-stu-id="aae5c-110">ScaleY</span></span>  <br/> |
   
<span data-ttu-id="aae5c-111">Para obtener una referencia desde un programa a la celda ScaleY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="aae5c-111">To get a reference to the ScaleY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aae5c-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="aae5c-112">Section index:</span></span>  <br/> |<span data-ttu-id="aae5c-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="aae5c-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="aae5c-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="aae5c-114">Row index:</span></span>  <br/> |<span data-ttu-id="aae5c-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="aae5c-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="aae5c-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="aae5c-116">Cell index:</span></span>  <br/> |<span data-ttu-id="aae5c-117">**visPrintPropertiesScaleY**</span><span class="sxs-lookup"><span data-stu-id="aae5c-117">**visPrintPropertiesScaleY**</span></span> <br/> |
   

