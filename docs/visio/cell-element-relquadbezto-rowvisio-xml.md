---
title: Elemento de celda (fila RelQuadBezTo) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8b3aea70-a69f-a85e-83d8-c0fa2ee68836
description: Contiene las coordenadas x o y del extremo de una curva Bézier cuadrática con respecto al ancho de la forma y el alto o las coordenadas x o y del punto de control del ancho y alto de la forma relativa de curva.
ms.openlocfilehash: 5f823e5930d3dad8bf6e20727e4b527493f89892
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821737"
---
# <a name="cell-element-relquadbezto-row-visio-xml"></a>Elemento de celda (fila RelQuadBezTo) ('XML de Visio')

Contiene las coordenadas x o y del extremo de una curva Bézier cuadrática con respecto al ancho de la forma y el alto o las coordenadas x o y del punto de control del ancho y alto de la forma relativa de curva.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |master # .xml, # .xml de página  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Elemento de fila (geometría)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelQuadBezTo_Type](relquadbezto_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del extremo de una curva Bézier cuadrática con respecto al ancho de la forma y el alto o las coordenadas x o y del punto de control del ancho y alto de la forma relativa de curva.  <br/> |
   
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
   
## <a name="remarks"></a>Comentarios

El atributo **N** de este elemento de **celda** debe ser uno de un conjunto limitado de valores que corresponden a las celdas de ShapeSheet. Hacer referencia a la tabla siguiente para determinar los valores del atributo **N** permitidas para este elemento de **celda** . 
  
|**Valor**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|X  <br/> |La coordenada x del vértice del extremo de una curva Bézier cuadrática con relación al ancho de la forma.  <br/> |[Fila RelQuadBezTo (sección Geometría)](relquadbezto-row-geometry-section.md) <br/> |
|v  <br/> |Coordenada y del vértice del extremo de una curva Bézier cuadrática con relación al alto de la forma.  <br/> |[Fila RelQuadBezTo (sección Geometría)](relquadbezto-row-geometry-section.md) <br/> |
|A  <br/> |Elija la coordenada x del control de la curva con respecto al ancho de la forma; un punto en el arco. El punto de control es mejor encuentra acerca de la mitad de la distancia entre el principio y el vértice final del arco.  <br/> |[Fila RelQuadBezTo (sección Geometría)](relquadbezto-row-geometry-section.md) <br/> |
|B  <br/> |Punto de la coordenada y de un control de la curva con relación al alto de la forma.  <br/> |[Fila RelQuadBezTo (sección Geometría)](relquadbezto-row-geometry-section.md) <br/> |
   

