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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332672"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a>Celda ShapePlaceFlip (Sección de diseño de la forma)

Determina de qué manera se voltea o se rota una forma colocable en la página cuando se diseñan las formas mediante el cuadro de diálogo **Configurar diseño** (en la ficha **Diseño**, en el grupo **Diseño**, haga clic en **Redistribuir página** y, a continuación, en **Más opciones de diseño**).
  
|**Value**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|comprendi  <br/> |Se utilizan las opciones predeterminadas de la página.  <br/> |**visLOFlipDefault** <br/> |
|1  <br/> |Se voltea horizontalmente.  <br/> |**visLOFlipX** <br/> |
|segundo  <br/> |Se voltea verticalmente.  <br/> |**visLOFlipY** <br/> |
|4  <br/> |Se voltea en incrementos de 90 grados entre 0 y 270.  <br/> |**visLOFlipRotate** <br/> |
|8,5  <br/> |No se voltea.  <br/> |**visLOFlipNone** <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de la celda ShapePlaceFlip ayuda a orientar una forma colocable hacia la siguiente forma colocable a la que esté conectada.
  
Para establecer este comportamiento para *todas* las formas de la página de dibujo, utilice la celda PlaceFlip de la sección de diseño de página. 
  
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
   

