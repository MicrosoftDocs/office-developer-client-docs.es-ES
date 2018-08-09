---
title: Celda PageTopMargin (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033785
localization_priority: Normal
ms.assetid: 2ba0fd22-65a6-6cb6-da00-08f391705544
description: Especifica el margen superior de la página impresa.
ms.openlocfilehash: 1b7be63e3f21365231120c602d8edfe1dc727f88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822723"
---
# <a name="pagetopmargin-cell-print-properties-section"></a><span data-ttu-id="77fe3-103">Celda PageTopMargin (sección Propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="77fe3-103">PageTopMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="77fe3-104">Especifica el margen superior de la página impresa.</span><span class="sxs-lookup"><span data-stu-id="77fe3-104">Specifies the margin at the top of the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="77fe3-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="77fe3-105">Remarks</span></span>

<span data-ttu-id="77fe3-p101">Este valor representa unidades físicas y no se ve afectado por escalas ni unidades de dibujo. Por ejemplo, si esta celda tiene el valor 0,25 pda., este margen será de 0,25 pulgadas incluso si se utilizan pies como unidades en la página. Si las unidades no se indican explícitamente, este valor asume de forma predeterminada las unidades de la página.</span><span class="sxs-lookup"><span data-stu-id="77fe3-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="77fe3-109">Para obtener una referencia a la celda PageTopMargin por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="77fe3-109">To get a reference to the PageTopMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="77fe3-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="77fe3-110">Cell name:</span></span>  <br/> | <span data-ttu-id="77fe3-111">PageTopMargin</span><span class="sxs-lookup"><span data-stu-id="77fe3-111">PageTopMargin</span></span>  <br/> |
   
<span data-ttu-id="77fe3-112">Para obtener una referencia desde un programa a la celda PageTopMargin por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="77fe3-112">To get a reference to the PageTopMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="77fe3-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="77fe3-113">Section index:</span></span>  <br/> |<span data-ttu-id="77fe3-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="77fe3-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="77fe3-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="77fe3-115">Row index:</span></span>  <br/> |<span data-ttu-id="77fe3-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="77fe3-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="77fe3-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="77fe3-117">Cell index:</span></span>  <br/> |<span data-ttu-id="77fe3-118">**visPrintPropertiesTopMargin**</span><span class="sxs-lookup"><span data-stu-id="77fe3-118">**visPrintPropertiesTopMargin**</span></span> <br/> |
   

