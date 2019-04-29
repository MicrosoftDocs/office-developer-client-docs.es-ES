---
title: Celda ShapeSplittable (Sección de diseño de la forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60081
localization_priority: Normal
ms.assetid: 6330304a-71f3-62b4-1b27-14495e3f12c3
description: Indica si la forma unidimensional se puede dividir.
ms.openlocfilehash: 9f92cf7d147be8e59d860bcc8a958bf0cdc008c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427076"
---
# <a name="shapesplittable-cell-shape-layout-section"></a>Celda ShapeSplittable (Sección de diseño de la forma)

Indica si la forma unidimensional se puede dividir. 
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| comprendi  <br/> | No se permite la división de la forma.  <br/> |**visSLOSplittableNone** <br/> |
| 1  <br/> | Se permite la división de la forma.  <br/> |**visSLOSplittableAllow** <br/> |
   
## <a name="remarks"></a>Comentarios

El comportamiento predeterminado de los conectores y de otras formas unidimensionales depende del tipo de dibujo. 
  
La división automática de las formas se habilita y deshabilita en tres niveles diferentes: aplicación, página y forma. La división está habilitada de forma predeterminada para la aplicación y para las páginas. 
  
Para habilitar o deshabilitar la división en el nivel de la aplicación, use la opción **Habilitar División de conectores** de la ficha **avanzadas** del cuadro de diálogo **Opciones de Visio** (haga clic en la pestaña **archivo** , haga clic en **Opciones**y, a continuación, haga clic en ** Avanzado** ). 
  
Para habilitar o deshabilitar la división en una página, vea la celda [PageShapeSplit](pageshapesplit-cell-page-layout-section.md). 
  
Para hacer que una forma pueda dividir una forma unidimensional divisible, vea la celda [ShapeSplit](shapesplit-cell-shape-layout-section.md). 
  
Para obtener una referencia a la celda ShapeSplittable por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ShapeSplittable  <br/> |
   
Para obtener una referencia a la celda ShapeSplittable por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
| Índice de celda:  <br/> |**visSLOSplittable** <br/> |
   

