---
title: Celda ShapePlaceFlip (Sección de diseño de la forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253247
localization_priority: Normal
ms.assetid: 40008507-d9e4-9c0e-603f-d5e6da73a94b
description: Determina de qué manera se voltea o se rota una forma colocable en la página cuando se diseñan las formas mediante el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en Redistribuir página y, a continuación, en Más opciones de diseño).
ms.openlocfilehash: 72ef1b67dd87d842e6a4372d1eb08d614f0eb2d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429281"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a>Celda ShapePlaceFlip (Sección de diseño de la forma)

Determina de qué manera se voltea o se rota una forma colocable en la página cuando se diseñan las formas mediante el cuadro de diálogo **Configurar diseño** (en la ficha **Diseño**, en el grupo **Diseño**, haga clic en **Redistribuir página** y, a continuación, en **Más opciones de diseño**).
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Se utilizan las opciones predeterminadas de la página.  <br/> |**visLOFlipDefault** <br/> |
|1  <br/> |Se voltea horizontalmente.  <br/> |**visLOFlipX** <br/> |
|2  <br/> |Se voltea verticalmente.  <br/> |**visLOFlipY** <br/> |
|4   <br/> |Se voltea en incrementos de 90 grados entre 0 y 270.  <br/> |**visLOFlipRotate** <br/> |
|8   <br/> |No se voltea.  <br/> |**visLOFlipNone** <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de la celda ShapePlaceFlip ayuda a orientar una forma colocable hacia la siguiente forma colocable a la que esté conectada.
  
Para establecer este comportamiento para  *todas las*  formas de la página de dibujo, use la celda PlaceFlip de la sección Diseño de página. 
  
Para obtener una referencia a la celda ShapePlaceFlip por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ShapePlaceFlip  <br/> |
   
Para obtener una referencia a la celda ShapePlaceFlip por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
|Índice de celda:  <br/> |**visSLOPlaceFlip** <br/> |
   

