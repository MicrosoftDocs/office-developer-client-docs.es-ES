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
ms.openlocfilehash: 76941b9c50e6f2c68ea9abf54e81dcd18be13a70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823156"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a>Celda ShapePlaceFlip (sección Diseño de forma)

Determina de qué manera se voltea o se rota una forma colocable en la página cuando se diseñan las formas mediante el cuadro de diálogo **Configurar diseño** (en la ficha **Diseño**, en el grupo **Diseño**, haga clic en **Redistribuir página** y, a continuación, en **Más opciones de diseño**).
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Se utilizan las opciones predeterminadas de la página.  <br/> |**visLOFlipDefault** <br/> |
|1  <br/> |Se voltea horizontalmente.  <br/> |**visLOFlipX** <br/> |
|2  <br/> |Se voltea verticalmente.  <br/> |**visLOFlipY** <br/> |
|4  <br/> |Se voltea en incrementos de 90 grados entre 0 y 270.  <br/> |**visLOFlipRotate** <br/> |
|8  <br/> |No se voltea.  <br/> |**visLOFlipNone** <br/> |
   
## <a name="remarks"></a>Observaciones

El valor de la celda ShapePlaceFlip ayuda a orientar una forma colocable hacia la siguiente forma colocable a la que esté conectada.
  
Para establecer este comportamiento para *todas* las formas en la página de dibujo, utilice la celda PlaceFlip de la sección de diseño de página. 
  
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
   

