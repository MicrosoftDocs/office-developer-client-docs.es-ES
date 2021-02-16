---
title: Elemento Cell (fila Ellipse) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 210e6731-7c94-90b1-c7c4-635df974fdb6
description: Contiene las coordenadas x o y del punto central de la elipse y dos puntos en la elipse.
ms.openlocfilehash: a2dde9cdc731595bfc8df646ab984cfbfb9db379
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541872"
---
# <a name="cell-element-ellipse-row-visio-xml"></a>Elemento Cell (fila Ellipse) (XML de Visio)

Contiene las coordenadas x o y del punto central de la elipse y dos puntos en la elipse.
  
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

Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Elemento Row (Geometría)](row-element-geometry-sectionvisio-xml.md) <br/> |[Ellipse_Type](ellipse_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y del punto central de la elipse y dos puntos de la elipse.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica una referencia a una página de dibujo.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |opcional  <br/> |Indica que la fórmula se evalúa como un error. El valor de **E** es el valor actual (una cadena de mensaje de error); el valor del atributo **V** es el último valor válido.  <br/> |Una cadena de mensaje de error.  <br/> |
|F  <br/> |xsd:string  <br/> |opcional  <br/> | Representa la fórmula del elemento. Este atributo puede contener una de las siguientes cadenas:  <br/>  '(alguna fórmula)' si la fórmula existe localmente  <br/>  `No Formula` si la fórmula se elimina o bloquea localmente  <br/>  `Inh` si la fórmula se hereda.  <br/> |Una fórmula.  <br/> |
|N  <br/> |xsd:string  <br/> |necesario  <br/> |Representa el nombre de la celda ShapeSheet.  <br/> |Nombre de la celda ShapeSheet.  <br/> Vea la sección Comentarios a continuación.  <br/> |
|U  <br/> |xsd:string  <br/> |opcional  <br/> |Representa una unidad de medida El valor predeterminado es DL.  <br/> |Unidades de la celda.  <br/> |
|V  <br/> |xsd:string  <br/> |opcional  <br/> |Representa el valor de la celda.  <br/> |Valor de la celda ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Comentarios

El **atributo N** de este elemento **Cell** debe ser uno de un conjunto limitado de valores que corresponden a las celdas de ShapeSheet. Consulte la tabla siguiente para determinar los valores del atributo **N** que se permiten para este **elemento Cell.** 
  
|**Valor**|**Descripción**|**Más información**|
|:-----|:-----|:-----|
|X  <br/> |Coordenada x del punto central.  <br/> |[Fila Ellipse (Sección de Geometría)](ellipse-row-geometry-section.md) <br/> |
|v  <br/> |Coordenada y del punto central.  <br/> |[Fila Ellipse (Sección de Geometría)](ellipse-row-geometry-section.md) <br/> |
|A  <br/> |Coordenada x del primer punto de la elipse; emparejada con la coordenada y representada por la celda B.  <br/> |[Fila Ellipse (Sección de Geometría)](ellipse-row-geometry-section.md) <br/> |
|B  <br/> |Coordenada y del primer punto de la elipse; emparejado con coordenada x representada por la celda A.  <br/> |[Fila Ellipse (Sección de Geometría)](ellipse-row-geometry-section.md) <br/> |
|C  <br/> |Coordenada x del segundo punto de la elipse; emparejada con la coordenada y representada por la celda D.  <br/> |[Fila Ellipse (Sección de Geometría)](ellipse-row-geometry-section.md) <br/> |
|D  <br/> |Coordenada y del segundo punto de la elipse; emparejada con la coordenada y representada por la celda C.  <br/> |[Fila Ellipse (Sección de Geometría)](ellipse-row-geometry-section.md) <br/> |
   

