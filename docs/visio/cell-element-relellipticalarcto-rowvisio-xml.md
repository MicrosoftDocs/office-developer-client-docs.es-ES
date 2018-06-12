---
title: Elemento de celda (fila RelEllipticalArcTo) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beaa8860-807e-c8dd-8a59-29cd0f91ba45
description: Contiene las coordenadas x o y del extremo de un arco elíptico en relación con el ancho y el alto, la forma de puntos de coordenadas x o y del control del arco con respecto a la forma width y height, ángulo desde el eje x en el eje de la elipse, o relación entre el ejes mayor y menor de la elipse.
ms.openlocfilehash: 661f6971ca4c03c68950ead45065bd12160918d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821739"
---
# <a name="cell-element-relellipticalarcto-row-visio-xml"></a>Elemento de celda (fila RelEllipticalArcTo) ('XML de Visio')

Contiene las coordenadas x o y del extremo de un arco elíptico en relación con el ancho y el alto, la forma de puntos de coordenadas x o y del control del arco con respecto a la forma width y height, ángulo desde el eje x en el eje de la elipse, o relación entre el ejes mayor y menor de la elipse.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |master # .xml, # .xml de página  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded">
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Elemento de fila (geometría)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelEllipticalArcTo_Type](relellipticalarcto_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del extremo de un arco elíptico en relación con el ancho y el alto, la forma de puntos de coordenadas x o y del control del arco con respecto a la forma width y height, ángulo desde el eje x en el eje de la elipse, o relación entre el ejes mayor y menor de la elipse.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica una referencia a una página de dibujo.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd: String  <br/> |opcional  <br/> |Indica que la fórmula da como resultado un error. El valor de **E** es el valor actual (una cadena de mensaje de error); el valor del atributo **V** es el último valor válido.  <br/> |Una cadena de mensaje de error.  <br/> |
|F  <br/> |xsd: String  <br/> |opcional  <br/> | Representa la fórmula del elemento. Este atributo puede contener uno de las siguientes cadenas:  <br/>  '(algunos fórmula)' Si la fórmula existe localmente  <br/>  `No Formula`Si la fórmula se ha eliminado localmente o bloqueada  <br/>  `Inh`Si la fórmula es heredada.  <br/> |Una fórmula.  <br/> |
|N  <br/> |xsd: String  <br/> |necesario  <br/> |Representa el nombre de la celda ShapeSheet.  <br/> |El nombre de la celda ShapeSheet.  <br/> Vea la sección comentarios que aparece a continuación.  <br/> |
|U  <br/> |xsd: String  <br/> |opcional  <br/> |Representa una unidad de medida, el valor predeterminado es DL.  <br/> |Las unidades de la celda.  <br/> |
|V  <br/> |xsd: String  <br/> |opcional  <br/> |Representa el valor de la celda.  <br/> |El valor de la celda ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Notas

El atributo **N** de este elemento de **celda** debe ser uno de un conjunto limitado de valores que corresponden a las celdas de ShapeSheet. Hacer referencia a la tabla siguiente para determinar los valores del atributo **N** permitidas para este elemento de **celda** . 
  
|**Valor**|**Descripción**|**Obtener más información**|
|:-----|:-----|:-----|
|X  <br/> |La coordenada x del vértice del extremo de un arco en relación con el ancho de la forma.  <br/> |[Fila de RelEllipticalArcTo (sección de geometría)](relellipticalarcto-row-geometry-section.md) <br/> |
|v  <br/> |Coordenada y del vértice del extremo de un arco con relación al alto de la forma.  <br/> |[Fila de RelEllipticalArcTo (sección de geometría)](relellipticalarcto-row-geometry-section.md) <br/> |
|A  <br/> |Elija la coordenada x del control del arco con respecto al ancho de la forma; un punto en el arco.  <br/> |[Fila de RelEllipticalArcTo (sección de geometría)](relellipticalarcto-row-geometry-section.md) <br/> |
|B  <br/> |Punto de la coordenada y del control de un arco con respecto al ancho de la forma.  <br/> |[Fila de RelEllipticalArcTo (sección de geometría)](relellipticalarcto-row-geometry-section.md) <br/> |
|C  <br/> |Ángulo del eje mayor de un arco con respecto al eje x de su forma principal.  <br/> |[Fila de RelEllipticalArcTo (sección de geometría)](relellipticalarcto-row-geometry-section.md) <br/> |
|D  <br/> |La relación de eje y el eje menor de un arco.  <br/> |[Fila de RelEllipticalArcTo (sección de geometría)](relellipticalarcto-row-geometry-section.md) <br/> |
   

