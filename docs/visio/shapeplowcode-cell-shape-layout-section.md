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
ms.openlocfilehash: 5917abad653e7aaf40da05eafa3f9f1a90a2cf9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823169"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a>Celda ShapePlowCode (sección Diseño de forma)

Determina si esta forma colocable se quita al colocar junto a ella otra forma colocable en la página de dibujo.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Se quita tal como especifique la página.  <br/> |**visSLOPlowDefault** <br/> |
|1  <br/> |No se quita ninguna forma.  <br/> |**visSLOPlowNever** <br/> |
|2  <br/> |Se quitan todas las formas.  <br/> |**visSLOPlowAlways** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer el valor de esta celda para una forma determinada en la ficha de **colocación** en el cuadro de diálogo **comportamiento** (con una forma seleccionada, en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) , en el grupo **Diseño de formas** , haga clic en **comportamiento**y, a continuación, haga clic en el Ficha **colocación** ). 
  
Para establecer este comportamiento para *todas* las formas en la página de dibujo, utilice la celda PlowCode de la sección de diseño de página. 
  
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
   

