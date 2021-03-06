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
ms.openlocfilehash: 62f8bfa0fdfb5c483836f344e8b784dc9092fded
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417521"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a>Celda ShapePermeableY (Sección de diseño de forma)

Determina si un conector puede enrutar verticalmente a través de una forma.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Se permite que los conectores enruten verticalmente a través de una forma.  <br/> |
|FALSE  <br/> |No se permite que los conectores enruten verticalmente a través de una forma.  <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer el valor de  esta celda en la ficha Ubicación del [](run-in-developer-mode-display-the-developer-tab.md) cuadro de diálogo Comportamiento (con una forma seleccionada, en la ficha Programador, en el grupo Diseño de formas, haga clic en Comportamiento y, a continuación, haga clic en la pestaña Ubicación).    
  
En las versiones anteriores a Visio 2000, este comportamiento se establece mediante la celda ObjInteract, en la sección de varios.
  
Para obtener una referencia a la celda ShapePermeableY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ShapePermeableY  <br/> |
   
Para obtener una referencia desde un programa a la celda ShapePermeableY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
|Índice de celda:  <br/> |**visSLOPermY** <br/> |
   

