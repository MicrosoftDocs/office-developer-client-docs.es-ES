---
title: Celda ShapePlaceStyle (Sección de diseño de la forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm70007
localization_priority: Normal
ms.assetid: 29bfe8ec-ca12-8fbf-b62b-ece3710dfe2e
description: Especifica cómo se colocan las formas en la página cuando se establecen formas en el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en Re-Layout Página y, a continuación, haga clic en Más opciones de diseño). Almacena los valores de estilo de diseño y alineación de VisCellIndices .
ms.openlocfilehash: 381f74912b64395f33a2dc55c0bad24d36a16286
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418578"
---
# <a name="shapeplacestyle-cell-shape-layout-section"></a>Celda ShapePlaceStyle (Sección de diseño de la forma)

Especifica cómo se colocan las formas en la  página cuando las formas se establecen  en el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en **Volver** a diseñar página y, a continuación, haga clic en Más opciones de  **diseño).** Almacena los valores de estilo y alineación del diseño desde **VisCellIndices**. 
  
|**Constante**|**Valor**|
|:-----|:-----|
|**visLOPlaceBottomToTop** <br/> |4   <br/> |
|**visLOPlaceCircular** <br/> |6   <br/> |
|**visLOPlaceCompactDownLeft** <br/> |14   <br/> |
|**visLOPlaceCompactDownRight** <br/> |7   <br/> |
|**visLOPlaceCompactLeftDown** <br/> |13  <br/> |
|**visLOPlaceCompactLeftUp** <br/> |12   <br/> |
|**visLOPlaceCompactRightDown** <br/> |8   <br/> |
|**visLOPlaceCompactRightUp** <br/> |9   <br/> |
|**visLOPlaceCompactUpLeft** <br/> |11  <br/> |
|**visLOPlaceCompactUpRight** <br/> |10  <br/> |
|**visLOPlaceDefault** <br/> |0  <br/> |
|**visLOPlaceHierarchyBottomToTopCenter** <br/> |20  <br/> |
|**visLOPlaceHierarchyBottomToTopLeft** <br/> |19  <br/> |
|**visLOPlaceHierarchyBottomToTopRight** <br/> | 21  <br/> |
|**visLOPlaceHierarchyLeftToRightBottom** <br/> |24  <br/> |
|**visLOPlaceHierarchyLeftToRightMiddle** <br/> |23  <br/> |
|**visLOPlaceHierarchyLeftToRightTop** <br/> |22  <br/> |
|**visLOPlaceHierarchyRightToLeftBottom** <br/> |27  <br/> |
|**visLOPlaceHierarchyRightToLeftMiddle** <br/> |26  <br/> |
|**visLOPlaceHierarchyRightToLeftTop** <br/> |25  <br/> |
|**visLOPlaceHierarchyTopToBottomCenter** <br/> |17   <br/> |
|**visLOPlaceHierarchyTopToBottomLeft** <br/> |16   <br/> |
|**visLOPlaceHierarchyTopToBottomRight** <br/> |18   <br/> |
|**visLOPlaceLeftToRight** <br/> |2  <br/> |
|**visLOPlaceParentDefault** <br/> |15  <br/> |
|**visLOPlaceRadial** <br/> |3  <br/> |
|**visLOPlaceRightToLeft** <br/> |5   <br/> |
|**visLOPlaceTopToBottom** <br/> |1  <br/> |
   
Para hacer referencia a la celda ShapePlaceStyle por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ShapePlaceStyle  <br/> |
   
Para hacer referencia desde un programa a la celda ShapePlaceStyle según su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
|Índice de celda:  <br/> |**visSLOPlaceStyle** <br/> |
   

