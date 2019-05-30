---
title: Elemento RefBy (complexType Cell_Type) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea2a63d3-d319-4420-1929-013dc832b308
description: Especifica una referencia a una página en el dibujo.
ms.openlocfilehash: cb47919a97b8ad42f62bcb1337cd8e6b3596f5ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538315"
---
# <a name="refby-element-celltype-complextype-visio-xml"></a>Elemento RefBy (complexType Cell_Type) (XML de Visio)

Especifica una referencia a una página en el dibujo.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Document. XML, Masters. XML, Master #. XML, Pages. XML, página #. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Elemento cell (sección etiqueta de acción)](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Define una propiedad para una etiqueta de acción en una forma o una página.  <br/> |
|[Elemento Cell (fila Acciones)](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una propiedad de una acción asociada con un comando personalizado en un menú contextual o de etiquetas de acción.  <br/> |
|[Elemento Cell (fila ArcTo)](cell-element-arcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene la coordenada x, la coordenada y o la curvatura de un arco circular.  <br/> |
|[Elemento cell (sección de caracteres)](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica un atributo de formato para la ejecución de texto de una forma, como la fuente, el color, el estilo, el caso, la posición relativa a la línea base o el tamaño en puntos.  <br/> |
|[Elemento Cell (fila Conexión)](cell-element-connection-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x-o y, la dirección horizontal o vertical, o el tipo de un punto de conexión único de una forma.  <br/> |
|[Elemento Cell (fila Controles)](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene una propiedad para un controlador de control determinado definido para una forma.  <br/> |
|[Elemento Cell (fila Elipse)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del punto central de la elipse y de dos puntos de la elipse.  <br/> |
|[Elemento Cell (fila EllipticalArcTo)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del extremo de un arco elíptico, las coordenadas x o y de los puntos de control del arco, el ángulo desde el eje x hasta el eje mayor de la elipse o la proporción entre los ejes mayor y menor de la elipse.  <br/> |
|[Elemento cell (sección campo)](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Presenta funciones y fórmulas insertadas en el texto de una forma con el cuadro de diálogo Campo.  <br/> |
|[Elemento cell (sección degradado de relleno)](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene el color, la transparencia y la posición de un punto de degradado para un degradado de relleno.  <br/> |
|[Elemento cell (sección geometría)](cell-element-geometry-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Define las propiedades que determinan el formato y las propiedades de comportamiento con respecto a las líneas y los arcos que componen la sección de geometría.  <br/> |
|[Elemento Cell (fila Hipervínculo)](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene información de un hipervínculo asociado con una forma. Una forma contendrá una fila Hyperlink por cada hipervínculo.  <br/> |
|[Elemento Cell (fila InfiniteLine)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y de dos puntos en una línea infinita.  <br/> |
|[Elemento cell (sección capa)](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una propiedad para una capa o sus propiedades para una página.  <br/> |
|[Elemento cell (sección degradado de línea)](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene el color, la transparencia o la posición de un punto de degradado de un degradado de línea.  <br/> |
|[Elemento Cell (fila LineTo)](cell-element-lineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del vértice del extremo de un segmento de línea recta.  <br/> |
|[Elemento Cell (fila MoveTo)](cell-element-moveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del primer vértice de una forma o representa las coordenadas x o y del primer vértice después de una interrupción en una ruta de acceso.  <br/> |
|[Elemento Cell (fila NURBSTo)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y, la posición del segundo al último nodo, la posición del último grosor, la posición del primer nodo, la posición del primer grosor o la fórmula de una spline B racional no uniforme (NURBS).  <br/> |
|[Elemento cell (sección párrafo)](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica un atributo de formato de párrafo para el texto de la forma, como sangrías, espacio entre líneas, viñetas o alineación horizontal de los párrafos.  <br/> |
|[Elemento Cell (fila PolyLineTo)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del último punto de una polilínea o una fórmula de polilínea.  <br/> |
|[Elemento Cell (fila RelCubBezTo)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del punto final de una curva Bézier cúbica en relación con el ancho y el alto de la forma, las coordenadas x o y del punto de control del principio del ancho y el alto de la forma relativa de la curva, o las coordenadas x o y del punto de control. de la finalización del ancho y el alto de la forma relativa de la curva.  <br/> |
|[Elemento Cell (fila RelEllipticalArcTo)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del extremo de un arco elíptico en relación con el ancho y el alto de la forma, las coordenadas x o y de los puntos de control del arco con respecto al ancho y el alto de la forma, el ángulo desde el eje x hasta el eje mayor de la elipse o la relación entre el ejes principal y secundario de la elipse.  <br/> |
|[Elemento cell (fila RelLineTo)](cell-element-rellineto-rowvisio-xml.md) [Celda](cell-element-rellineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del vértice del extremo de un segmento de línea recta con relación al ancho y el alto de la forma.  <br/> |
|[Elemento Cell (fila RelMoveTo)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del primer vértice de una forma, o las coordenadas x o y del primer vértice después de una interrupción en una ruta de acceso, en relación con el alto y ancho de la forma.  <br/> |
|[Elemento cell (sección RelQuadBezTo](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del punto final de una curva Bézier cuadrática en relación con el ancho y el alto de la forma o las coordenadas x o y del punto de control del ancho y alto de la forma relativa de la curva.  <br/> |
|[Elemento cell (sección borrador)](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica un área de trabajo para escribir y probar fórmulas a las que se puede hacer referencia en otras celdas.  <br/> |
|[Elemento cell (sección datos de formas](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una propiedad de los datos de formas.  <br/> |
|[Elemento Cell (fila SplineKnot)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del punto de control de una spline o de un nodo de una spline.  <br/> |
|[Elemento cell (sección SplineStart](cell-element-splinestart-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del segundo punto de control de una spline, su segundo nodo, su primer nodo, el último nodo o el grado de la spline.  <br/> |
|[Elemento cell (sección tabulaciones)](cell-element-tabs-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica una propiedad que controla la posición o alineación de las tabulaciones de la forma y el estilo.  <br/> |
|[Elemento cell (sección celdas definidas por el usuario)](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Una propiedad de una información especificada por el usuario a la que se puede hacer referencia por otras celdas y herramientas complementarias.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> |Especifica el identificador de una página en el dibujo.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|T  <br/> |xsd: String  <br/> |necesario  <br/> |Especifica el tipo de referencia.  <br/> |Valores del tipo xsd: String.  <br/> |
   

