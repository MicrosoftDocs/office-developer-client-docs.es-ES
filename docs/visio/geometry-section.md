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
description: Contiene filas que muestran las coordenadas de los vértices de las líneas y los arcos que constituyen la forma.
ms.openlocfilehash: d45f960ecc697dc6f0f5a0efa18e6cbbc6e4fff0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542286"
---
# <a name="geometry-section"></a>Sección de geometría

Contiene filas que muestran las coordenadas de los vértices de las líneas y los arcos que constituyen la forma. 
  
La geometría de una forma se puede expresar en varias secciones **de** geometría. Varias rutas de acceso pueden ser útiles cuando varias rutas de acceso tienen propiedades diferentes (por ejemplo, rutas de recorte [de](clippingpath-cell-foreign-image-info-section.md) imágenes). 
  
## <a name="remarks"></a>Comentarios

La **sección Geometría** contiene los siguientes tipos de fila. Para obtener más detalles, vea los temas acerca de las filas. 
  
|Fila|Description|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> |Va a una coordenada.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> |Dibuja una línea en una coordenada.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> |Dibuja un arco circular en una coordenada.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> |Dibuja un arco elíptico en una coordenada.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> |Dibuja una polilínea, o líneas consecutivas, en una coordenada.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> |Dibuja una spline B racional no uniforme (NURBS) en una coordenada.  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> |Inicia una spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> |Dibuja un segmento de spline en la coordenada de un nodo.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> |Dibuja una línea infinita de una coordenada a otra.  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> |Dibuja una elipse a partir de una coordenada central y unos ejes mayor y menor.  <br/> |
|[RelMtBezTo](relcubbezto-row-geometry-section.md) <br/> |Dibuja una curva Bézier cúbica con relación al ancho y alto de la forma.  <br/> |
|[RelEllipticalArcTo](relellipticalarcto-row-geometry-section.md) <br/> |Dibuja un arco elíptico en una coordenada con relación al alto y ancho de la forma.  <br/> |
|[RelLineTo](rellineto-row-geometry-section.md) <br/> |Dibujar una línea a una coordenada relativa al alto y ancho de una forma.  <br/> |
|[RelMoveTo](relmoveto-row-geometry-section.md) <br/> |Desplazarse a una coordenada relativa al ancho y alto de la forma.  <br/> |
|[RelQuadBezTo](relquadbezto-row-geometry-section.md) <br/> |Dibuja una curva Bézier cuadrática con relación al ancho y alto de la forma.  <br/> |
   
Para cambiar un tipo de fila en esta sección, haga clic con el botón secundario en la fila y, a continuación, haga clic en Cambiar tipo de fila **en** el menú contextual. 
  

