---
title: Celda ShapePermeableY (Sección de diseño de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251666
localization_priority: Normal
ms.assetid: 90701ecf-3d34-2eac-9ee9-7965e16c0f7c
description: Determina si un conector puede enrutar verticalmente a través de una forma.
ms.openlocfilehash: 4a7a389ec1d753b8582b7ff0b921a615e582b1ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823146"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a>Celda ShapePermeableY (Sección de diseño de forma)

Determina si un conector puede enrutar verticalmente a través de una forma.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Se permite que los conectores enruten verticalmente a través de una forma.  <br/> |
|FALSE  <br/> |No se permite que los conectores enruten verticalmente a través de una forma.  <br/> |
   
## <a name="remarks"></a>Observaciones

También puede establecer el valor de esta celda en la ficha de **colocación** en el cuadro de diálogo **comportamiento** (con una forma seleccionada, en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) , en el grupo **Diseño de formas** , haga clic en **comportamiento**y, a continuación, haga clic en la ficha **colocación** ). 
  
En las versiones anteriores a Visio 2000, este comportamiento se establece mediante la celda ObjInteract, en la sección de varios.
  
Para obtener una referencia a la celda ShapePermeableY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ShapePermeableY  <br/> |
   
Para obtener una referencia a la celda ShapePermeableY por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
|Índice de celda:  <br/> |**visSLOPermY** <br/> |
   

