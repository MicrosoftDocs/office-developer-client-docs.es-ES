---
title: Celda RouteStyle (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251662
localization_priority: Normal
ms.assetid: 3a223dac-538b-cb5d-a32d-61395276f9da
description: Determina el estilo y la dirección de enrutamiento de todos los conectores de la página de dibujo que no tengan un estilo de enrutamiento local.
ms.openlocfilehash: 38de871460c155ee5d495599a239ebeb0ff1c33d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424787"
---
# <a name="routestyle-cell-page-layout-section"></a>Celda RouteStyle (Sección de diseño de página)

Determina el estilo y la dirección de enrutamiento de todos los conectores de la página de dibujo que no tengan un estilo de enrutamiento local.
  
|**Valor**|**Enrutamiento, estilo**|**Direction**|**Constante de automatización**|
|:-----|:-----|:-----|:-----|
|comprendi  <br/> |Predeterminado; ángulo recto  <br/> |Ninguna  <br/> |**visLORouteDefault** <br/> |
|1  <br/> |Ángulo recto  <br/> |Ninguna  <br/> |**visLORouteRightAngle** <br/> |
|segundo  <br/> |Directas  <br/> |Ninguna  <br/> |**visLORouteStraight** <br/> |
|3  <br/> |Organigrama  <br/> |De arriba abajo  <br/> |**visLORouteOrgChartNS** <br/> |
|4   <br/> |Organigrama  <br/> |De izquierda a derecha  <br/> |**visLORouteOrgChartWE** <br/> |
|5   <br/> |Diagrama de flujo  <br/> |De arriba abajo  <br/> |**visLORouteFlowchartNS** <br/> |
|6   <br/> |Diagrama de flujo  <br/> |De izquierda a derecha  <br/> |**visLORouteFlowchartWE** <br/> |
|7   <br/> |Árboles  <br/> |De arriba abajo  <br/> |**visLORouteTreeNS** <br/> |
|8   <br/> |Árboles  <br/> |De izquierda a derecha  <br/> |**visLORouteTreeWE** <br/> |
|9   <br/> |Red  <br/> |Ninguna  <br/> |**visLORouteNetwork** <br/> |
|10   <br/> |Organigrama  <br/> |De abajo arriba  <br/> |**visLORouteOrgChartSN** <br/> |
|11   <br/> |Organigrama  <br/> |De derecha a izquierda  <br/> |**visLORouteOrgChartEW** <br/> |
|12  <br/> |Diagrama de flujo  <br/> |De abajo arriba  <br/> |**visLORouteFlowchartSN** <br/> |
|13   <br/> |Diagrama de flujo  <br/> |De derecha a izquierda  <br/> |**visLORouteFlowchartEW** <br/> |
|14   <br/> |Árboles  <br/> |De abajo arriba  <br/> |**visLORouteTreeSN** <br/> |
|15   <br/> |Árboles  <br/> |De derecha a izquierda  <br/> |**visLORouteTreeEW** <br/> |
|16   <br/> |De centro a centro  <br/> |Ninguna  <br/> |**visLORouteCenterToCenter** <br/> |
|17   <br/> |Simple  <br/> |De arriba abajo  <br/> |**visLORouteSimpleNS** <br/> |
|18   <br/> |Simple  <br/> |De izquierda a derecha  <br/> |**visLORouteSimpleWE** <br/> |
|18  <br/> |Simple  <br/> |De abajo arriba  <br/> |**visLORouteSimpleSN** <br/> |
|20  <br/> |Simple  <br/> |De derecha a izquierda  <br/> |**visLORouteSimpleEW** <br/> |
|21  <br/> |Horizontal-vertical simple  <br/> |Ninguna  <br/> |**visLORouteSimpleHV** <br/> |
|22  <br/> |Vertical-horizontal simple  <br/> |Ninguna  <br/> |**visLORouteSimpleVH** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer el valor de esta celda en la ficha **diseño y enrutamiento** del cuadro de diálogo **Configurar página** (en la ficha **diseño** , haga clic en la flecha **Configurar página** , haga clic en **diseño y enrutamiento**y, a continuación, haga clic en **espaciado** ). 
  
Puede establecer un estilo de enrutamiento local para un conector en la celda ShapeRouteStyle de la sección de diseño de la forma. 
  
Para obtener una referencia a la celda RouteStyle por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |RouteStyle  <br/> |
   
Para obtener una referencia a la celda RouteStyle por su índice desde un programa, use la propiedad **CellsSRC** con los siguientes argumentos: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPageLayout** <br/> |
|Índice de celda:  <br/> |**visPLORouteStyle** <br/> |
   

