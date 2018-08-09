---
title: Celda ShapeRouteStyle (Sección de diseño de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm905
localization_priority: Normal
ms.assetid: a5dcd2e0-e343-5ee2-2b63-2a1312437901
description: Determina el estilo y la dirección de enrutamiento del conector seleccionado en la página de dibujo.
ms.openlocfilehash: b165d43e64842565806d93d620ddbd24f41a2d57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823164"
---
# <a name="shaperoutestyle-cell-shape-layout-section"></a>Celda ShapeRouteStyle (sección Diseño de forma)

Determina el estilo y la dirección de enrutamiento del conector seleccionado en la página de dibujo.
  
|**Valor**|**Enrutamiento, estilo**|**Direction**|**Constante de automatización**|
|:-----|:-----|:-----|:-----|
|0  <br/> |Se utilizan las opciones predeterminadas de la página  <br/> |Ninguno  <br/> |**visLORouteDefault** <br/> |
|1  <br/> |Ángulo recto  <br/> |Ninguna  <br/> |**visLORouteRightAngle** <br/> |
|2  <br/> |Recta  <br/> |Ninguna  <br/> |**visLORouteStraight** <br/> |
|3  <br/> |Organigrama  <br/> |De arriba abajo  <br/> |**visLORouteOrgChartNS** <br/> |
|4  <br/> |Organigrama  <br/> |De izquierda a derecha  <br/> |**visLORouteOrgChartWE** <br/> |
|5  <br/> |Diagrama de flujo  <br/> |De arriba abajo  <br/> |**visLORouteFlowchartNS** <br/> |
|6  <br/> |Diagrama de flujo  <br/> |De izquierda a derecha  <br/> |**visLORouteFlowchartWE** <br/> |
|7  <br/> |Árbol  <br/> |De arriba abajo  <br/> |**visLORouteTreeNS** <br/> |
|8  <br/> |Árbol  <br/> |De izquierda a derecha  <br/> |**visLORouteTreeWE** <br/> |
|9  <br/> |Red  <br/> |Ninguna  <br/> |**visLORouteNetwork** <br/> |
|10  <br/> |Organigrama  <br/> |De abajo arriba  <br/> |**visLORouteOrgChartSN** <br/> |
|11  <br/> |Organigrama  <br/> |De derecha a izquierda  <br/> |**visLORouteOrgChartEW** <br/> |
|12  <br/> |Diagrama de flujo  <br/> |De abajo arriba  <br/> |**visLORouteFlowchartSN** <br/> |
|13  <br/> |Diagrama de flujo  <br/> |De derecha a izquierda  <br/> |**visLORouteFlowchartEW** <br/> |
|14  <br/> |Árbol  <br/> |De abajo arriba  <br/> |**visLORouteTreeSN** <br/> |
|15  <br/> |Árbol  <br/> |De derecha a izquierda  <br/> |**visLORouteTreeEW** <br/> |
|16  <br/> |De centro a centro  <br/> |Ninguna  <br/> |**visLORouteCenterToCenter** <br/> |
|17  <br/> |Simple  <br/> |De arriba abajo  <br/> |**visLORouteSimpleNS** <br/> |
|18  <br/> |Simple  <br/> |De izquierda a derecha  <br/> |**visLORouteSimpleWE** <br/> |
|19  <br/> |Simple  <br/> |De abajo arriba  <br/> |**visLORouteSimpleSN** <br/> |
|20  <br/> |Simple  <br/> |De derecha a izquierda  <br/> |**visLORouteSimpleEW** <br/> |
|21  <br/> |Horizontal-vertical simple  <br/> |Ninguna  <br/> |**visLORouteSimpleHV** <br/> |
|22  <br/> |Vertical-horizontal simple  <br/> |Ninguna  <br/> |**visLORouteSimpleVH** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer el valor de esta celda para un conector determinado en la ficha **conector** en el cuadro de diálogo **comportamiento** (con un conector, haga clic en **comportamiento** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, haga clic en la ficha **conector** ). 
  
Para establecer este comportamiento para *todos* los conectores en una página, utilice la celda RouteStyle de la sección de diseño de página. 
  
En las versiones anteriores a Visio 2000, este comportamiento se establece mediante la celda ObjBehavior, en la sección de varios.
  
Para obtener una referencia a la celda ShapeRouteStyle por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Celda ShapeRouteStyle  <br/> |
   
Para obtener una referencia desde un programa a la celda ShapeRouteStyle por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
|Índice de celda:  <br/> |**visSLORouteStyle** <br/> |
   

