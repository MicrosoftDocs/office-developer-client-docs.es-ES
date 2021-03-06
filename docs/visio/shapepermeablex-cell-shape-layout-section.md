---
title: Celda ShapePermeableX (Sección de diseño de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm890
localization_priority: Normal
ms.assetid: 7e27b36c-4fd1-34e0-c168-f49eb5757b0e
description: Determina si un conector puede enrutar horizontalmente a través de una forma que puede colocarse.
ms.openlocfilehash: 21fa1683c4b1afd24992ec7a8a6daa52a8280825
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409478"
---
# <a name="shapepermeablex-cell-shape-layout-section"></a>Celda ShapePermeableX (Sección de diseño de forma)

Determina si un conector puede enrutar horizontalmente a través de una forma que puede colocarse.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Se permite que los conectores enruten horizontalmente a través de una forma que puede colocarse.  <br/> |
|FALSE  <br/> |No se permite que los conectores enruten horizontalmente a través de una forma que puede colocarse.  <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer el valor de  esta celda en la ficha Ubicación del [](run-in-developer-mode-display-the-developer-tab.md) cuadro de diálogo Comportamiento (con una forma seleccionada, en la ficha Programador, en el grupo Diseño de formas, haga clic en Comportamiento y, a continuación, haga clic en la pestaña Ubicación).    
  
En las versiones anteriores a Visio 2000, este comportamiento se establece mediante la celda ObjInteract, en la sección de varios. 
  
Para obtener una referencia a la celda ShapePermeableX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ShapePermeableX  <br/> |
   
Para obtener una referencia desde un programa a la celda ShapePermeableX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
|Índice de celda:  <br/> |**visSLOPermX** <br/> |
   

