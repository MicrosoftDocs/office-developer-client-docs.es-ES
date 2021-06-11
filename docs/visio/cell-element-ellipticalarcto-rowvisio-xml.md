---
title: Elemento Cell (Fila EllipticalArcTo) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c0aa7a3-cc54-ffac-2c62-917b3d0a357e
description: Contiene coordenadas x o y del extremo de un arco elíptico, las coordenadas X o Y de los puntos de control en el arco, el ángulo desde el eje X hasta el eje principal de la elipse o la relación entre los ejes principales y los ejes menores de la elipse.
ms.openlocfilehash: 396575c069925fe472fa3df0543e29303881dad3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539831"
---
# <a name="cell-element-ellipticalarcto-row-visio-xml"></a>Elemento Cell (Fila EllipticalArcTo) (Visio XML)

Contiene coordenadas x o y del extremo de un arco elíptico, las coordenadas X o Y de los puntos de control en el arco, el ángulo desde el eje X hasta el eje principal de la elipse o la relación entre los ejes principales y los ejes menores de la elipse.
  
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
|[Elemento Row (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[EllipticalArcTo_Type](ellipticalarcto_type-complextypevisio-xml.md) <br/> |Contiene coordenadas x o y del extremo de un arco elíptico, las coordenadas X o Y de los puntos de control en el arco, el ángulo desde el eje X hasta el eje principal de la elipse o la relación entre los ejes principales y los ejes menores de la elipse.  <br/> |
   
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
|X  <br/> |Coordenada x del vértice del extremo de un arco.  <br/> |[Fila EllipticalArcTo (Sección de Geometría)](ellipticalarcto-row-geometry-section.md) <br/> |
|v  <br/> |Coordenada y del vértice del extremo de un arco.  <br/> |[Fila EllipticalArcTo (Sección de Geometría)](ellipticalarcto-row-geometry-section.md) <br/> |
|A  <br/> |Coordenada x del punto de control del arco (un punto del arco). La mejor posición del punto de control está en la mitad de la distancia entre el vértice inicial y el vértice final del arco. De otra manera, el arco puede crecer demasiado para pasar por el punto de control, lo que puede dar lugar a resultados inesperados.  <br/> |[Fila EllipticalArcTo (Sección de Geometría)](ellipticalarcto-row-geometry-section.md) <br/> |
|B  <br/> |Coordenada y del punto de control de un arco.  <br/> |[Fila EllipticalArcTo (Sección de Geometría)](ellipticalarcto-row-geometry-section.md) <br/> |
|C  <br/> |Ángulo del eje principal de un arco con relación al eje X de su forma primaria.  <br/> |[Fila EllipticalArcTo (Sección de Geometría)](ellipticalarcto-row-geometry-section.md) <br/> |
|D  <br/> |Relación entre el eje mayor y el eje menor de un arco. A pesar del significado normal de estas palabras, el eje "mayor" no tiene por qué ser más grande que el eje "menor", por lo que esta relación no tiene que ser mayor que 1. Si establece en esta celda un valor menor o igual que 0, o mayor que 1000, pueden producirse resultados inesperados.  <br/> |[Fila EllipticalArcTo (Sección de Geometría)](ellipticalarcto-row-geometry-section.md) <br/> |
   

