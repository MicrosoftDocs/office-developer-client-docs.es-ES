---
title: Celda ShapePlowCode (Sección de diseño de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm900
localization_priority: Normal
ms.assetid: acf07fd7-6aa6-1a92-9b7a-bd6fea8a7cb2
description: Determina si esta forma colocable se quita al colocar junto a ella otra forma colocable en la página de dibujo.
ms.openlocfilehash: 6e155103f7bfc70a78826297f441fc9ce78942ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325609"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a>Celda ShapePlowCode (Sección de diseño de forma)

Determina si esta forma colocable se quita al colocar junto a ella otra forma colocable en la página de dibujo.
  
|**Value**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|comprendi  <br/> |Se quita tal como especifique la página.  <br/> |**visSLOPlowDefault** <br/> |
|1  <br/> |No se quita ninguna forma.  <br/> |**visSLOPlowNever** <br/> |
|segundo  <br/> |Se quitan todas las formas.  <br/> |**visSLOPlowAlways** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer el valor de esta celda para una forma determinada en la ficha **colocación** del cuadro de diálogo **comportamiento** (seleccione una forma, en la ficha [programador](run-in-developer-mode-display-the-developer-tab.md) , en el grupo **diseño de formas** , haga clic en **comportamiento**y, a continuación, haga clic en el Ficha **colocación** ). 
  
Para establecer este comportamiento para *todas* las formas de la página de dibujo, utilice la celda PlowCode de la sección de diseño de página. 
  
Para obtener una referencia a la celda ShapePlowCode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ShapePlowCode  <br/> |
   
Para obtener una referencia desde un programa a la celda ShapePlowCode por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
|Índice de celda:  <br/> |**visSLOPlowCode** <br/> |
   

