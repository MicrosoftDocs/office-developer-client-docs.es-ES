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
ms.openlocfilehash: b782977bd5b7e828223675eb16f4e7e48f4ca55d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823182"
---
# <a name="shapesplit-cell-shape-layout-section"></a>Celda ShapeSplit (sección Diseño de forma)

Indica si la forma puede dividir formas divisibles.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | No se permite que esta forma divida otras formas.  <br/> |**visSLOSplitNone** <br/> |
| 1  <br/> | Se permite que esta forma divida otras formas.  <br/> |**visSLOSplitAllow** <br/> |
   
## <a name="remarks"></a>Observaciones

Una forma que pueda dividir otras tiene que ser una forma bidimensional o bien una forma colocable unidimensional. 
  
La división automática de formas se habilita y deshabilita en tres niveles diferentes: aplicación, página y forma. La división está habilitada de forma predeterminada para la aplicación y para las páginas; para las formas, depende del tipo de dibujo. 
  
Para habilitar o deshabilitar la división en el nivel de aplicación, use la opción **Habilitar división de conectores** en la ficha **Avanzadas** del cuadro de diálogo **Opciones de Visio** (haga clic en la pestaña **archivo** , haga clic en **Opciones**y, a continuación, haga clic en ** Avanzada**). 
  
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
   

