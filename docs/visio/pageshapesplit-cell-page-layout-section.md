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
ms.openlocfilehash: 18a40e0876b117556a1e7ab43f640e798dc248c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422022"
---
# <a name="pageshapesplit-cell-page-layout-section"></a>Celda PageShapeSplit (Sección de diseño de página)

Indica si las formas de la página se pueden dividir de forma automática.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|comprendi  <br/> |No se permite la división automática de formas.  <br/> |**visPLOSplitNone** <br/> |
|1  <br/> |Se permite la división automática de formas (valor predeterminado).  <br/> |**visPLOSplitAllow** <br/> |
   
## <a name="remarks"></a>Comentarios

La división automática de formas se habilita y deshabilita en tres niveles distintos: aplicación, página y forma. La división está habilitada de forma predeterminada para la aplicación y para las páginas. La configuración predeterminada para las formas depende del tipo de dibujo. 
  
Para habilitar o deshabilitar la división en el nivel de la aplicación, use la opción **Habilitar División de conectores** de la ficha **avanzadas** del cuadro de diálogo **Opciones de Visio** (haga clic en el botón **Office** y haga clic en **Opciones** en **Visio** y, a continuación, haga clic en **avanzadas** ). 
  
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
   

