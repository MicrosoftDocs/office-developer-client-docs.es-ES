---
title: Elemento Cell (fila NURBSTo) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e76bae8f-b9de-39ef-1f56-b00a6cd2ba6c
description: Contiene las coordenadas x o y, la posición del segundo al último nudo, la posición del último peso, la posición del primer nudo, la posición del primer peso o la fórmula de una spline B racional no uniforme (NURBS).
ms.openlocfilehash: 3128149d1e787dde7677c2a202a29ac8efa6da43
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539491"
---
# <a name="cell-element-nurbsto-row-visio-xml"></a>Elemento Cell (fila NURBSTo) (Visio XML)

Contiene las coordenadas x o y, la posición del segundo al último nudo, la posición del último peso, la posición del primer nudo, la posición del primer peso o la fórmula de una spline B racional no uniforme (NURBS).
  
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
|[Elemento Row (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[NURBSTo_Type](nurbsto_type-complextypevisio-xml.md) <br/> |Contiene las coordenadas x o y, la posición del segundo al último nudo, la posición del último peso, la posición del primer nudo, la posición del primer peso o la fórmula de una spline B racional no uniforme (NURBS).  <br/> |
   
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
|X  <br/> |Coordenada x del último punto de control de una NURBS.  <br/> |[Fila NURBSTo (Sección de Geometría)](nurbsto-row-geometry-section.md) <br/> |
|v  <br/> |Coordenada y del último punto de control de una NURBS.  <br/> |[Fila NURBSTo (Sección de Geometría)](nurbsto-row-geometry-section.md) <br/> |
|A  <br/> |Penúltimo nodo de una NURBS.  <br/> |[Fila NURBSTo (Sección de Geometría)](nurbsto-row-geometry-section.md) <br/> |
|B  <br/> |Último grosor de una NURBS.  <br/> |[Fila NURBSTo (Sección de Geometría)](nurbsto-row-geometry-section.md) <br/> |
|C  <br/> |Primer nodo de una NURBS.  <br/> |[Fila NURBSTo (Sección de Geometría)](nurbsto-row-geometry-section.md) <br/> |
|D  <br/> |Primer grosor de una NURBS.  <br/> |[Fila NURBSTo (Sección de Geometría)](nurbsto-row-geometry-section.md) <br/> |
|E  <br/> |Fórmula de NURBS.  <br/> |[Fila NURBSTo (Sección de Geometría)](nurbsto-row-geometry-section.md) <br/> |
   

