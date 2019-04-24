---
title: Celda PlaceFlip (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253251
localization_priority: Normal
ms.assetid: df014b98-cfd5-b6d3-4b8a-b0acb3b94412
description: Determina de qué manera se voltean o rotan las formas colocables en una página al usar el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en Redistribuir página y, a continuación, en Más opciones de diseño).
ms.openlocfilehash: d1c31654782012b3536d35f3a12a923c2cc7a8f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346875"
---
# <a name="placeflip-cell-page-layout-section"></a>Celda PlaceFlip (Sección de diseño de página)

Determina de qué manera se voltean o rotan las formas colocables en una página al usar el cuadro de diálogo **Configurar diseño** (en la ficha **Diseño**, en el grupo **Diseño**, haga clic en **Redistribuir página** y, a continuación, en **Más opciones de diseño**).
  
|**Value**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|&amp;H0  <br/> |Éste es el valor predeterminado. No se voltea.  <br/> |**visLOFlipDefault** <br/> |
|&amp;H1  <br/> |Se voltea horizontalmente.  <br/> |**visLOFlipX** <br/> |
|&amp;H2  <br/> |Se voltea verticalmente.  <br/> |**visLOFlipY** <br/> |
|&amp;H4  <br/> |Se voltea en incrementos de 90 grados.  <br/> |**visLOFlipRotate** <br/> |
|&amp;H8  <br/> |No se voltea.  <br/> |**visLOFlipNone** <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de la celda PlaceFlip ayuda a orientar una forma colocable hacia la siguiente forma colocable a la que está conectada. Suele emplearse cuando se diseñan dibujos que precisan pegado estático.
  
Para establecer este comportamiento para una forma en particular, use la celda ShapePlaceFlip en la sección de diseño de la forma.
  
Para obtener una referencia a la celda PlaceFlip por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |PlaceFlip  <br/> |
   
Para obtener una referencia desde un programa a la celda PlaceFlip por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPageLayout** <br/> |
|Índice de celda:  <br/> |**visPLOPlaceFlip** <br/> |
   

