---
title: Celda PageShapeSplit (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033777
localization_priority: Normal
ms.assetid: 4d3bdf77-0ad4-86a4-d215-1d5a5fbe33f7
description: Indica si las formas de la página se pueden dividir de forma automática.
ms.openlocfilehash: 7f1df0158cde6853c5518597c853cb56151eefbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822730"
---
# <a name="pageshapesplit-cell-page-layout-section"></a>Celda PageShapeSplit (sección Diseño de página)

Indica si las formas de la página se pueden dividir de forma automática.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |No se permite la división automática de formas.  <br/> |**visPLOSplitNone** <br/> |
|1  <br/> |Se permite la división automática de formas (valor predeterminado).  <br/> |**visPLOSplitAllow** <br/> |
   
## <a name="remarks"></a>Observaciones

La división automática de formas se habilita y deshabilita en tres niveles distintos: aplicación, página y forma. La división está habilitada de forma predeterminada para la aplicación y para las páginas. La configuración predeterminada para las formas depende del tipo de dibujo. 
  
Para habilitar o deshabilitar la división en el nivel de aplicación, use la opción **Habilitar división de conectores** en la ficha **Avanzadas** del cuadro de diálogo **Opciones de Visio** (haga clic en el botón de **Office** , haga clic en **Opciones** en el de **Visio** ficha y, a continuación, haga clic en **Opciones avanzadas** ). 
  
Para habilitar o deshabilitar la división en el nivel de la forma, vea las celdas ShapeSplit y ShapeSplittable. 
  
Para obtener una referencia a la celda PageShapeSplit por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |PageShapeSplit  <br/> |
   
Para obtener una referencia desde un programa a la celda PageShapeSplit por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPageLayout** <br/> |
|Índice de celda:  <br/> |**visPLOSplit** <br/> |
   

