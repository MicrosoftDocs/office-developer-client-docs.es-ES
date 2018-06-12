---
title: Sección de geometría
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2055
localization_priority: Normal
ms.assetid: 75601a1e-6b1a-27ee-a2bd-69e569315982
description: Contiene filas que enumeran las coordenadas de los vértices de las líneas y arcos que constituyen la forma.
ms.openlocfilehash: 59f85c512b7038f6cfddcb657435730a2e724bd6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822216"
---
# <a name="geometry-section"></a>Sección de geometría

Contiene filas que enumeran las coordenadas de los vértices de las líneas y arcos que constituyen la forma. 
  
La geometría de una forma se puede expresar en varias secciones de **geometría** . Varias rutas de acceso pueden ser útiles cuando varias rutas de acceso tienen propiedades diferentes (por ejemplo, las rutas de acceso de [recorte de imágenes](clippingpath-cell-foreign-image-info-section.md) ). 
  
## <a name="remarks"></a>Notas

La sección de **geometría** contiene los siguientes tipos de fila. Para obtener información detallada, vea los temas de la fila. 
  
|**Row**|**Descripción**|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> |Va a una coordenada.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> |Dibuja una línea en una coordenada.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> |Dibuja un arco circular en una coordenada.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> |Dibuja un arco elíptico en una coordenada.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> |Dibuja una polilínea, o líneas consecutivas, en una coordenada.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> |Dibuja una no uniforme spline B racional (NURBS) una coordenada.  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> |Inicia una spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> |Dibuja un segmento de spline en la coordenada de un nodo.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> |Dibuja una línea infinita de una coordenada a otra.  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> |Dibuja una elipse a partir de una coordenada central y unos ejes mayor y menor.  <br/> |
|[RelCubBezTo](relcubbezto-row-geometry-section.md) <br/> |Dibujar una curva Bézier cúbica en relación con el ancho y el alto de la forma.  <br/> |
|[RelEllipticalArcTo](relellipticalarcto-row-geometry-section.md) <br/> |Dibuja un arco elíptico en una coordenada en relación con el alto y el ancho de la forma.  <br/> |
|[RelLineTo](rellineto-row-geometry-section.md) <br/> |Dibuja una línea a una coordenada relativa el alto y el ancho de una forma.  <br/> |
|[RelMoveTo](relmoveto-row-geometry-section.md) <br/> |Mover a una coordenada en relación con el ancho y el alto de la forma.  <br/> |
|[RelQuadBezTo](relquadbezto-row-geometry-section.md) <br/> |Dibuja una curva Bézier cuadrática en relación con el ancho y el alto de la forma.  <br/> |
   
Para cambiar un tipo de fila en esta sección, haga clic en la fila y, a continuación, haga clic en **Cambiar tipo de fila** en el menú contextual. 
  

