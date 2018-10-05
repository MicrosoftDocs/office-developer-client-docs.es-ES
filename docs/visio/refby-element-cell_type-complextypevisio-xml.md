---
title: Elemento de RefBy (Cell_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea2a63d3-d319-4420-1929-013dc832b308
description: Especifica una referencia a una página en el dibujo.
ms.openlocfilehash: 1731bd20a5ba4358c72370dfcdc6d8a6fc791e2f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385861"
---
# <a name="refby-element-celltype-complextype-visio-xml"></a>Elemento de RefBy (Cell_Type complexType) ('XML de Visio')

Especifica una referencia a una página en el dibujo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Document.XML, masters.xml, maestra # .xml, pages.xml, página # .xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Elemento Cell (sección Etiqueta de acción)](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Define una propiedad para una etiqueta de acción en una forma o página.  <br/> |
|[Elemento Cell (fila Acciones)](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una propiedad de una acción asociada con un comando personalizado en un menú contextual o de acción de la etiqueta.  <br/> |
|[Elemento Cell (fila ArcTo)](cell-element-arcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene la x coordenadas, coordenada y o curvatura de un arco circular.  <br/> |
|[Elemento Cell (sección Carácter)](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica un atributo de formato para la ejecución de texto de una forma, como fuente, color, estilo, caso, posición relativa a la línea base o tamaño en puntos.  <br/> |
|[Elemento Cell (fila Conexión)](cell-element-connection-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y, dirección horizontal o vertical o tipo para un único punto de conexión en una forma.  <br/> |
|[Elemento Cell (fila Controles)](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene una propiedad para un controlador definido para una forma.  <br/> |
|[Elemento Cell (fila Elipse)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del punto central y dos puntos de la elipse de la elipse.  <br/> |
|[Elemento Cell (fila EllipticalArcTo)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del extremo de un arco elíptico, puntos de coordenadas x o y del control del arco, el ángulo desde el eje x a eje mayor de la elipse o relación entre los ejes mayor y menor de la elipse.  <br/> |
|[Elemento Cell (sección Campo)](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Presenta funciones y fórmulas insertadas en el texto de una forma con el cuadro de diálogo Campo.  <br/> |
|[Elemento Cell (sección Degradado de relleno)](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene el color, la transparencia y la posición de un punto de degradado para un degradado de relleno.  <br/> |
|[Elemento Cell (sección Geometría)](cell-element-geometry-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Define las propiedades que determinan las propiedades de formato y el comportamiento con respecto a las líneas y arcos que constituyen la sección de geometría.  <br/> |
|[Elemento Cell (fila Hipervínculo)](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene información de un hipervínculo asociado con una forma. Una forma contendrá una fila Hyperlink por cada hipervínculo.  <br/> |
|[Elemento Cell (fila InfiniteLine)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y de dos puntos en una línea infinita.  <br/> |
|[Elemento Cell (sección Capa)](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una propiedad de una capa o sus propiedades de una página.  <br/> |
|[Elemento Cell (sección Degradado de línea)](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene el color, la transparencia o la posición de un punto de degradado para un degradado de línea.  <br/> |
|[Elemento Cell (fila LineTo)](cell-element-lineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene x- o coordenadas y del vértice del extremo de un segmento de línea recta.  <br/> |
|[Elemento Cell (fila MoveTo)](cell-element-moveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del primer vértice de una forma o representa las coordenadas x o y del primer vértice después de una interrupción en una ruta de acceso.  <br/> |
|[Elemento Cell (fila NURBSTo)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y, la posición del segundo al último nodo, la posición del último grosor, la posición del primer nodo, la posición del primer grosor o la fórmula para una B-spline racional no uniforme (NURBS).  <br/> |
|[Elemento Cell (sección Párrafo)](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica un atributo para el texto de la forma, como sangrías, espaciado de líneas, viñetas o alineación horizontal de los párrafos de formato de párrafo.  <br/> |
|[Elemento Cell (fila PolyLineTo)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del último punto de una polilínea o una fórmula de polilínea.  <br/> |
|[Elemento Cell (fila RelCubBezTo)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y de extremo de una curva de Bézier cúbica con relación al ancho de la forma y el alto, las coordenadas x o y del punto de control del principio de la curva relativa al ancho de la forma y el alto o las coordenadas x o y del punto de control del final del ancho y alto de la forma relativa de curva.  <br/> |
|[Elemento Cell (fila RelEllipticalArcTo)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del extremo de un arco elíptico en relación con el ancho y el alto, la forma de puntos de coordenadas x o y del control del arco con respecto a la forma width y height, ángulo desde el eje x en el eje de la elipse, o relación entre el ejes mayor y menor de la elipse.  <br/> |
|[Elemento de celda (fila RelLineTo)](cell-element-rellineto-rowvisio-xml.md) [Celda](cell-element-rellineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene x- o coordenadas y del vértice del extremo de un segmento de línea recta con relación al ancho y alto de una forma.  <br/> |
|[Elemento Cell (fila RelMoveTo)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del primer vértice de una forma o las coordenadas x o y del primer vértice después de una interrupción de una ruta de acceso, en relación con el alto y el ancho de la forma.  <br/> |
|[Elemento de celda (sección de RelQuadBezTo](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del extremo de una curva Bézier cuadrática con respecto al ancho de la forma y el alto o las coordenadas x o y del punto de control del ancho y alto de la forma relativa de curva.  <br/> |
|[Elemento Cell (sección Borrador)](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica un área de trabajo para escribir y probar fórmulas a las que se pueden hacer referencia a otras celdas.  <br/> |
|[Elemento de celda (sección Shape Data](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una propiedad de los datos de formas.  <br/> |
|[Elemento Cell (fila SplineKnot)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y para el punto de control de una spline o nodo de una spline.  <br/> |
|[Elemento de celda (sección de SplineStart](cell-element-splinestart-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y para el segundo punto de control de una spline, sus nodos segundo, primero, el último nodo o el grado de la spline.  <br/> |
|[Elemento Cell (sección Tabulaciones)](cell-element-tabs-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una propiedad que controla la forma y el estilo de posición de tabulación o la alineación.  <br/> |
|[Elemento Cell (sección Celdas definidas por el usuario)](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Una propiedad de una parte especificada por el usuario de la información que se puede hacer referencia a otras celdas y herramientas complementarias.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Especifica el identificador de una página en el dibujo.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|T  <br/> |xsd: String  <br/> |necesario  <br/> |Especifica el tipo de referencia.  <br/> |Valores del tipo XSD: String.  <br/> |
   

