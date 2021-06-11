---
title: Elemento Row (sección Geometry) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2b273958-1997-7c63-4a61-d231f023a81f
description: Contiene filas que muestran las coordenadas de los vértices de las líneas y los arcos que constituyen la forma.
ms.openlocfilehash: 6dbf18b749ed072645c4941922729010f74fc0ae
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540857"
---
# <a name="row-element-geometry-section-visio-xml"></a>Elemento Row (sección Geometry) (Visio XML)

Contiene filas que muestran las coordenadas de los vértices de las líneas y los arcos que constituyen la forma.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[GeometryRow_Type](geometry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Row" type="GeometryRow_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Contiene filas que muestran las coordenadas de los vértices de las líneas y los arcos que constituyen la forma.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

> [!NOTE]
> El elemento Cell es el único elemento secundario de este elemento. Según el atributo "T" de este elemento, el significado de los elementos Cell difiere. En la tabla siguiente, el texto paratético del nombre del elemento corresponde al valor "T" al que se aplica el tema. 
  
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
|[Elemento Cell (fila RelCubBezTo)](relcubbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del extremo de una curva bézier cúbica con relación al ancho y alto de la forma, las coordenadas x e y del punto de control del principio del ancho y alto de la forma relativa de la curva, y las coordenadas x e y del punto de control del final del ancho y alto de la forma relativa de la curva.  <br/> |
|[Elemento Cell (fila RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del extremo de una curva bézier cuadrática en relación con el ancho y alto de la forma y las coordenadas x e y del punto de control del ancho y alto relativos de la forma de curva.  <br/> |
|[Elemento Cell (fila RelEllipticalArcTo)](relellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene coordenadas x e y del extremo de un arco elíptico con relación al ancho y alto de la forma, las coordenadas x e y de los puntos de control del arco con relación al ancho y alto de la forma, el ángulo desde el eje X al eje principal de la elipse y la relación entre los ejes principales y los ejes menores de la elipse.  <br/> |
|[Elemento Cell (fila RelLineTo)](rellineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene coordenadas x e y del vértice final de un segmento de línea recta con relación al ancho y alto de una forma.  <br/> |
|[Elemento Cell (fila RelMoveTo)](relmoveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del primer vértice de una forma o las coordenadas x e y del primer vértice después de un salto en una ruta de acceso, en relación con el alto y el ancho de la forma.  <br/> |
|[Elemento Cell (fila RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del extremo de una curva bézier cuadrática en relación con el ancho y alto de la forma y las coordenadas x e y del punto de control del ancho y alto relativos de la forma de curva.  <br/> |
|[Elemento Cell (fila SplineKnot)](splineknot-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del punto de control y de un nodo de una spline.  <br/> |
|[Elemento Cell (fila SplineStart)](splinestart-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del segundo punto de control de una spline, sus nodos segundo, primero y último, y el grado de la spline.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |opcional  <br/> |Especifica si se ha eliminado una fila que se heredaría de una forma maestra.  <br/> |Valores del tipo xsd:boolean.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador único de la fila. Debe ser unqiue y mayor que otros identificadores de la misma sección. El atributo IX solo se usa para las secciones Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch y Tabs. Una fila solo puede tener uno de los atributos IX o N.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|LocalName  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica el nombre único dependiente del idioma de la fila.  <br/> |Valores del tipo xsd:string.  <br/> |
|N  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica el nombre único independiente del idioma de la fila. El atributo N solo se usa para las secciones User, Property, Actions, Control, Connection, Hyperlink y ActionTag. Una fila solo puede tener uno de los atributos IX o N.  <br/> |Valores del tipo xsd:string.  <br/> |
|T  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica el tipo de la ruta geométrica representada por la fila y usada en la visualización de geometría. El atributo T solo se usa para la sección Geometría.  <br/> |Valores del tipo xsd:string.  <br/> |
   
## <a name="remarks"></a>Comentarios

El **atributo T** de este elemento **Row** debe ser uno de un conjunto limitado de valores que corresponden a filas ShapeSheet. Consulte la tabla siguiente para determinar los valores del atributo **T** permitidos para este **elemento Row.** 
  
|**Valor**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|ArcTo  <br/> |Contiene las coordenadas x e y, y la curvatura de un arco circular.  <br/> |[Fila ArcTo (Sección de geometría)](arcto-row-geometry-section.md) <br/> |
|Elipse  <br/> |Contiene las coordenadas x e y del punto central y de dos puntos más de la elipse.  <br/> |[Fila Ellipse (Sección de Geometría)](ellipse-row-geometry-section.md) <br/> |
|EllipticalArcTo  <br/> |Contiene las coordenadas x e y del extremo de un arco elíptico, las coordenadas x e y de los puntos de control del arco, el ángulo desde el eje x hasta el eje mayor de la elipse y la relación entre los ejes mayor y menor de la elipse.  <br/> |[Fila EllipticalArcTo (Sección de Geometría)](ellipticalarcto-row-geometry-section.md) <br/> |
|InfiniteLine  <br/> |Contiene las coordenadas x e y de dos puntos en una línea infinita.  <br/> |[Fila InfiniteLine (Sección de Geometría)](infiniteline-row-geometry-section.md) |
|LineTo  <br/> |Contiene las coordenadas x e y del vértice del extremo de un segmento de línea recta.  <br/> |[Fila LineTo (Sección de Geometría)](lineto-row-geometry-section.md) <br/> |
|MoveTo  <br/> |Contiene las coordenadas x e y del primer vértice de una forma o representa las coordenadas x e y del primer vértice después de una interrupción de una trayectoria.  <br/> |[Fila MoveTo (Sección de Geometría)](moveto-row-geometry-section.md) <br/> |
|NURBSTo  <br/> |Contiene las coordenadas x e y, la posición del segundo al último nodo, la posición del último grosor, la posición del primer nodo, la posición del primer grosor y la fórmula de una spline B racional no uniforme (NURBS).  <br/> |[Fila NURBSTo (Sección de Geometría)](nurbsto-row-geometry-section.md) <br/> |
|PolylineTo  <br/> |Contiene las coordenadas x e y del último punto de una polilínea y una fórmula de polilínea.  <br/> |[Fila PolylineTo (Sección de Geometría)](polylineto-row-geometry-section.md) <br/> |
|RelCubBezTo  <br/> |Contiene las coordenadas x e y del extremo de una curva bézier cúbica con relación al ancho y alto de la forma, las coordenadas x e y del punto de control del principio del ancho y alto de la forma relativa de la curva, y las coordenadas x e y del punto de control del final del ancho y alto de la forma relativa de la curva.  <br/> |[Fila RelCubBezTo (sección Geometría)](relcubbezto-row-geometry-section.md) <br/> |
|RelEllipticalArcTo  <br/> |Contiene coordenadas x e y del extremo de un arco elíptico con relación al ancho y alto de la forma, las coordenadas x e y de los puntos de control del arco con relación al ancho y alto de la forma, el ángulo desde el eje X al eje principal de la elipse y la relación entre los ejes principales y los ejes menores de la elipse.  <br/> |[Fila RelEllipticalArcTo (sección Geometría)](relellipticalarcto-row-geometry-section.md) <br/> |
|RelLineTo  <br/> |Contiene coordenadas x e y del vértice final de un segmento de línea recta con relación al ancho y alto de una forma.  <br/> |[Fila RelLineTo (sección Geometría)](rellineto-row-geometry-section.md) <br/> |
|RelMoveTo  <br/> |Contiene las coordenadas x e y del primer vértice de una forma o las coordenadas x e y del primer vértice después de un salto en una ruta de acceso, en relación con el alto y el ancho de la forma.  <br/> |[Fila RelMoveTo (sección Geometría)](relmoveto-row-geometry-section.md) <br/> |
|RelQuadBezTo  <br/> |Contiene las coordenadas x e y del extremo de una curva bézier cuadrática en relación con el ancho y alto de la forma y las coordenadas x e y del punto de control del ancho y alto relativos de la forma de curva.  <br/> |[Fila RelQuadBezTo (sección Geometría)](relquadbezto-row-geometry-section.md) <br/> |
|SplineKnot  <br/> |Contiene las coordenadas x e y del punto de control y de un nodo de una spline.  <br/> |[Fila SplineKnot (Sección de Geometría)](splineknot-row-geometry-section.md) <br/> |
|SplineStart  <br/> |Contiene las coordenadas x e y del segundo punto de control de una spline, sus nodos segundo, primero y último, y el grado de la spline.  <br/> |[Fila SplineStart (Sección de Geometría)](splinestart-row-geometry-section.md) <br/> |
   

