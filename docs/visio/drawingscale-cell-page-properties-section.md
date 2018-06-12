---
title: Celda DrawingScale (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm265
localization_priority: Normal
ms.assetid: bc447f22-a188-2c61-e33c-df0d401a4725
description: Representa el valor de la unidad de dibujo en la escala de dibujo actual. La escala de dibujo de la página es la relación entre la unidad de la página mostrada en la celda PageScale y la unidad de dibujo que aparece en la celda DrawingScale.
ms.openlocfilehash: cdd3222f5e56c34ac8947c9ef5a653cfe19fbd0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822018"
---
# <a name="drawingscale-cell-page-properties-section"></a><span data-ttu-id="a4160-104">Celda DrawingScale (Sección de propiedades de página)</span><span class="sxs-lookup"><span data-stu-id="a4160-104">DrawingScale Cell (Page Properties Section)</span></span>

<span data-ttu-id="a4160-p102">Representa el valor de la unidad de dibujo en la escala de dibujo actual. La escala de dibujo de la página es la relación entre la unidad de la página mostrada en la celda PageScale y la unidad de dibujo que aparece en la celda DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="a4160-p102">Represents the value of the drawing unit in the current drawing scale. The drawing scale for the page is the ratio of the page unit shown in the PageScale cell to the drawing unit shown in the DrawingScale cell.</span></span>
  
<span data-ttu-id="a4160-107">Puede establecer la celda DrawingScale para cambiar las unidades de reglas de una página de un programa.</span><span class="sxs-lookup"><span data-stu-id="a4160-107">You can set the DrawingScale cell to change the units of a page's rulers from a program.</span></span> <span data-ttu-id="a4160-108">Este es un ejemplo de cambio de las unidades de medida de pulgadas a centímetros para un programa.</span><span class="sxs-lookup"><span data-stu-id="a4160-108">Here is an example of changing the measurement units from inches to centimeters from a program.</span></span> <span data-ttu-id="a4160-109">En este caso, usamos el método **ConvertResult** para conservar igual la distancia pero expresada en unidades distintas.</span><span class="sxs-lookup"><span data-stu-id="a4160-109">In this case, we use the **ConvertResult** method to keep the distance the same but express it in different units.</span></span> 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

<span data-ttu-id="a4160-110">Puede determinar el sistema de medida de un dibujo mediante el examen de la propiedad **Units** de la celda DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="a4160-110">You can determine the measurement system in a drawing by examining the **Units** property of the DrawingScale cell.</span></span> <span data-ttu-id="a4160-111">Después de ejecutar la macro anterior, la siguiente instrucción ejecutada en la ejecución del Editor de Visual Basic ventana devolverá *True* .</span><span class="sxs-lookup"><span data-stu-id="a4160-111">After running the above macro the following statement executed in the Visual Basic Editor Immediate window will return  *True*  .</span></span> 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a><span data-ttu-id="a4160-112">Notas</span><span class="sxs-lookup"><span data-stu-id="a4160-112">Remarks</span></span>

<span data-ttu-id="a4160-113">Esta celda corresponde a la configuración en el cuadro de diálogo **Configurar página** (haga clic en la flecha de **Configurar página** en la ficha **Inicio** ).</span><span class="sxs-lookup"><span data-stu-id="a4160-113">This cell corresponds to the settings in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="a4160-p105">Las unidades de la fórmula de la celda DrawingScale determinan las unidades de medida utilizadas por las reglas en la ventana de dibujo. Si no desea cambiar la escala del dibujo, puede seguir uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="a4160-p105">The units of the formula in the DrawingScale cell determine the measurement units used by the rulers in the drawing window. If you do not want to also change the drawing's scale, you can do one of the following:</span></span>
  
- <span data-ttu-id="a4160-116">Mantener la misma distancia expresada en la celda DrawingScale, pero en unidades distintas.</span><span class="sxs-lookup"><span data-stu-id="a4160-116">Keep the distance expressed in the DrawingScale cell the same but express it in different units.</span></span>
    
- <span data-ttu-id="a4160-117">Cambiar la distancia expresada en la celda PageScale en la misma proporción que cambie la celda DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="a4160-117">Change the distance expressed in the PageScale cell by the same factor that you change DrawingScale.</span></span>
    
<span data-ttu-id="a4160-118">Para obtener una referencia a la celda DrawingScale por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="a4160-118">To get a reference to the DrawingScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a4160-119">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="a4160-119">Cell name:</span></span>  <br/> |<span data-ttu-id="a4160-120">DrawingScale</span><span class="sxs-lookup"><span data-stu-id="a4160-120">DrawingScale</span></span>  <br/> |
   
<span data-ttu-id="a4160-121">Para obtener una referencia a la celda DrawingScale por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a4160-121">To get a reference to the DrawingScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a4160-122">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="a4160-122">Section index:</span></span>  <br/> |<span data-ttu-id="a4160-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a4160-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a4160-124">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="a4160-124">Row index:</span></span>  <br/> |<span data-ttu-id="a4160-125">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="a4160-125">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="a4160-126">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="a4160-126">Cell index:</span></span>  <br/> |<span data-ttu-id="a4160-127">**visPageDrawingScale**</span><span class="sxs-lookup"><span data-stu-id="a4160-127">**visPageDrawingScale**</span></span> <br/> |
   

