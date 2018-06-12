---
title: Elemento Row (sección de geometría) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2b273958-1997-7c63-4a61-d231f023a81f
description: Contiene filas que enumeran las coordenadas de los vértices de las líneas y arcos que constituyen la forma.
ms.openlocfilehash: 7a829651c4cab62a5c583d068211b9ffa20e725e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823037"
---
# <a name="row-element-geometry-section-visio-xml"></a>Elemento Row (sección de geometría) ('XML de Visio')

Contiene filas que enumeran las coordenadas de los vértices de las líneas y arcos que constituyen la forma.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[GeometryRow_Type](geometry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |master # .xml, # .xml de página  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Row" type="GeometryRow_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Sección](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Contiene filas que enumeran las coordenadas de los vértices de las líneas y arcos que constituyen la forma.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

> [!NOTE]
> El elemento de celda es el único secundario de este elemento. Dependiendo del atributo "T" de este elemento, el significado de los elementos de celda son diferentes. En la tabla siguiente, parathetical texto en el nombre del elemento corresponde al valor "T" a la que se aplica el tema. 
  
|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Elemento de celda (fila ArcTo)](arcto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y y la curvatura de un arco circular.  <br/> |
|[Elemento de celda (fila Ellipse)](ellipse-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del punto central y dos puntos de la elipse de la elipse.  <br/> |
|[Elemento de celda (fila EllipticalArcTo)](ellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del extremo de un arco elíptico, puntos de coordenadas x e y del control del arco, el ángulo desde el eje x a la elipse eje y la relación entre los ejes mayor y menor de la elipse.  <br/> |
|[Elemento de celda (fila InfiniteLine)](infiniteline-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y de dos puntos en una línea infinita.  <br/> |
|[Elemento de celda (fila LineTo)](lineto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene x- y las coordenadas y del vértice del extremo de un segmento de línea recta.  <br/> |
|[Elemento de celda (fila MoveTo)](moveto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del primer vértice de una forma o representa las coordenadas x e y del primer vértice después de una interrupción en una ruta de acceso.  <br/> |
|[Elemento de celda (fila NURBSTo)](nurbsto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y, la posición del segundo al último nodo, la posición del último grosor, la posición del primer nodo, la posición del primer grosor y la fórmula para una B-spline racional no uniforme (NURBS).  <br/> |
|[Elemento de celda (fila PolyLineTo)](polylineto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del último punto de una polilínea y una fórmula de polilínea.  <br/> |
|[Elemento de celda (fila RelCubBezTo)](relcubbezto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del extremo de una curva de Bézier cúbica con relación al ancho de la forma y el alto, las coordenadas x e y del punto de control del principio de la curva relativa al ancho de la forma y el alto y las coordenadas x e y del control punto de la hora de finalización del ancho y alto de la forma relativa de curva.  <br/> |
|[Elemento de celda (fila RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y de extremo de una curva Bézier cuadrática con respecto al ancho de la forma y el alto y las coordenadas x e y del punto de control del ancho y alto de la forma relativa de curva.  <br/> |
|[Elemento de celda (fila RelEllipticalArcTo)](relellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del extremo de un arco elíptico con relación al ancho de la forma y el alto, las coordenadas x e y de los puntos de control del arco con respecto al ancho de la forma y el alto, el ángulo desde el eje x a eje de la elipse y la relación entre ejes mayor y menor de la elipse.  <br/> |
|[Elemento de celda (fila RelLineTo)](rellineto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene x- y las coordenadas y del vértice del extremo de un segmento de línea recta con relación al ancho y alto de una forma.  <br/> |
|[Elemento de celda (fila RelMoveTo)](relmoveto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y del primer vértice de una forma o las coordenadas x e y del primer vértice después de una interrupción de una ruta de acceso, en relación con el alto y el ancho de la forma.  <br/> |
|[Elemento de celda (fila RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y de extremo de una curva Bézier cuadrática con respecto al ancho de la forma y el alto y las coordenadas x e y del punto de control del ancho y alto de la forma relativa de curva.  <br/> |
|[Elemento de celda (fila SplineKnot)](splineknot-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y de punto de control de una spline y un nodo de una spline.  <br/> |
|[Elemento de celda (fila SplineStart)](splinestart-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contiene las coordenadas x e y para el segundo punto de control de una spline, sus nodos segundo, primero, el último nodo y el grado de la spline.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|SUPR  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Especifica si se ha eliminado una fila que de lo contrario heredan la configuración de una forma de patrón.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica el identificador basado en uno de la fila. Debe ser único y mayor que otros identificadores en la misma sección. El atributo IX solo se usa para las secciones de carácter, conexión, campo, FillGradient, geometría, capa, LineGradient, párrafo, revisor, cero y las fichas. Sólo una fila puede tener uno de los atributos IX o N.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|LocalName  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el nombre único de dependen del idioma de la fila.  <br/> |Valores del tipo XSD: String.  <br/> |
|N  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el nombre único de independiente del idioma de la fila. El atributo N solo se usa para las secciones de usuario, propiedad, acciones, Control, conexión, hipervínculo y ActionTag. Sólo una fila puede tener uno de los atributos IX o N.  <br/> |Valores del tipo XSD: String.  <br/> |
|T  <br/> |xsd: String  <br/> |opcional  <br/> |Especifica el tipo de la ruta de acceso geométrica representada por la fila y utilizado en la visualización de la geometría. El atributo T solo se usa para la sección de geometría.  <br/> |Valores del tipo XSD: String.  <br/> |
   
## <a name="remarks"></a>Notas

El atributo **T** de este elemento de **fila** debe ser uno de un conjunto limitado de valores que corresponden a las filas de ShapeSheet. Hacer referencia a la tabla siguiente para determinar los valores del atributo **T** que se permiten para este elemento de **fila** . 
  
|**Valor**|**Descripción**|**Obtener más información**|
|:-----|:-----|:-----|
|ArcTo  <br/> |Contiene las coordenadas x e y y la curvatura de un arco circular.  <br/> |[Fila ArcTo (Sección de geometría)](arcto-row-geometry-section.md) <br/> |
|Elipse  <br/> |Contiene las coordenadas x e y del punto central y dos puntos de la elipse de la elipse.  <br/> |[Fila Ellipse (Sección de Geometría)](ellipse-row-geometry-section.md) <br/> |
|EllipticalArcTo  <br/> |Contiene las coordenadas x e y del extremo de un arco elíptico, puntos de coordenadas x e y del control del arco, el ángulo desde el eje x a la elipse eje y la relación entre los ejes mayor y menor de la elipse.  <br/> |[Fila EllipticalArcTo (Sección de Geometría)](ellipticalarcto-row-geometry-section.md) <br/> |
|InfiniteLine  <br/> |Contiene las coordenadas x e y de dos puntos en una línea infinita.  <br/> |[Fila InfiniteLine (Sección de Geometría)](http://msdn.microsoft.com/library/Contains the x- and y-coordinates of two points on an infinite line.%28Office.15%29.aspx) <br/> |
|LineTo  <br/> |Contiene x- y las coordenadas y del vértice del extremo de un segmento de línea recta.  <br/> |[Fila LineTo (Sección de Geometría)](lineto-row-geometry-section.md) <br/> |
|MoveTo  <br/> |Contiene las coordenadas x e y del primer vértice de una forma o representa las coordenadas x e y del primer vértice después de una interrupción en una ruta de acceso.  <br/> |[Fila MoveTo (Sección de Geometría)](moveto-row-geometry-section.md) <br/> |
|NURBSTo  <br/> |Contiene las coordenadas x e y, la posición del segundo al último nodo, la posición del último grosor, la posición del primer nodo, la posición del primer grosor y la fórmula para una B-spline racional no uniforme (NURBS).  <br/> |[Fila NURBSTo (Sección de Geometría)](nurbsto-row-geometry-section.md) <br/> |
|PolylineTo  <br/> |Contiene las coordenadas x e y del último punto de una polilínea y una fórmula de polilínea.  <br/> |[Fila PolylineTo (Sección de Geometría)](polylineto-row-geometry-section.md) <br/> |
|RelCubBezTo  <br/> |Contiene las coordenadas x e y del extremo de una curva de Bézier cúbica con relación al ancho de la forma y el alto, las coordenadas x e y del punto de control del principio de la curva relativa al ancho de la forma y el alto y las coordenadas x e y del control punto de la hora de finalización del ancho y alto de la forma relativa de curva.  <br/> |[Fila de RelCubBezTo (sección de geometría)](relcubbezto-row-geometry-section.md) <br/> |
|RelEllipticalArcTo  <br/> |Contiene las coordenadas x e y del extremo de un arco elíptico con relación al ancho de la forma y el alto, las coordenadas x e y de los puntos de control del arco con respecto al ancho de la forma y el alto, el ángulo desde el eje x a eje de la elipse y la relación entre ejes mayor y menor de la elipse.  <br/> |[Fila de RelEllipticalArcTo (sección de geometría)](relellipticalarcto-row-geometry-section.md) <br/> |
|RelLineTo  <br/> |Contiene x- y las coordenadas y del vértice del extremo de un segmento de línea recta con relación al ancho y alto de una forma.  <br/> |[Fila de RelLineTo (sección de geometría)](rellineto-row-geometry-section.md) <br/> |
|RelMoveTo  <br/> |Contiene las coordenadas x e y del primer vértice de una forma o las coordenadas x e y del primer vértice después de una interrupción de una ruta de acceso, en relación con el alto y el ancho de la forma.  <br/> |[Fila de RelMoveTo (sección de geometría)](relmoveto-row-geometry-section.md) <br/> |
|RelQuadBezTo  <br/> |Contiene las coordenadas x e y de extremo de una curva Bézier cuadrática con respecto al ancho de la forma y el alto y las coordenadas x e y del punto de control del ancho y alto de la forma relativa de curva.  <br/> |[Fila de RelQuadBezTo (sección de geometría)](relquadbezto-row-geometry-section.md) <br/> |
|SplineKnot  <br/> |Contiene las coordenadas x e y de punto de control de una spline y un nodo de una spline.  <br/> |[Fila SplineKnot (Sección de Geometría)](splineknot-row-geometry-section.md) <br/> |
|SplineStart  <br/> |Contiene las coordenadas x e y para el segundo punto de control de una spline, sus nodos segundo, primero, el último nodo y el grado de la spline.  <br/> |[Fila SplineStart (Sección de Geometría)](splinestart-row-geometry-section.md) <br/> |
   

