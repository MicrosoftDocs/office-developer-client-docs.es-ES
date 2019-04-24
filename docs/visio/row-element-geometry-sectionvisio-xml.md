---
title: Elemento Row (sección geometría) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2b273958-1997-7c63-4a61-d231f023a81f
description: Contiene filas que muestran las coordenadas de los vértices de las líneas y los arcos que constituyen la forma.
ms.openlocfilehash: 53482b0db3f2deb3c8e2ba30f41be67f0d9e27a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358558"
---
# <a name="row-element-geometry-section-visio-xml"></a>Elemento Row (sección geometría) ("XML" de Visio)

Contiene filas que muestran las coordenadas de los vértices de las líneas y los arcos que constituyen la forma.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[GeometryRow_Type](geometry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Master #. XML, página #. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Row" type="GeometryRow_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Contiene filas que muestran las coordenadas de los vértices de las líneas y los arcos que constituyen la forma.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

> [!NOTE]
> El elemento cell es el único elemento secundario de este elemento. Según el atributo "T" de este elemento, el significado de los elementos de celda son distintos. En la siguiente tabla, parathetical texto en el nombre del elemento corresponde al valor "T" al que se aplica el tema. 
  
|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Elemento Cell (fila ArcTo)](arcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y, y la curvatura de un arco circular.  <br/> |
|[Elemento Cell (fila Elipse)](ellipse-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del punto central y de dos puntos más de la elipse.  <br/> |
|[Elemento Cell (fila EllipticalArcTo)](ellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del extremo de un arco elíptico, las coordenadas x e y de los puntos de control del arco, el ángulo desde el eje x hasta el eje mayor de la elipse y la relación entre los ejes mayor y menor de la elipse.  <br/> |
|[Elemento Cell (fila InfiniteLine)](infiniteline-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y de dos puntos en una línea infinita.  <br/> |
|[Elemento Cell (fila LineTo)](lineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del vértice del extremo de un segmento de línea recta.  <br/> |
|[Elemento Cell (fila MoveTo)](moveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del primer vértice de una forma o representa las coordenadas x e y del primer vértice después de una interrupción de una trayectoria.  <br/> |
|[Elemento Cell (fila NURBSTo)](nurbsto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y, la posición del segundo al último nodo, la posición del último grosor, la posición del primer nodo, la posición del primer grosor y la fórmula de una spline B racional no uniforme (NURBS).  <br/> |
|[Elemento Cell (fila PolyLineTo)](polylineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del último punto de una polilínea y una fórmula de polilínea.  <br/> |
|[Elemento Cell (fila RelCubBezTo)](relcubbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del punto final de una curva Bézier cúbica en relación con el ancho y el alto de la forma, las coordenadas x e y del punto de control del principio del ancho y el alto de la forma relativa de la curva, y las coordenadas x-e y-del control. punto de final del ancho y alto de la forma relativa de la curva.  <br/> |
|[Elemento Cell (fila RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del punto final de una curva Bézier cuadrática en relación con el ancho y el alto de la forma y las coordenadas x e y del punto de control del ancho y alto de la forma relativa de la curva.  <br/> |
|[Elemento Cell (fila RelEllipticalArcTo)](relellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del extremo de un arco elíptico en relación con el ancho y el alto de la forma, las coordenadas x e y de los puntos de control del arco con respecto al ancho y el alto de la forma, el ángulo desde el eje x hasta el eje principal de la elipse y la relación entre los ejes mayor y menor de la elipse.  <br/> |
|[Elemento Cell (fila RelLineTo)](rellineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del vértice del extremo de un segmento de línea recta con relación al ancho y el alto de la forma.  <br/> |
|[Elemento Cell (fila RelMoveTo)](relmoveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del primer vértice de una forma o las coordenadas x-e y del primer vértice después de una interrupción en una ruta de acceso, en relación con el alto y ancho de la forma.  <br/> |
|[Elemento Cell (fila RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del punto final de una curva Bézier cuadrática en relación con el ancho y el alto de la forma y las coordenadas x e y del punto de control del ancho y alto de la forma relativa de la curva.  <br/> |
|[Elemento Cell (fila SplineKnot)](splineknot-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del punto de control y de un nodo de una spline.  <br/> |
|[Elemento Cell (fila SplineStart)](splinestart-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del segundo punto de control de una spline, sus nodos segundo, primero y último, y el grado de la spline.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Especifica si se ha eliminado una fila que, de lo contrario, se heredaría de una forma de patrón.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|IX  <br/> |xsd: unsignedInt  <br/> |opcional  <br/> |Especifica el identificador de base uno de la fila. Debe ser único y mayor que otros identificadores de la misma sección. El atributo IX solo se usa para las secciones character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, paraGraph, Reviewer, Scratch y Tabs. Una fila sólo puede tener uno de los atributos IX o N.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|LocalName  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el nombre único dependiente del idioma de la fila.  <br/> |Valores del tipo xsd: String.  <br/> |
|N  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el nombre único independiente del idioma de la fila. El atributo N solo se usa para las secciones User, Property, Actions, control, Connection, HYPERLINK y ActionTag. Una fila sólo puede tener uno de los atributos IX o N.  <br/> |Valores del tipo xsd: String.  <br/> |
|T  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el tipo de la ruta geométrica representada por la fila y utilizada en la visualización de geometría. El atributo T solo se usa para la sección Geometry.  <br/> |Valores del tipo xsd: String.  <br/> |
   
## <a name="remarks"></a>Comentarios

El atributo **T** de este elemento **Row** debe ser uno de un conjunto limitado de valores que corresponden a las filas de ShapeSheet. Consulte la tabla siguiente para determinar los valores del atributo **T** que se permiten para este elemento **Row** . 
  
|**Value**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|ArcTo  <br/> |Contiene las coordenadas x e y, y la curvatura de un arco circular.  <br/> |[Fila ArcTo (Sección de geometría)](arcto-row-geometry-section.md) <br/> |
|Origina  <br/> |Contiene las coordenadas x e y del punto central y de dos puntos más de la elipse.  <br/> |[Fila Ellipse (Sección de Geometría)](ellipse-row-geometry-section.md) <br/> |
|EllipticalArcTo  <br/> |Contiene las coordenadas x e y del extremo de un arco elíptico, las coordenadas x e y de los puntos de control del arco, el ángulo desde el eje x hasta el eje mayor de la elipse y la relación entre los ejes mayor y menor de la elipse.  <br/> |[Fila EllipticalArcTo (Sección de Geometría)](ellipticalarcto-row-geometry-section.md) <br/> |
|InfiniteLine  <br/> |Contiene las coordenadas x e y de dos puntos en una línea infinita.  <br/> |[Fila InfiniteLine (Sección de Geometría)](infiniteline-row-geometry-section.md) |
|LineTo  <br/> |Contiene las coordenadas x e y del vértice del extremo de un segmento de línea recta.  <br/> |[Fila LineTo (Sección de Geometría)](lineto-row-geometry-section.md) <br/> |
|MoveTo  <br/> |Contiene las coordenadas x e y del primer vértice de una forma o representa las coordenadas x e y del primer vértice después de una interrupción de una trayectoria.  <br/> |[Fila MoveTo (Sección de Geometría)](moveto-row-geometry-section.md) <br/> |
|NURBSTo  <br/> |Contiene las coordenadas x e y, la posición del segundo al último nodo, la posición del último grosor, la posición del primer nodo, la posición del primer grosor y la fórmula de una spline B racional no uniforme (NURBS).  <br/> |[Fila NURBSTo (Sección de Geometría)](nurbsto-row-geometry-section.md) <br/> |
|PolylineTo  <br/> |Contiene las coordenadas x e y del último punto de una polilínea y una fórmula de polilínea.  <br/> |[Fila PolylineTo (Sección de Geometría)](polylineto-row-geometry-section.md) <br/> |
|RelCubBezTo  <br/> |Contiene las coordenadas x e y del punto final de una curva Bézier cúbica en relación con el ancho y el alto de la forma, las coordenadas x e y del punto de control del principio del ancho y el alto de la forma relativa de la curva, y las coordenadas x-e y-del control. punto de final del ancho y alto de la forma relativa de la curva.  <br/> |[Fila RelCubBezTo (sección geometría)](relcubbezto-row-geometry-section.md) <br/> |
|RelEllipticalArcTo  <br/> |Contiene las coordenadas x e y del extremo de un arco elíptico en relación con el ancho y el alto de la forma, las coordenadas x e y de los puntos de control del arco con respecto al ancho y el alto de la forma, el ángulo desde el eje x hasta el eje principal de la elipse y la relación entre los ejes mayor y menor de la elipse.  <br/> |[Fila RelEllipticalArcTo (sección geometría)](relellipticalarcto-row-geometry-section.md) <br/> |
|RelLineTo  <br/> |Contiene las coordenadas x e y del vértice del extremo de un segmento de línea recta con relación al ancho y el alto de la forma.  <br/> |[Fila RelLineTo (sección geometría)](rellineto-row-geometry-section.md) <br/> |
|RelMoveTo  <br/> |Contiene las coordenadas x e y del primer vértice de una forma o las coordenadas x-e y del primer vértice después de una interrupción en una ruta de acceso, en relación con el alto y ancho de la forma.  <br/> |[Fila RelMoveTo (sección geometría)](relmoveto-row-geometry-section.md) <br/> |
|RelQuadBezTo  <br/> |Contiene las coordenadas x e y del punto final de una curva Bézier cuadrática en relación con el ancho y el alto de la forma y las coordenadas x e y del punto de control del ancho y alto de la forma relativa de la curva.  <br/> |[Fila RelQuadBezTo (sección geometría)](relquadbezto-row-geometry-section.md) <br/> |
|SplineKnot  <br/> |Contiene las coordenadas x e y del punto de control y de un nodo de una spline.  <br/> |[Fila SplineKnot (Sección de Geometría)](splineknot-row-geometry-section.md) <br/> |
|SplineStart  <br/> |Contiene las coordenadas x e y del segundo punto de control de una spline, sus nodos segundo, primero y último, y el grado de la spline.  <br/> |[Fila SplineStart (Sección de Geometría)](splinestart-row-geometry-section.md) <br/> |
   

