---
title: Elemento cell (fila RelEllipticalArcTo) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beaa8860-807e-c8dd-8a59-29cd0f91ba45
description: Contiene las coordenadas x o y del extremo de un arco elíptico en relación con el ancho y el alto de la forma, las coordenadas x o y de los puntos de control del arco con respecto al ancho y el alto de la forma, el ángulo desde el eje x hasta el eje mayor de la elipse o la relación entre el ejes principal y secundario de la elipse.
ms.openlocfilehash: 55e7f664aaab34aa079bafe8f11c57e99fd8a935
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339553"
---
# <a name="cell-element-relellipticalarcto-row-visio-xml"></a>Elemento cell (fila RelEllipticalArcTo) ("XML" de Visio)

Contiene las coordenadas x o y del extremo de un arco elíptico en relación con el ancho y el alto de la forma, las coordenadas x o y de los puntos de control del arco con respecto al ancho y el alto de la forma, el ángulo desde el eje x hasta el eje mayor de la elipse o la relación entre el ejes principal y secundario de la elipse.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Master #. XML, página #. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded">
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Elemento Row (geometría)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelEllipticalArcTo_Type](relellipticalarcto_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del extremo de un arco elíptico en relación con el ancho y el alto de la forma, las coordenadas x o y de los puntos de control del arco con respecto al ancho y el alto de la forma, el ángulo desde el eje x hasta el eje mayor de la elipse o la relación entre el ejes principal y secundario de la elipse.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica una referencia a una página de dibujo.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd: String  <br/> |opcional  <br/> |Indica que la fórmula da como resultado un error. El valor de **E** es el valor actual (una cadena de mensaje de error); el valor del atributo **V** es el último valor válido.  <br/> |Una cadena de mensaje de error.  <br/> |
|F  <br/> |xsd: String  <br/> |opcional  <br/> | Representa la fórmula del elemento. Este atributo puede contener una de las siguientes cadenas:  <br/>  ' (alguna fórmula) ' si la fórmula existe localmente  <br/>  `No Formula`Si la fórmula se ha eliminado o bloqueado localmente  <br/>  `Inh`Si la fórmula es heredada.  <br/> |Una fórmula.  <br/> |
|N  <br/> |xsd: String  <br/> |necesario  <br/> |Representa el nombre de la celda ShapeSheet.  <br/> |Nombre de la celda ShapeSheet.  <br/> Vea la sección Comentarios a continuación.  <br/> |
|U  <br/> |xsd: String  <br/> |opcional  <br/> |Representa una unidad de medida el valor predeterminado es DL.  <br/> |Unidades de la celda.  <br/> |
|V  <br/> |xsd: String  <br/> |opcional  <br/> |Representa el valor de la celda.  <br/> |El valor de la celda ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Comentarios

El atributo **N** de este elemento de **celda** debe ser uno de un conjunto de valores limitado que corresponda a las celdas de ShapeSheet. Consulte la tabla siguiente para determinar los valores del atributo **N** que se permiten para este elemento de **celda** . 
  
|**Value**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|X  <br/> |Coordenada x del vértice del extremo de un arco en relación con el ancho de la forma.  <br/> |[Fila RelEllipticalArcTo (sección geometría)](relellipticalarcto-row-geometry-section.md) <br/> |
|v  <br/> |Coordenada y del vértice del extremo de un arco en relación con el alto de la forma.  <br/> |[Fila RelEllipticalArcTo (sección geometría)](relellipticalarcto-row-geometry-section.md) <br/> |
|A  <br/> |Coordenada x del punto de control del arco con respecto al ancho de la forma; un punto en el arco.  <br/> |[Fila RelEllipticalArcTo (sección geometría)](relellipticalarcto-row-geometry-section.md) <br/> |
|B  <br/> |Coordenada y del punto de control de un arco con respecto al ancho de la forma.  <br/> |[Fila RelEllipticalArcTo (sección geometría)](relellipticalarcto-row-geometry-section.md) <br/> |
|C  <br/> |Ángulo del eje mayor de un arco con respecto al eje x de su elemento primario.  <br/> |[Fila RelEllipticalArcTo (sección geometría)](relellipticalarcto-row-geometry-section.md) <br/> |
|D  <br/> |Relación entre el eje mayor y el eje menor de un arco.  <br/> |[Fila RelEllipticalArcTo (sección geometría)](relellipticalarcto-row-geometry-section.md) <br/> |
   

