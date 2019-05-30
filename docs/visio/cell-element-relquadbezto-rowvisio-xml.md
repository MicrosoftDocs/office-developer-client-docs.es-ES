---
title: Elemento cell (fila RelQuadBezTo) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8b3aea70-a69f-a85e-83d8-c0fa2ee68836
description: Contiene las coordenadas x o y del punto final de una curva Bézier cuadrática en relación con el ancho y el alto de la forma o las coordenadas x o y del punto de control del ancho y alto de la forma relativa de la curva.
ms.openlocfilehash: 7bdd55cfd5401c8455f09cf7d237117572d12723
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542390"
---
# <a name="cell-element-relquadbezto-row-visio-xml"></a>Elemento cell (fila RelQuadBezTo) (XML de Visio)

Contiene las coordenadas x o y del punto final de una curva Bézier cuadrática en relación con el ancho y el alto de la forma o las coordenadas x o y del punto de control del ancho y alto de la forma relativa de la curva.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Master #. XML, página #. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Elemento Row (geometría)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelQuadBezTo_Type](relquadbezto_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del punto final de una curva Bézier cuadrática en relación con el ancho y el alto de la forma o las coordenadas x o y del punto de control del ancho y alto de la forma relativa de la curva.  <br/> |
   
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
   
## <a name="remarks"></a>Observaciones

El atributo **N** de este elemento de **celda** debe ser uno de un conjunto de valores limitado que corresponda a las celdas de ShapeSheet. Consulte la tabla siguiente para determinar los valores del atributo **N** que se permiten para este elemento de **celda** . 
  
|**Value**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|X  <br/> |Coordenada x del vértice del extremo de una curva cuadrática de Bézier con relación al ancho de la forma.  <br/> |[Fila RelQuadBezTo (sección geometría)](relquadbezto-row-geometry-section.md) <br/> |
|v  <br/> |Coordenada y del vértice del extremo de una curva cuadrática de Bézier en relación con el alto de la forma.  <br/> |[Fila RelQuadBezTo (sección geometría)](relquadbezto-row-geometry-section.md) <br/> |
|A  <br/> |Coordenada x del punto de control de la curva con relación al ancho de la forma; un punto en el arco. El punto de control se encuentra mejor cerca de la mitad de la distancia entre los vértices inicial y final del arco.  <br/> |[Fila RelQuadBezTo (sección geometría)](relquadbezto-row-geometry-section.md) <br/> |
|B  <br/> |Coordenada y del punto de control de una curva en relación con el alto de la forma.  <br/> |[Fila RelQuadBezTo (sección geometría)](relquadbezto-row-geometry-section.md) <br/> |
   

