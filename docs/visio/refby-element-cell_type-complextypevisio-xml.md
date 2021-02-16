---
title: Elemento RefBy (Cell_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea2a63d3-d319-4420-1929-013dc832b308
description: Especifica una referencia a una página del dibujo.
ms.openlocfilehash: cb47919a97b8ad42f62bcb1337cd8e6b3596f5ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538315"
---
# <a name="refby-element-cell_type-complextype-visio-xml"></a>Elemento RefBy (Cell_Type complexType) (XML de Visio)

Especifica una referencia a una página del dibujo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |document.xml, masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Elemento Cell (Sección de etiquetas de acción)](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Define una propiedad para una etiqueta de acción en una forma o página.  <br/> |
|[Elemento Cell (fila Acciones)](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una propiedad de una acción asociada a un comando personalizado en un menú contextual o de etiqueta de acción.  <br/> |
|[Elemento Cell (fila ArcTo)](cell-element-arcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene la coordenada x, la coordenada y o la proa de un arco circular.  <br/> |
|[Elemento Cell (Sección de caracteres)](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica un atributo de formato para la ejecución de texto de una forma, como fuente, color, estilo, mayúsculas y minúsculas, posición relativa a la línea base o tamaño de punto.  <br/> |
|[Elemento Cell (fila Conexión)](cell-element-connection-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y, dirección horizontal o vertical, o el tipo de un único punto de conexión en una forma.  <br/> |
|[Elemento Cell (fila Controles)](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene una propiedad para un controlador determinado definido para una forma.  <br/> |
|[Elemento Cell (fila Elipse)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del punto central de la elipse y dos puntos en la elipse.  <br/> |
|[Elemento Cell (fila EllipticalArcTo)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene coordenadas x o y del extremo de un arco elíptico, las coordenadas x o y de los puntos de control del arco, el ángulo desde el eje X hasta el eje principal de la elipse o la relación entre los ejes principales y menores de la elipse.  <br/> |
|[Elemento Cell (Sección de campo)](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Presenta funciones y fórmulas insertadas en el texto de una forma con el cuadro de diálogo Campo.  <br/> |
|[Elemento Cell (Sección de degradado de relleno)](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene el color, la transparencia y la posición de un delimitador de degradado para un degradado de relleno.  <br/> |
|[Elemento Cell (Sección de geometría)](cell-element-geometry-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Define las propiedades que determinan las propiedades de formato y comportamiento con respecto a las líneas y arcos que integran la sección de geometría.  <br/> |
|[Elemento Cell (fila Hipervínculo)](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene información de un hipervínculo asociado con una forma. Una forma contendrá una fila Hyperlink por cada hipervínculo.  <br/> |
|[Elemento Cell (fila InfiniteLine)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y de dos puntos en una línea infinita.  <br/> |
|[Elemento Cell (Sección de capa)](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una propiedad para una capa o sus propiedades para una página.  <br/> |
|[Elemento Cell (Sección de degradado de línea)](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene el color, la transparencia o la posición de un delimitador de degradado para un degradado de línea.  <br/> |
|[Elemento Cell (fila LineTo)](cell-element-lineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene coordenadas x o y del vértice final de un segmento de línea recta.  <br/> |
|[Elemento Cell (fila MoveTo)](cell-element-moveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del primer vértice de una forma o representa las coordenadas x o y del primer vértice después de un salto en una ruta de acceso.  <br/> |
|[Elemento Cell (fila NURBSTo)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y, la posición del segundo al último nodo, la posición del último grosor, la posición del primer nodo, la posición del primer grosor o la fórmula de una spline B racional no uniforme (NURBS).  <br/> |
|[Elemento Cell (Sección de párrafo)](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica un atributo de formato de párrafo para el texto de la forma, como sangrías, interlineado, viñetas o alineación horizontal de párrafos.  <br/> |
|[Elemento Cell (fila PolyLineTo)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene coordenadas x o y del último punto de una polilínea o una fórmula de polilínea.  <br/> |
|[Elemento Cell (fila RelCubBezTo)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del extremo de una curva Bézier cúbica en relación con el ancho y alto de la forma, las coordenadas x o y del punto de control del principio del ancho y alto relativos de la forma de curva, o las coordenadas x- o y del punto de control del final del ancho y alto relativos de la forma de curva.  <br/> |
|[Elemento Cell (fila RelEllipticalArcTo)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene coordenadas x o y del extremo de un arco elíptico con relación al ancho y alto de la forma, las coordenadas x o y de los puntos de control del arco con relación al ancho y alto de la forma, el ángulo desde el eje X hasta el eje principal de la elipse o la relación entre los ejes principales y menores de la elipse.  <br/> |
|[Celda del elemento Cell (fila RelLineTo)](cell-element-rellineto-rowvisio-xml.md)[](cell-element-rellineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene coordenadas x o y del vértice final de un segmento de línea recta con relación al ancho y alto de una forma.  <br/> |
|[Elemento Cell (fila RelMoveTo)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del primer vértice de una forma, o las coordenadas x o y del primer vértice después de un salto en una ruta de acceso, en relación con el alto y el ancho de la forma.  <br/> |
|[Elemento Cell (Sección RelQuadBezTo](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del extremo de una curva Bézier cuadrática con relación al ancho y alto de la forma o a las coordenadas x o y del punto de control del ancho y alto relativos de la forma.  <br/> |
|[Elemento Cell (Sección de scratch)](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica un área de trabajo para escribir y probar fórmulas a las que pueden hacer referencia otras celdas.  <br/> |
|[Elemento Cell (Sección de datos de formas)](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una propiedad de los datos de formas.  <br/> |
|[Elemento Cell (fila SplineKnot)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene coordenadas x o y para el punto de control de una spline o el nodo de una spline.  <br/> |
|[Elemento Cell (sección SplineStart)](cell-element-splinestart-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene coordenadas x o y para el segundo punto de control de una spline, su segundo nodo, su primer nodo, el último nodo o el grado de la spline.  <br/> |
|[Elemento Cell (Sección de tabulaciones)](cell-element-tabs-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una propiedad que controla la posición o alineación de la tabulación de forma y estilo.  <br/> |
|[Elemento Cell (Sección de celdas definidas por el usuario)](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Una propiedad de una información especificada por el usuario a la que pueden hacer referencia otras celdas y herramientas de complementos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Especifica el identificador de una página del dibujo.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|T  <br/> |xsd:string  <br/> |necesario  <br/> |Especifica el tipo de referencia.  <br/> |Valores del tipo xsd:string.  <br/> |
   

