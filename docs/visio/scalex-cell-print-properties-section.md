---
title: Celda ScaleX (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
localization_priority: Normal
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
description: Especifica el porcentaje de ampliación de la página de dibujo en la página de impresora.
ms.openlocfilehash: d1c2f6c184f987e1e7190b1c208310b83a823ee3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410213"
---
# <a name="scalex-cell-print-properties-section"></a><span data-ttu-id="67650-103">Celda ScaleX (sección de propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="67650-103">ScaleX Cell (Print Properties Section)</span></span>

<span data-ttu-id="67650-104">Especifica el porcentaje de ampliación de la página de dibujo en la página de impresora.</span><span class="sxs-lookup"><span data-stu-id="67650-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="67650-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="67650-105">Remarks</span></span>

<span data-ttu-id="67650-106">Este valor solo se usa cuando el valor de la celda OnPage es FALSE.</span><span class="sxs-lookup"><span data-stu-id="67650-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="67650-107">Las celdas ScaleX y ScaleY siempre tienen el mismo  valor, que corresponde al valor  de la opción Ajustar a de  la ficha Configurar impresión del cuadro de diálogo Configurar página (en la ficha Diseño, haga clic en la flecha del programa de instalación de página).  </span><span class="sxs-lookup"><span data-stu-id="67650-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="67650-108">Para obtener una referencia a la celda ScaleX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="67650-108">To get a reference to the ScaleX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="67650-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="67650-109">Cell name:</span></span>  <br/> |<span data-ttu-id="67650-110">ScaleX</span><span class="sxs-lookup"><span data-stu-id="67650-110">ScaleX</span></span>  <br/> |
   
<span data-ttu-id="67650-111">Para obtener una referencia desde un programa a la celda ScaleX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="67650-111">To get a reference to the ScaleX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="67650-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="67650-112">Section index:</span></span>  <br/> |<span data-ttu-id="67650-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="67650-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="67650-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="67650-114">Row index:</span></span>  <br/> |<span data-ttu-id="67650-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="67650-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="67650-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="67650-116">Cell index:</span></span>  <br/> |<span data-ttu-id="67650-117">**visPrintPropertiesScaleX**</span><span class="sxs-lookup"><span data-stu-id="67650-117">**visPrintPropertiesScaleX**</span></span> <br/> |
   

