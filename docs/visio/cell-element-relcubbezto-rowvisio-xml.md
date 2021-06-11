---
title: Elemento Cell (RelCubBezTo Row) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: daa5c527-65fe-a1e4-ab3e-24e77bdb522b
description: Contiene las coordenadas x o y del extremo de una curva bézier cúbica con relación al ancho y alto de la forma, las coordenadas x o y del punto de control del principio del ancho y alto de la forma relativa de la curva, o las coordenadas X o Y del punto de control del final del ancho y alto de la forma relativa de la curva.
ms.openlocfilehash: c52b0108cc6ed753c0e494d2bce72025cabb1c93
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539442"
---
# <a name="cell-element-relcubbezto-row-visio-xml"></a>Elemento Cell (RelCubBezTo Row) (Visio XML)

Contiene las coordenadas x o y del extremo de una curva bézier cúbica con relación al ancho y alto de la forma, las coordenadas x o y del punto de control del principio del ancho y alto de la forma relativa de la curva, o las coordenadas X o Y del punto de control del final del ancho y alto de la forma relativa de la curva.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Elemento Row (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelCubBezTo_Type](relcubbezto_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del extremo de una curva bézier cúbica con relación al ancho y alto de la forma, las coordenadas x o y del punto de control del principio del ancho y alto de la forma relativa de la curva, o las coordenadas X o Y del punto de control del final del ancho y alto de la forma relativa de la curva.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica una referencia a una página de dibujo.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |opcional  <br/> |Indica que la fórmula se evalúa como un error. El valor de **E** es el valor actual (una cadena de mensaje de error); el valor del atributo **V** es el último valor válido.  <br/> |Una cadena de mensaje de error.  <br/> |
|F  <br/> |xsd:string  <br/> |opcional  <br/> | Representa la fórmula del elemento. Este atributo puede contener una de las cadenas siguientes:  <br/>  '(alguna fórmula)' si la fórmula existe localmente  <br/>  `No Formula` si la fórmula se elimina o bloquea localmente  <br/>  `Inh` si la fórmula se hereda.  <br/> |Una fórmula.  <br/> |
|N  <br/> |xsd:string  <br/> |necesario  <br/> |Representa el nombre de la celda ShapeSheet.  <br/> |Nombre de la celda ShapeSheet.  <br/> Vea la sección Comentarios a continuación.  <br/> |
|U  <br/> |xsd:string  <br/> |opcional  <br/> |Representa una unidad de medida El valor predeterminado es DL.  <br/> |Las unidades de la celda.  <br/> |
|V  <br/> |xsd:string  <br/> |opcional  <br/> |Representa el valor de la celda.  <br/> |Valor de la celda ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Comentarios

El **atributo N** de este elemento **Cell** debe ser uno de un conjunto limitado de valores que corresponden a celdas ShapeSheet. Consulte la tabla siguiente para determinar los valores del atributo **N** permitidos para este **elemento Cell.** 
  
|**Valor**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|X  <br/> |Coordenada x del vértice final de una curva bézier cúbica con relación al ancho de la forma.  <br/> |[Fila RelCubBezTo (sección Geometría)](relcubbezto-row-geometry-section.md) <br/> |
|v  <br/> |Coordenada y del vértice final de una curva bézier cúbica con relación al alto de la forma.  <br/> |[Fila RelCubBezTo (sección Geometría)](relcubbezto-row-geometry-section.md) <br/> |
|A  <br/> |Coordenada x del punto de control inicial de la curva con relación al ancho de la forma; un punto en el arco. El punto de control se encuentra mejor entre los vértices inicial y final del arco.  <br/> |[Fila RelCubBezTo (sección Geometría)](relcubbezto-row-geometry-section.md) <br/> |
|B  <br/> |Coordenada y del punto de control inicial de una curva con relación al alto de la forma.  <br/> |[Fila RelCubBezTo (sección Geometría)](relcubbezto-row-geometry-section.md) <br/> |
|C  <br/> |Coordenada x del punto de control final de la curva con relación al ancho de la forma; un punto en el arco. El punto de control se encuentra mejor entre el punto de control inicial y los vértices finales del arco.  <br/> |[Fila RelCubBezTo (sección Geometría)](relcubbezto-row-geometry-section.md) <br/> |
|D  <br/> |Coordenada y del punto de control final de una curva con relación al alto de la forma.  <br/> |[Fila RelCubBezTo (sección Geometría)](relcubbezto-row-geometry-section.md) <br/> |
   

