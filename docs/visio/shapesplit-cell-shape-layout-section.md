---
title: Celda ShapeSplit (Sección de diseño de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60080
localization_priority: Normal
ms.assetid: 96b8c503-67b3-8623-d99b-0dad7b15c224
description: Indica si la forma puede dividir formas divisibles.
ms.openlocfilehash: 46b42e9be070b54095d3e9a5c247d63be6348f77
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349122"
---
# <a name="shapesplit-cell-shape-layout-section"></a>Celda ShapeSplit (Sección de diseño de forma)

Indica si la forma puede dividir formas divisibles.
  
|**Value**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| comprendi  <br/> | No se permite que esta forma divida otras formas.  <br/> |**visSLOSplitNone** <br/> |
| 1  <br/> | Se permite que esta forma divida otras formas.  <br/> |**visSLOSplitAllow** <br/> |
   
## <a name="remarks"></a>Comentarios

Una forma que pueda dividir otras tiene que ser una forma bidimensional o bien una forma colocable unidimensional. 
  
La división automática de formas se habilita y deshabilita en tres niveles diferentes: aplicación, página y forma. La división está habilitada de forma predeterminada para la aplicación y para las páginas; para las formas, depende del tipo de dibujo. 
  
Para habilitar o deshabilitar la división en el nivel de la aplicación, use la opción **Habilitar División de conectores** de la ficha **avanzadas** del cuadro de diálogo **Opciones de Visio** (haga clic en la pestaña **archivo** , haga clic en **Opciones**y, a continuación, haga clic en ** Avanzado**). 
  
Para habilitar o deshabilitar la división en una página, vea la celda PageShapeSplit. 
  
Para hacer que una forma unidimensional sea divisible, vea la celda ShapeSplittable.
  
Para obtener una referencia a la celda ShapeSplit por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ShapeSplit  <br/> |
   
Para obtener una referencia desde un programa a la celda ShapeSplit por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
| Índice de celda:  <br/> |**visSLOSplit** <br/> |
   

