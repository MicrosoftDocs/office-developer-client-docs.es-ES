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
ms.openlocfilehash: 8a3a5f93ff096e42ba3c13b671b46bf1cf97df82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316509"
---
# <a name="drawingscale-cell-page-properties-section"></a>Celda DrawingScale (Sección de propiedades de página)

Representa el valor de la unidad de dibujo en la escala de dibujo actual. La escala de dibujo de la página es la relación entre la unidad de la página mostrada en la celda PageScale y la unidad de dibujo que aparece en la celda DrawingScale.
  
Puede establecer la celda DrawingScale para cambiar las unidades de las reglas de una página de un programa. A continuación, figura un ejemplo de cómo cambiar de unidades de pulgadas a centímetros para un programa. En este caso, se utiliza el método **ConvertResult** para mantener la misma distancia, pero en unidades distintas. 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

Puede determinar el sistema de medida de un dibujo observando la propiedad **Units** de la celda DrawingScale. Después de ejecutar la macro anterior, la siguiente instrucción ejecutada en la ventana inmediato del editor de Visual Basic devolverá *true* . 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a>Comentarios

Esta celda corresponde a la configuración del cuadro de diálogo **Configurar página** (haga clic en la flecha de **Configurar página** en la ficha **Inicio**). 
  
Las unidades de la fórmula de la celda DrawingScale determinan las unidades de medida utilizadas por las reglas en la ventana de dibujo. Si no desea cambiar la escala del dibujo, puede seguir uno de estos procedimientos:
  
- Mantener la misma distancia expresada en la celda DrawingScale, pero en unidades distintas.
    
- Cambiar la distancia expresada en la celda PageScale en la misma proporción que cambie la celda DrawingScale.
    
Para obtener una referencia a la celda DrawingScale por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |DrawingScale  <br/> |
   
Para obtener una referencia a la celda DrawingScale por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPage** <br/> |
|Índice de celda:  <br/> |**visPageDrawingScale** <br/> |
   

