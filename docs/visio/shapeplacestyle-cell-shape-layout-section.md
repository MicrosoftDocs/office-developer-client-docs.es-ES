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
description: Especifica cómo se colocan las formas en la página cuando se disponen las formas en el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo diseño, haga clic en reDistribuir página y, a continuación, haga clic en más opciones de diseño). Almacena los valores de estilo y alineación de diseño desde VisCellIndices.
ms.openlocfilehash: 381f74912b64395f33a2dc55c0bad24d36a16286
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326512"
---
# <a name="shapeplacestyle-cell-shape-layout-section"></a>Celda ShapePlaceStyle (Sección de diseño de la forma)

Especifica cómo se colocan las formas en la página cuando se disponen las formas en el cuadro de diálogo **configurar diseño** (en la ficha **diseño** , en el grupo **diseño** , haga clic en **redistribuir página**y, a continuación, haga clic en **más opciones de diseño**). Almacena los valores de estilo y alineación del diseño desde **VisCellIndices**. 
  
|**Constante**|**Valor**|
|:-----|:-----|
|**visLOPlaceBottomToTop** <br/> |4  <br/> |
|**visLOPlaceCircular** <br/> |6,5  <br/> |
|**visLOPlaceCompactDownLeft** <br/> |apartado  <br/> |
|**visLOPlaceCompactDownRight** <br/> |0,7  <br/> |
|**visLOPlaceCompactLeftDown** <br/> |apartado  <br/> |
|**visLOPlaceCompactLeftUp** <br/> |12  <br/> |
|**visLOPlaceCompactRightDown** <br/> |8,5  <br/> |
|**visLOPlaceCompactRightUp** <br/> |9  <br/> |
|**visLOPlaceCompactUpLeft** <br/> |12  <br/> |
|**visLOPlaceCompactUpRight** <br/> |metros  <br/> |
|**visLOPlaceDefault** <br/> |comprendi  <br/> |
|**visLOPlaceHierarchyBottomToTopCenter** <br/> |20  <br/> |
|**visLOPlaceHierarchyBottomToTopLeft** <br/> |18  <br/> |
|**visLOPlaceHierarchyBottomToTopRight** <br/> |21  <br/> |
|**visLOPlaceHierarchyLeftToRightBottom** <br/> |apartado  <br/> |
|**visLOPlaceHierarchyLeftToRightMiddle** <br/> |veintitrés  <br/> |
|**visLOPlaceHierarchyLeftToRightTop** <br/> |22  <br/> |
|**visLOPlaceHierarchyRightToLeftBottom** <br/> |,27  <br/> |
|**visLOPlaceHierarchyRightToLeftMiddle** <br/> |apartado  <br/> |
|**visLOPlaceHierarchyRightToLeftTop** <br/> |IVA  <br/> |
|**visLOPlaceHierarchyTopToBottomCenter** <br/> |432  <br/> |
|**visLOPlaceHierarchyTopToBottomLeft** <br/> |16  <br/> |
|**visLOPlaceHierarchyTopToBottomRight** <br/> |dieciocho  <br/> |
|**visLOPlaceLeftToRight** <br/> |segundo  <br/> |
|**visLOPlaceParentDefault** <br/> |15  <br/> |
|**visLOPlaceRadial** <br/> |3  <br/> |
|**visLOPlaceRightToLeft** <br/> |2,5  <br/> |
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
   

