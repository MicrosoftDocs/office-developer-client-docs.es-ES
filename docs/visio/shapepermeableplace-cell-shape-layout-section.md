---
title: Celda ShapePermeablePlace (Sección de diseño de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm885
localization_priority: Normal
ms.assetid: b647cbb5-2769-068d-bbda-2dc983c47ac9
description: Determina si las formas colocables se pueden colocar encima de una forma al diseñarlas en el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en Redistribuir página y, a continuación, en Más opciones de diseño).
ms.openlocfilehash: ceecfa25c66c3ba261865d0131a3f55ef444d5e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427223"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a>Celda ShapePermeablePlace (sección de diseño de forma)

Determina si las formas colocables se pueden colocar encima de una forma al diseñarlas en el cuadro de diálogo **Configurar diseño** (en la ficha **Diseño**, en el grupo **Diseño**, haga clic en **Redistribuir página** y, a continuación, en **Más opciones de diseño**).
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Permite que se coloquen formas encima.  <br/> |
|FALSE  <br/> |No permite que se coloquen formas encima.  <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer el valor de  esta celda en la ficha Ubicación del [](run-in-developer-mode-display-the-developer-tab.md) cuadro de diálogo Comportamiento (con una forma seleccionada, en la ficha Programador, en el grupo Diseño de formas, haga clic en Comportamiento y, a continuación, haga clic en la pestaña Ubicación).    
  
En las versiones anteriores a Visio 2000, este comportamiento se establece mediante la celda ObjInteract, en la sección de varios.
  
Para obtener una referencia a la celda ShapePermeablePlace por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ShapePermeablePlace  <br/> |
   
Para obtener una referencia desde un programa a la celda ShapePermeablePlace por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
|Índice de celda:  <br/> |**visSLOPermeablePlace** <br/> |
   

