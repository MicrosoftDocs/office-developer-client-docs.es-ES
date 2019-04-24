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
ms.openlocfilehash: e5725d461a71dad4623161d99134a20250abe724
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326526"
---
# <a name="shaperoutestyle-cell-shape-layout-section"></a>Celda ShapeRouteStyle (Sección de diseño de forma)

Determina el estilo y la dirección de enrutamiento del conector seleccionado en la página de dibujo.
  
|**Value**|**Enrutamiento, estilo**|**Direction**|**Constante de automatización**|
|:-----|:-----|:-----|:-----|
|comprendi  <br/> |Se utilizan las opciones predeterminadas de la página  <br/> |Ninguno  <br/> |**visLORouteDefault** <br/> |
|1  <br/> |Ángulo recto  <br/> |Ninguno  <br/> |**visLORouteRightAngle** <br/> |
|segundo  <br/> |Directas  <br/> |Ninguno  <br/> |**visLORouteStraight** <br/> |
|3  <br/> |Organigrama  <br/> |De arriba abajo  <br/> |**visLORouteOrgChartNS** <br/> |
|4  <br/> |Organigrama  <br/> |De izquierda a derecha  <br/> |**visLORouteOrgChartWE** <br/> |
|2,5  <br/> |Diagrama de flujo  <br/> |De arriba abajo  <br/> |**visLORouteFlowchartNS** <br/> |
|6,5  <br/> |Diagrama de flujo  <br/> |De izquierda a derecha  <br/> |**visLORouteFlowchartWE** <br/> |
|0,7  <br/> |Árboles  <br/> |De arriba abajo  <br/> |**visLORouteTreeNS** <br/> |
|8,5  <br/> |Árboles  <br/> |De izquierda a derecha  <br/> |**visLORouteTreeWE** <br/> |
|9  <br/> |Red  <br/> |Ninguno  <br/> |**visLORouteNetwork** <br/> |
|metros  <br/> |Organigrama  <br/> |De abajo arriba  <br/> |**visLORouteOrgChartSN** <br/> |
|12  <br/> |Organigrama  <br/> |De derecha a izquierda  <br/> |**visLORouteOrgChartEW** <br/> |
|12  <br/> |Diagrama de flujo  <br/> |De abajo arriba  <br/> |**visLORouteFlowchartSN** <br/> |
|apartado  <br/> |Diagrama de flujo  <br/> |De derecha a izquierda  <br/> |**visLORouteFlowchartEW** <br/> |
|apartado  <br/> |Árboles  <br/> |De abajo arriba  <br/> |**visLORouteTreeSN** <br/> |
|15  <br/> |Árboles  <br/> |De derecha a izquierda  <br/> |**visLORouteTreeEW** <br/> |
|16  <br/> |De centro a centro  <br/> |Ninguno  <br/> |**visLORouteCenterToCenter** <br/> |
|432  <br/> |Simple  <br/> |De arriba abajo  <br/> |**visLORouteSimpleNS** <br/> |
|dieciocho  <br/> |Simple  <br/> |De izquierda a derecha  <br/> |**visLORouteSimpleWE** <br/> |
|18  <br/> |Simple  <br/> |De abajo arriba  <br/> |**visLORouteSimpleSN** <br/> |
|20  <br/> |Simple  <br/> |De derecha a izquierda  <br/> |**visLORouteSimpleEW** <br/> |
|21  <br/> |Horizontal-vertical simple  <br/> |Ninguno  <br/> |**visLORouteSimpleHV** <br/> |
|22  <br/> |Vertical-horizontal simple  <br/> |Ninguno  <br/> |**visLORouteSimpleVH** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer el valor de esta celda para un conector determinado en la ficha **conector** en el cuadro de diálogo **comportamiento** (seleccione un conector, haga clic en **comportamiento** en la ficha [programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, haga clic en la pestaña **conector** ). 
  
Para establecer este comportamiento para *todos* los conectores de una página, utilice la celda RouteStyle de la sección de diseño de página. 
  
En las versiones anteriores a Visio 2000, este comportamiento se establece mediante la celda ObjBehavior, en la sección de varios.
  
Para obtener una referencia a la celda ShapeRouteStyle por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ShapeRouteStyle  <br/> |
   
Para obtener una referencia desde un programa a la celda ShapeRouteStyle por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
|Índice de celda:  <br/> |**visSLORouteStyle** <br/> |
   

